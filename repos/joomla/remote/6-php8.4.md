## `joomla:6-php8.4`

```console
$ docker pull joomla@sha256:565faaf8bff33fdea96bc6515dea0d7af7d5a8fbfa805efed494d45652997209
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `joomla:6-php8.4` - linux; amd64

```console
$ docker pull joomla@sha256:2c2a55cff6d3f74fbcbf4c5d107fa234c2ac06a852a4763e606d6f550ebd543d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278052604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff092058e8782a14177016517a7068fd195817c4faef9deeecc217971a28eb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 18:36:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 13 Feb 2026 18:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 13 Feb 2026 18:36:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 18:36:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:36:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:36:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 13 Feb 2026 18:36:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 13 Feb 2026 18:36:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 13 Feb 2026 18:36:29 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 13 Feb 2026 18:36:29 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 13 Feb 2026 18:36:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:36:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:36:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:36:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 13 Feb 2026 18:36:29 GMT
ENV PHP_VERSION=8.4.18
# Fri, 13 Feb 2026 18:36:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Fri, 13 Feb 2026 18:36:29 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:36:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:36:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:39:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:39:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:39:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:39:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:39:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:39:15 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:39:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:39:15 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:39:15 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:39:15 GMT
CMD ["apache2-foreground"]
# Tue, 17 Feb 2026 21:47:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 17 Feb 2026 21:47:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 17 Feb 2026 21:47:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:50:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.28; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 17 Feb 2026 21:50:13 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 17 Feb 2026 21:50:13 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 17 Feb 2026 21:50:13 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 17 Feb 2026 21:50:13 GMT
VOLUME [/var/www/html]
# Tue, 17 Feb 2026 21:50:13 GMT
ENV JOOMLA_VERSION=6.0.3
# Tue, 17 Feb 2026 21:50:13 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Tue, 17 Feb 2026 21:50:14 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 17 Feb 2026 21:50:14 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:50:14 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 17 Feb 2026 21:50:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:50:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e733238083fbfd8924dd8848ef2e10dfe0782cd77f42c7abe8f9ee30642687`  
		Last Modified: Fri, 13 Feb 2026 18:39:37 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca87fb91f2941b900919a4ff7d86237c1f73a4f1d068d3046ed283fd620c411`  
		Last Modified: Fri, 13 Feb 2026 18:39:42 GMT  
		Size: 117.8 MB (117838975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70762577e1e3e472658e7d7d57f8690cfb14ce79ae7e1798c2e1d5f11f472934`  
		Last Modified: Fri, 13 Feb 2026 18:39:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526c6eceb8a766e7182b6410205ecbe1646e36247b591de1e74a6bee1188feee`  
		Last Modified: Fri, 13 Feb 2026 18:39:38 GMT  
		Size: 4.2 MB (4226878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53e63b4916e9c922fb92077d7ea89a160f7f404c13fa40b222225860dff7e6d`  
		Last Modified: Fri, 13 Feb 2026 18:39:38 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c647321481bc86b5ec20f93b222ae6a7121a11af3bcd53f14d09362d4f3028`  
		Last Modified: Fri, 13 Feb 2026 18:39:39 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbf310210fd277b33e249614642e03a180f509134fa8a2350f11879d552045d`  
		Last Modified: Fri, 13 Feb 2026 18:39:40 GMT  
		Size: 13.8 MB (13841086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:744e1c8a191154d34af2d8bf92ed2b170cd898d74b3fc288038d85e260221783`  
		Last Modified: Fri, 13 Feb 2026 18:39:39 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee063a2cc5cb32f4e9d8abfb023f5ffb5c93725bc66e92b9876a7a59233edd1`  
		Last Modified: Fri, 13 Feb 2026 18:39:40 GMT  
		Size: 13.5 MB (13545114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e06dfb6d55a4ffd9b0da651e2c6c83118a651eed298287a33b420d27a8794cb`  
		Last Modified: Fri, 13 Feb 2026 18:39:40 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec443dd4bdb12101f0e8c10a01f39cda29ea1a231f8336f33da48fb7e9e78c`  
		Last Modified: Fri, 13 Feb 2026 18:39:41 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe2b38940867259a852f82bc858a8d1eabe8ef077ca6962a3520462226ffda15`  
		Last Modified: Fri, 13 Feb 2026 18:39:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb6e44fb11c414978d829b618806edbfff6129da7778a9698685cdc6e074bc1`  
		Last Modified: Fri, 13 Feb 2026 18:39:42 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cefcbacba4e4e026a5d2b20ea95c1f0b51ec74fdef3a15058a1cdfcd39dde84`  
		Last Modified: Tue, 17 Feb 2026 21:50:25 GMT  
		Size: 27.3 MB (27273565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521bb769446b6d4072f3365eb4b7f20e7616326dd428834d9b47e87c86bb015f`  
		Last Modified: Tue, 17 Feb 2026 21:50:26 GMT  
		Size: 45.1 MB (45090155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d5aa6d7dabd1199abbd956b4c4bdb6cdfabff97dbe89f78818cd80029cbcbc`  
		Last Modified: Tue, 17 Feb 2026 21:50:24 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30cc644404e25c78beff66fceb3117b42f9014155525392f87b378f8c9275f5a`  
		Last Modified: Tue, 17 Feb 2026 21:50:24 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23061c5d6a9977467c09525d78895598c836b7e3cff4050171f9e2bd0140379d`  
		Last Modified: Tue, 17 Feb 2026 21:50:25 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b83fd7c4b6d1c4b76d9277ee417ec1a6f03fab3ead77ead80557b05fc445ceb`  
		Last Modified: Tue, 17 Feb 2026 21:50:26 GMT  
		Size: 26.4 MB (26428261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf3b1b52ffb62ac49eb362a17b07146e366832fc8426813bb116ab4f159e8ee`  
		Last Modified: Tue, 17 Feb 2026 21:50:26 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cad9f85fcf6f6dc01ff0f1d18609364be2640d6507898c7e307501c1be530cb`  
		Last Modified: Tue, 17 Feb 2026 21:50:26 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.4` - unknown; unknown

```console
$ docker pull joomla@sha256:301319fd3a2f75b84cbf52858123c61dc9b531fa2ac1f33f3303b834a7d174d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 KB (61387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7064d720a7c0c3b2b8e5d3bf30d05bcc3de09cedcdc72d28b916490c828302d3`

```dockerfile
```

-	Layers:
	-	`sha256:67b63592d3e3f06fa1ab1c33502c065e5fb28cb646b193679a3ec0d977e0868e`  
		Last Modified: Tue, 17 Feb 2026 21:50:24 GMT  
		Size: 61.4 KB (61387 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.4` - linux; arm variant v5

```console
$ docker pull joomla@sha256:fd009f55cbc36a15c530a188c13ac3c7ba569b2e4c25906037fb7f4c78de1f71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.0 MB (248979977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c79941ea8cb132b4d6c0485a36c7d9eeda1d68339f1588ab6a140dfdb9d1ad52`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 18:46:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 13 Feb 2026 18:47:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 13 Feb 2026 18:47:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 18:47:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:47:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:47:07 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 13 Feb 2026 18:47:07 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 13 Feb 2026 18:47:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 13 Feb 2026 18:47:17 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 13 Feb 2026 18:47:17 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 13 Feb 2026 18:47:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:47:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:47:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:47:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 13 Feb 2026 18:47:17 GMT
ENV PHP_VERSION=8.4.18
# Fri, 13 Feb 2026 18:47:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Fri, 13 Feb 2026 18:47:17 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:47:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:47:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:50:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:50:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:50:44 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:50:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:50:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:50:44 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:50:44 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:50:44 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:50:44 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:50:44 GMT
CMD ["apache2-foreground"]
# Tue, 17 Feb 2026 21:45:07 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 17 Feb 2026 21:45:07 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 17 Feb 2026 21:45:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:48:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.28; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 17 Feb 2026 21:48:45 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 17 Feb 2026 21:48:45 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 17 Feb 2026 21:48:45 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 17 Feb 2026 21:48:45 GMT
VOLUME [/var/www/html]
# Tue, 17 Feb 2026 21:48:45 GMT
ENV JOOMLA_VERSION=6.0.3
# Tue, 17 Feb 2026 21:48:45 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Tue, 17 Feb 2026 21:48:47 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 17 Feb 2026 21:48:47 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:48:47 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 17 Feb 2026 21:48:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:48:47 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c78e9d2a64a635d4112d81774fcad6603b8ae5cc5a2b50f64fe1c9d2e4aa63`  
		Last Modified: Fri, 13 Feb 2026 18:51:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b62f9424736dc8dc62919cab9bf300f81027c1b6206d3326c0e1ca0cc7260e1`  
		Last Modified: Fri, 13 Feb 2026 18:51:06 GMT  
		Size: 94.9 MB (94876136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a87fa3e0ae8e7c9e7441d54bd223dfb1fee7dc609509a4a9ad9568718e9e15e`  
		Last Modified: Fri, 13 Feb 2026 18:51:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f48cd0caccccec6964fb546415cf2c128ea5bcefb282a2a3ebf4b9ed580c867`  
		Last Modified: Fri, 13 Feb 2026 18:51:04 GMT  
		Size: 4.1 MB (4088849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69eab748c277c33e431d0e0c86f4e0237a69a590775e26920ff16c7a74f29b0`  
		Last Modified: Fri, 13 Feb 2026 18:51:04 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6301abdde8bf988391973a42239f16fd50b6b08de86364a787b3ad254c7fa5`  
		Last Modified: Fri, 13 Feb 2026 18:51:05 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea39ee1c8f5511358e499522112ed46bd3a7652eeb7b85371fac847954cbf63`  
		Last Modified: Fri, 13 Feb 2026 18:51:05 GMT  
		Size: 13.8 MB (13838451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3475b617821838a499e8529c1da0c6fa6d2ff083e99aa8e508804e7947d570d6`  
		Last Modified: Fri, 13 Feb 2026 18:51:06 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f47f33ee218a16754c461c916e85ca07ec0657721a818d9971cd0d4c03d52b7c`  
		Last Modified: Fri, 13 Feb 2026 18:51:06 GMT  
		Size: 12.2 MB (12199957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c913d2f04779ed25d3948dfa8f7f95a6984e83a06ef62f0f40cb422c05c1a446`  
		Last Modified: Fri, 13 Feb 2026 18:51:06 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aadfc9be3e69c09825ea0e04dd815c05dcab09009248c8d2fb2d5ea1379d202`  
		Last Modified: Fri, 13 Feb 2026 18:51:07 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3186b4edcb0280f9673be789e2d0a4219675ad9f7577c2b8f4d09a743541ac`  
		Last Modified: Fri, 13 Feb 2026 18:51:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01dac7114ef38299b5513f3aadd3142167ae9ea6f697fc3a14375cbb0e99136`  
		Last Modified: Fri, 13 Feb 2026 18:51:08 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1201129309328edfc8e68e9ab78644243f7e3faf05c34cde5b5d016e1454d8`  
		Last Modified: Tue, 17 Feb 2026 21:48:57 GMT  
		Size: 26.7 MB (26706151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf48ce485cef337a005f4e33eddb5ed688055fba979455ca9c2b159d42fae918`  
		Last Modified: Tue, 17 Feb 2026 21:48:58 GMT  
		Size: 42.9 MB (42864646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c5aec7c3962cb459ebb8626d1061135b236055b26b6fb1fb0ddae281d84f2e`  
		Last Modified: Tue, 17 Feb 2026 21:48:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f284258904c6e9e220ca42bd01f98e6808761372cc8fe9cd82866dbb52da3867`  
		Last Modified: Tue, 17 Feb 2026 21:48:56 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:956f0273a24238d8c4737949e7340e1a42f79d35e6e0aa29f499a07bc524091f`  
		Last Modified: Tue, 17 Feb 2026 21:48:57 GMT  
		Size: 18.8 KB (18796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036082d081e89019ab95b1a80d8161e5582b99fea2a873a5cdd3d95fb8102605`  
		Last Modified: Tue, 17 Feb 2026 21:48:58 GMT  
		Size: 26.4 MB (26428261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7991ace2797fcd8f0564d527dd196f67dfa1a31d4ee7f17642e69a2163f797`  
		Last Modified: Tue, 17 Feb 2026 21:48:49 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e248cd0175db716829ab8f6b4008db14e9a819a26b47e709aa9c224175679319`  
		Last Modified: Tue, 17 Feb 2026 21:48:50 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.4` - unknown; unknown

```console
$ docker pull joomla@sha256:efa9aa9a143a1b536d757f1df411f37418eb73bbb56322acbc6306ba2ee13107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 KB (61619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bba5dfd0e6a00f4bf9a574fea389b13f9c4877fc6d75609660b008aea6a2a50`

```dockerfile
```

-	Layers:
	-	`sha256:c0c9c871d5faef9c5e241b7f3b5cd55a5b6f3b808dfa266ccb9d8a985e710c5b`  
		Last Modified: Tue, 17 Feb 2026 21:48:55 GMT  
		Size: 61.6 KB (61619 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.4` - linux; arm variant v7

```console
$ docker pull joomla@sha256:174e712cfa0a58f0384fc07ebff7c9ca68eed74074a88e8ce27286bf77da9b24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.3 MB (235343194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9e818bfc812db3df9ae6c9dcc58889453451f6cf1d0c67baa01f2a7407fab3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 18:33:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 13 Feb 2026 18:33:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 13 Feb 2026 18:33:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 18:33:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:33:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 13 Feb 2026 18:33:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 13 Feb 2026 18:33:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 13 Feb 2026 18:33:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 13 Feb 2026 18:33:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 13 Feb 2026 18:33:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:33:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:33:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:33:50 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 13 Feb 2026 18:33:50 GMT
ENV PHP_VERSION=8.4.18
# Fri, 13 Feb 2026 18:33:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Fri, 13 Feb 2026 18:33:50 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:34:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:34:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:36:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:36:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:36:50 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:36:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:36:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:36:50 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:36:50 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:36:50 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:36:50 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:36:50 GMT
CMD ["apache2-foreground"]
# Tue, 17 Feb 2026 21:49:12 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 17 Feb 2026 21:49:12 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 17 Feb 2026 21:49:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:52:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.28; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 17 Feb 2026 21:52:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 17 Feb 2026 21:52:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 17 Feb 2026 21:52:12 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 17 Feb 2026 21:52:12 GMT
VOLUME [/var/www/html]
# Tue, 17 Feb 2026 21:52:12 GMT
ENV JOOMLA_VERSION=6.0.3
# Tue, 17 Feb 2026 21:52:12 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Tue, 17 Feb 2026 21:52:13 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 17 Feb 2026 21:52:14 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:52:14 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 17 Feb 2026 21:52:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:52:14 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eabdc9911afa5509d8b0529b842891062455a47f5b46a85b0781d251b8882c`  
		Last Modified: Fri, 13 Feb 2026 18:37:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7d1aa4452ec2c9c0eaf03ffa7b296992de52d278281d13609e452561fd382c`  
		Last Modified: Fri, 13 Feb 2026 18:37:10 GMT  
		Size: 86.2 MB (86244813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd66a8f03b9ea04881612d354b7e467db4bb172c3994c50f15297077f2388e96`  
		Last Modified: Fri, 13 Feb 2026 18:37:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e17a9655d719f905731ff924320a83586c4f49ff5e9b235eaf00b54e38cd5f17`  
		Last Modified: Fri, 13 Feb 2026 18:37:08 GMT  
		Size: 3.8 MB (3757550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887de3d23abc0d62374670f2e02d3df23907ba172a8ddac0c14fdd48407acef0`  
		Last Modified: Fri, 13 Feb 2026 18:37:09 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45905e290095d99a17416f425c41898fac1b10cc8c220b9a674ecc0981392902`  
		Last Modified: Fri, 13 Feb 2026 18:37:09 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9c98ee0e382d740393ac75aaa67274572c59082bea2527f399cce7e30ad6d6`  
		Last Modified: Fri, 13 Feb 2026 18:37:09 GMT  
		Size: 13.8 MB (13838590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8835cd014d7a4f8e7e429063ec92301dda7b1c589a7dd5d1af6d3a23e5dfd34c`  
		Last Modified: Fri, 13 Feb 2026 18:37:10 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e086ba02f8e71873d86d960cb80c81b027f004ea4e98ea2e0dd91f30d30965bd`  
		Last Modified: Fri, 13 Feb 2026 18:37:10 GMT  
		Size: 11.6 MB (11613539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a921d715a478eb9863a3cbffe8896a2e627e15d3dc4eaf42c32248ba268ba1`  
		Last Modified: Fri, 13 Feb 2026 18:37:11 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:317154feb758aea0d03cf17bc9752d36f450ce3bff414d6659a6b74a45c00c5b`  
		Last Modified: Fri, 13 Feb 2026 18:37:11 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37ffbdeb90fab70f46eaef8e25c890fba8a94d287d962fc6d6699352cd62ae3`  
		Last Modified: Fri, 13 Feb 2026 18:37:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a4db0503051ed9bfd38225ea004c831fb22c75d38808e4db5852e90633f597`  
		Last Modified: Fri, 13 Feb 2026 18:37:11 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dd736975313ffc6a98514b0a7c089278110d1754faed1f51fc6aec4cd23e1f`  
		Last Modified: Tue, 17 Feb 2026 21:52:22 GMT  
		Size: 25.9 MB (25925722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21001474deb93c0ae969f862e89e88fd4510bdc86c23a8844fab96053fa00ff`  
		Last Modified: Tue, 17 Feb 2026 21:52:23 GMT  
		Size: 41.3 MB (41291053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a15e1852b926c2d787764c2738e384275647738101052173697c876209ffce`  
		Last Modified: Tue, 17 Feb 2026 21:52:22 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191087c2a14c4124c07591efd89bfac1059703ce2d1c7fa3b501ef0e650ea649`  
		Last Modified: Tue, 17 Feb 2026 21:52:21 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438ba9d25e9cbb26fc2988ca2455d14ddb8914d9b443696d44f760e6d17d1261`  
		Last Modified: Tue, 17 Feb 2026 21:52:23 GMT  
		Size: 18.8 KB (18800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616d43e49a8056213c643b409a4a12574905b011a3224851d6ed0b02fbd47fc6`  
		Last Modified: Tue, 17 Feb 2026 21:52:23 GMT  
		Size: 26.4 MB (26428212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a57aaceffacccf93115b9eec8126a2ef11e2852123001e436f090ea70c9bda1`  
		Last Modified: Tue, 17 Feb 2026 21:52:06 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e099126140528b41df5561bdd45a7871a8684f0b0fea69313e1e7537fbeefa39`  
		Last Modified: Tue, 17 Feb 2026 21:52:07 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.4` - unknown; unknown

```console
$ docker pull joomla@sha256:07afcb256d1dfa98c60093f8c9132dd46a90a0be19b5a3e9a1bf1bc8986c106b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 KB (61619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe43742a14536022ea1ac793c9a663206ebdb9228cb6c4cf98f738c6ea60aabb`

```dockerfile
```

-	Layers:
	-	`sha256:27f7c2854b44ae464de8ac06bc3bfefe7d16f90a39948bc69d1b4756cc4db1e0`  
		Last Modified: Tue, 17 Feb 2026 21:52:21 GMT  
		Size: 61.6 KB (61619 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.4` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:0b662d657f7c6bb5b48244574d8c73b7bcb1182033edbd307dd2b96c63e08937
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269194607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daacbcea6eb002954fa924e7543667d1f43902a022f8b9078225d473af89f2f8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 18:36:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 13 Feb 2026 18:36:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 13 Feb 2026 18:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 18:36:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:36:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:36:41 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 13 Feb 2026 18:36:41 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 13 Feb 2026 18:36:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 13 Feb 2026 18:36:48 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 13 Feb 2026 18:36:48 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 13 Feb 2026 18:36:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:36:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:36:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:36:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 13 Feb 2026 18:36:48 GMT
ENV PHP_VERSION=8.4.18
# Fri, 13 Feb 2026 18:36:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Fri, 13 Feb 2026 18:36:48 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:36:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:36:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:40:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:40:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:40:04 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:40:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:40:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:40:04 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:40:04 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:40:04 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:40:04 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:40:04 GMT
CMD ["apache2-foreground"]
# Tue, 17 Feb 2026 21:47:46 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 17 Feb 2026 21:47:46 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 17 Feb 2026 21:47:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:50:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.28; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 17 Feb 2026 21:50:20 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 17 Feb 2026 21:50:20 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 17 Feb 2026 21:50:20 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 17 Feb 2026 21:50:20 GMT
VOLUME [/var/www/html]
# Tue, 17 Feb 2026 21:50:20 GMT
ENV JOOMLA_VERSION=6.0.3
# Tue, 17 Feb 2026 21:50:20 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Tue, 17 Feb 2026 21:50:22 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 17 Feb 2026 21:50:22 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:50:22 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 17 Feb 2026 21:50:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:50:22 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3d649018b59c03ef66e57603c3c55cd57c99868ff8f42066a3f2e6e6761271`  
		Last Modified: Fri, 13 Feb 2026 18:40:25 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82228c70c2bd46131caddc5803e7892ab866b2f017c5eecb2706f13af575a3cf`  
		Last Modified: Fri, 13 Feb 2026 18:40:28 GMT  
		Size: 110.2 MB (110165087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1933c10ef1ee9146e10a1ec5ec50d60a9315b9ebc6ea562bec0e13e32d2cc9`  
		Last Modified: Fri, 13 Feb 2026 18:40:25 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c439bc7c724d4c41132c8392020a3245b6c5dc3a0365ce7900113a66292a643`  
		Last Modified: Fri, 13 Feb 2026 18:40:26 GMT  
		Size: 4.3 MB (4304907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59fafb6c33982c0174a74887e8799f02bff008a07fdd6fc2a3779809db19bd74`  
		Last Modified: Fri, 13 Feb 2026 18:40:26 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed0d25f75be317f809b54e283661962edbdaec5bf294ea00b1edb3b6469f166`  
		Last Modified: Fri, 13 Feb 2026 18:40:26 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8a89edbcc2c4646464777756ea2f7757e0f6c5692e60d3a1399901a10c6f56`  
		Last Modified: Fri, 13 Feb 2026 18:40:28 GMT  
		Size: 13.8 MB (13840513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ff962e163e6ffa6513e61bfd84d2955e3413ed7d16ffcc75333ac5d0f654ee`  
		Last Modified: Fri, 13 Feb 2026 18:40:27 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c51721c989d91783e47544311a35fab5d96ca89268d1cc62c25983bcf64dac`  
		Last Modified: Fri, 13 Feb 2026 18:40:28 GMT  
		Size: 13.2 MB (13195211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbcfa4a11040578fa230012dec536cfaadc03ff1c5bed4ef8dda251fa45ee95`  
		Last Modified: Fri, 13 Feb 2026 18:40:29 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74deab8bf2f7d0c0985147173806170f6914324eee0a4286fc083676d2afb835`  
		Last Modified: Fri, 13 Feb 2026 18:40:29 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452e6f1052f378dc41ace47fbae77ebdb6abc9a8b8925918b3e1172982401068`  
		Last Modified: Fri, 13 Feb 2026 18:40:29 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2fb91388ca78f203b15e8bd606ff4f64371c229d1d7e72869a0ea9f1506171`  
		Last Modified: Fri, 13 Feb 2026 18:40:30 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81f1037254892c56f19476f3adc7cacd1ceff7bac0a1dca9e81765e81aea32c`  
		Last Modified: Tue, 17 Feb 2026 21:50:32 GMT  
		Size: 27.1 MB (27100111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ae9f84faefbfe5c794daf931f62bd9cb1263d52f01ee0ef9eebc53c5917c22`  
		Last Modified: Tue, 17 Feb 2026 21:50:32 GMT  
		Size: 44.0 MB (43990511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f2d511850ecc37c4915fbbdb42be99f43445dc34816a0fdcb6e6fe075cc50c`  
		Last Modified: Tue, 17 Feb 2026 21:50:31 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f578b8e871bb9a7d313657839f71a423ce99282ad839fc019b837669132051fd`  
		Last Modified: Tue, 17 Feb 2026 21:50:31 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e6ce0c52332888c4b14324a6f5150ff61351674f106bb3b99e910d8f2be88f`  
		Last Modified: Tue, 17 Feb 2026 21:50:32 GMT  
		Size: 18.8 KB (18793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a77667fc3fbde8fa98ad2355cc3974f29a9cf15025c97c328036a1412f4957`  
		Last Modified: Tue, 17 Feb 2026 21:50:33 GMT  
		Size: 26.4 MB (26428212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241526058cd623e61a61591b76f40691feac28fcd5cae4f21a810a7b57826b82`  
		Last Modified: Tue, 17 Feb 2026 21:49:57 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88894c73f4585d5e8010ac5eac7b161413f62db395a931d7b638654604b1a35`  
		Last Modified: Tue, 17 Feb 2026 21:49:57 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.4` - unknown; unknown

```console
$ docker pull joomla@sha256:fa09cc50239a7ad812f28b6628014f1bb5370e3d6ea903eeac7858d1027af377
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 KB (61710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33503a8ef98d3233d3e309585e009b83d94e3af0673e521646115c0de1422fc0`

```dockerfile
```

-	Layers:
	-	`sha256:3c568a32f9d4ea3880541453d1335d3c9dd10d774a484d0b5946443616747774`  
		Last Modified: Tue, 17 Feb 2026 21:50:30 GMT  
		Size: 61.7 KB (61710 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.4` - linux; 386

```console
$ docker pull joomla@sha256:bc5aced63a1af44c6961c888dc43bc0e6e578a2a5b49cee0314f839e18026903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 MB (279050964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e687f108032f9f7df1d31864452b085abf79af66718a8d51b733f7c787eb145`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 18:36:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 13 Feb 2026 18:36:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 13 Feb 2026 18:36:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 18:36:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:36:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:36:55 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 13 Feb 2026 18:36:55 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 13 Feb 2026 18:37:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 13 Feb 2026 18:37:02 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 13 Feb 2026 18:37:03 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 13 Feb 2026 18:37:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:37:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:37:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:37:03 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 13 Feb 2026 18:37:03 GMT
ENV PHP_VERSION=8.4.18
# Fri, 13 Feb 2026 18:37:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Fri, 13 Feb 2026 18:37:03 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:37:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:37:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:40:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:40:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:40:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:40:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:40:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:40:09 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:40:09 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:40:09 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:40:09 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:40:09 GMT
CMD ["apache2-foreground"]
# Tue, 17 Feb 2026 21:47:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 17 Feb 2026 21:47:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 17 Feb 2026 21:47:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 21:50:16 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.28; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 17 Feb 2026 21:50:16 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 17 Feb 2026 21:50:16 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 17 Feb 2026 21:50:17 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 17 Feb 2026 21:50:17 GMT
VOLUME [/var/www/html]
# Tue, 17 Feb 2026 21:50:17 GMT
ENV JOOMLA_VERSION=6.0.3
# Tue, 17 Feb 2026 21:50:17 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Tue, 17 Feb 2026 21:50:18 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 17 Feb 2026 21:50:18 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 21:50:18 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 17 Feb 2026 21:50:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 21:50:18 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba9835133d9b5c9df9d246f78ab4edd8f3f4d8f90feb937375b4a2f82d39ed13`  
		Last Modified: Fri, 13 Feb 2026 18:40:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb4e64367763eb8a314079e7efdac346a2cd0094ced998d749f6e6fecc67c83`  
		Last Modified: Fri, 13 Feb 2026 18:40:32 GMT  
		Size: 116.1 MB (116140032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8639968547263a3fc9ae0fed0c8a680b57c90d33194ab3e48e4c50b4874cf78c`  
		Last Modified: Fri, 13 Feb 2026 18:40:29 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbfd2769b2c421b6255cb4d1c8f3791207b1d79dcf658aba97fa0187c7a80964`  
		Last Modified: Fri, 13 Feb 2026 18:40:29 GMT  
		Size: 4.5 MB (4458290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9043c9539642788dbdb72453a526acf34613e53c5e870e9b050fa74d93bd6d80`  
		Last Modified: Fri, 13 Feb 2026 18:40:30 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78149712856a1337eb4cfdcb16c8e8d788c855706d59f32d6d557b6a63b9876`  
		Last Modified: Fri, 13 Feb 2026 18:40:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39c707f7f72dc5834cbe4482efa16c040bb3f38ee93867a7ed427818bf49e5d`  
		Last Modified: Fri, 13 Feb 2026 18:40:31 GMT  
		Size: 13.8 MB (13839989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3986be460edea7a45f0ee4c3983d687194d2c29704b8eb2183417820f966e4d2`  
		Last Modified: Fri, 13 Feb 2026 18:40:31 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804dd8160c411eac116bfbe023ec5cbc96f9fb3c54c70c0f89f75bbc7dd0821a`  
		Last Modified: Fri, 13 Feb 2026 18:40:32 GMT  
		Size: 13.8 MB (13841943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e607c0afaf9f10c25860c1d9667edda32c7395ba289b774475d8eabb6d431f4`  
		Last Modified: Fri, 13 Feb 2026 18:40:32 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c10570c87332d98793c68bc15322870c5fa5d0adaeefd56075ee2a9e3e794f3`  
		Last Modified: Fri, 13 Feb 2026 18:40:32 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4ddf18b642dacf78211cb086c6cf8e1188556db3065f50c9b976621895a0ef`  
		Last Modified: Fri, 13 Feb 2026 18:40:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4714148ca8b5efd89ad2ae7e09ba3a69a998dd9c68aa962cf7d4d5d50aa258dc`  
		Last Modified: Fri, 13 Feb 2026 18:40:33 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8937b3d0064506f049c5de37e97313922288029e6d93649f7ce8f00350f6d29`  
		Last Modified: Tue, 17 Feb 2026 21:50:29 GMT  
		Size: 27.7 MB (27715935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8478967bd7a9bc32040fc9c6751de3903ebd244b80ca64135dc2699b9ea2d46`  
		Last Modified: Tue, 17 Feb 2026 21:50:29 GMT  
		Size: 45.3 MB (45302682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aec9d001b939bb268817dc8830d2d923ce82796f5c9256aef3f9df5e4d10b17`  
		Last Modified: Tue, 17 Feb 2026 21:50:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6731c888555e2708cf52fc139bb707810378273e3af2ba0db5cb878c511be1d9`  
		Last Modified: Tue, 17 Feb 2026 21:50:28 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b584176a891c393f62cdb1ce8e3ef6603d506141d213bcbd018ffa0af2002dd5`  
		Last Modified: Tue, 17 Feb 2026 21:50:29 GMT  
		Size: 18.8 KB (18795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9833cd83e1928a07d151781bded1fc6ebeb533952ee11fc23d67edb611f9d22f`  
		Last Modified: Tue, 17 Feb 2026 21:50:30 GMT  
		Size: 26.4 MB (26428258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfd091295d7a270626e80b0d9c014f5a1bde4c8c76431d87b9c27f539be265b`  
		Last Modified: Tue, 17 Feb 2026 21:50:03 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe2c3146bea0de3ae1fba4d5a64bc7b059c8bd9fa6852150c959eb834eddb74`  
		Last Modified: Tue, 17 Feb 2026 21:50:03 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.4` - unknown; unknown

```console
$ docker pull joomla@sha256:95bafc77793e5afc96e8688ba27b39792d940f49d8bd3e335793ed781dbc47bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 KB (61285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21bdb454e2587b36ca805668c6342db60d43da71df4953afecd8fbc4d3360bad`

```dockerfile
```

-	Layers:
	-	`sha256:f2ef7bbdb5652b0d1e5d93377f4a3ac102579d559875faefa0f8c4904676d02b`  
		Last Modified: Tue, 17 Feb 2026 21:50:28 GMT  
		Size: 61.3 KB (61285 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.4` - linux; s390x

```console
$ docker pull joomla@sha256:a22bc75db025cf777c6574f662689090f367e811af252f61c55ef04429b382e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252522273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d27462d4bef7261f5fd43b2a4540c9b32c9add8627d79f9b3e8c0a7b895926`
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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 03 Feb 2026 02:43:34 GMT
ENV PHP_VERSION=8.4.18
# Tue, 03 Feb 2026 02:43:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 03 Feb 2026 02:43:34 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Fri, 13 Feb 2026 18:52:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:52:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:58:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:58:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:58:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Feb 2026 18:58:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:58:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:58:28 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:58:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:58:28 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:58:28 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:58:28 GMT
CMD ["apache2-foreground"]
# Tue, 17 Feb 2026 22:28:15 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 17 Feb 2026 22:28:15 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 17 Feb 2026 22:28:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Feb 2026 22:33:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.28; 	pecl install memcached-3.4.0; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 17 Feb 2026 22:33:15 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 17 Feb 2026 22:33:15 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 17 Feb 2026 22:33:16 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 17 Feb 2026 22:33:16 GMT
VOLUME [/var/www/html]
# Tue, 17 Feb 2026 22:33:16 GMT
ENV JOOMLA_VERSION=6.0.3
# Tue, 17 Feb 2026 22:33:16 GMT
ENV JOOMLA_SHA512=2390bd8b741e948d8b5b93b14b16a7aa7d6e60b8d0a18eb678be5ae11b664cfd375def9a8398b979a7fdcbe8eb30b75ae0ef25d95fcbd11a5f435450c8a75608
# Tue, 17 Feb 2026 22:33:18 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.3/Joomla_6.0.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 17 Feb 2026 22:33:18 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:33:19 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 17 Feb 2026 22:33:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Feb 2026 22:33:19 GMT
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
	-	`sha256:b74774ed0609fe8edb040f36b41b0f6fef790c385ca86cbaf291f9c9afe0c983`  
		Last Modified: Fri, 13 Feb 2026 18:58:49 GMT  
		Size: 13.9 MB (13854826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14a3f988451034a5cd1e1d535ee3fe12691b0a1fbe4cad1ef735f6ff2c94188c`  
		Last Modified: Fri, 13 Feb 2026 18:58:49 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a420a9c05fe68343692f84af266cb80e305799d86e948488eca6c0ef8657262`  
		Last Modified: Fri, 13 Feb 2026 18:58:49 GMT  
		Size: 13.3 MB (13306866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b291ea97a924bc1eb388e5ae7232dc6525dba0a3dcad7ee0e6ba49a8ab01b2`  
		Last Modified: Fri, 13 Feb 2026 18:58:49 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a235280065792a93ee20b7eb37982d37db4fa3f251399580ad8761a4b9abd933`  
		Last Modified: Fri, 13 Feb 2026 18:58:50 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3b1cbfe7ce9abaca97e35fbf6234aeef3425ffe5b9c1d86e090940ad4ebff5`  
		Last Modified: Fri, 13 Feb 2026 18:58:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae98f19e17bc452b3d775ecb8fdc641bb64c30108aa34d54d773b46b0662104`  
		Last Modified: Fri, 13 Feb 2026 18:58:50 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08ba5eaf3da4509cf818bf241f529862bc34d33eddc767fdf5aea8dcb820b37`  
		Last Modified: Tue, 17 Feb 2026 22:33:44 GMT  
		Size: 27.6 MB (27552355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473256c52b0e21b5c82bb510b9f8d658e3799f28ddf6905c1ff6cf27e7046602`  
		Last Modified: Tue, 17 Feb 2026 22:33:44 GMT  
		Size: 44.6 MB (44615478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f774c4724f340a3340954c436c10ae76a20b5102ece074db8d40ff18e01a0d`  
		Last Modified: Tue, 17 Feb 2026 22:33:43 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a249175ad7d6de56fb26e65cc0b2af6826b4b9de4e52dd730f7b92d32cf73d7`  
		Last Modified: Tue, 17 Feb 2026 22:33:43 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8944b3807701a57af078f623d6d478933c8e57a96ef56d84f86d0db4e13348`  
		Last Modified: Tue, 17 Feb 2026 22:33:44 GMT  
		Size: 18.8 KB (18807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6e114d38a3546d946628d4696a8d27406c0c291549b14b0f8bdd4cf00edb1c`  
		Last Modified: Tue, 17 Feb 2026 22:33:44 GMT  
		Size: 26.4 MB (26428217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625b465e3b6b49278f152bf3bd18ac7226ef0857644c1cb6de15eafd04187484`  
		Last Modified: Tue, 17 Feb 2026 22:33:45 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78beb720ebb2a9bb904c787d486c718f8adec3eac515143c1502d0276c6edee6`  
		Last Modified: Tue, 17 Feb 2026 22:33:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.4` - unknown; unknown

```console
$ docker pull joomla@sha256:5077f13f64639148d0759c9c8f086830502e33efe024bee11b8efef209ebdd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 KB (61378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7126a18b7c14ce4d3986f96fdd2566f4ea68bd648f218edd22f4191ff4c4f9c3`

```dockerfile
```

-	Layers:
	-	`sha256:db996b32707f4a8a1c2d974437346d2f7aeae43621123fa19cf9c93c5fe96df2`  
		Last Modified: Tue, 17 Feb 2026 22:33:42 GMT  
		Size: 61.4 KB (61378 bytes)  
		MIME: application/vnd.in-toto+json
