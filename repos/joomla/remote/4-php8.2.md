## `joomla:4-php8.2`

```console
$ docker pull joomla@sha256:2d9d274613be1480f7ffb9ab01e026900954b32c1cc30e6b02aec6e088a5ce5c
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `joomla:4-php8.2` - linux; amd64

```console
$ docker pull joomla@sha256:afcabff513ed225a8a1f43bebc6770ec479028c73c474b6e6cffc18cd4672364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 MB (260264460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2666e754301050c558a1ab9af486227d828e3bb59aaa7363458802d1adc8bfc5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 19 Feb 2025 09:48:51 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Feb 2025 09:48:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_VERSION=8.2.28
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Feb 2025 09:48:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 19 Feb 2025 09:48:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
WORKDIR /var/www/html
# Wed, 19 Feb 2025 09:48:51 GMT
EXPOSE map[80/tcp:{}]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
# Wed, 19 Feb 2025 09:48:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
VOLUME [/var/www/html]
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_VERSION=4.4.11
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_SHA512=f72d4ed13388ad20c3a65542262414867a05e67360cd771d0526e09b907bb44f3ae08b9eeb2a0b98316b787352dce6a47452f8c4fbac970666908e5357d0e43d
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.11/Joomla_4.4.11-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db2c4b6137bab7816c2890896c1881e39d1ee6d7d7da17e6c4a6f2cc4e632dd`  
		Last Modified: Mon, 17 Mar 2025 23:22:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacb60b59038a7ef1b0ead1aa77dddbd90635ca615d432b337f5b423c2a7819b`  
		Last Modified: Mon, 17 Mar 2025 23:22:58 GMT  
		Size: 104.3 MB (104328581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64450047668b4e16566bc65aadfc64131a56987f311f72781177e2582da7d8a9`  
		Last Modified: Mon, 17 Mar 2025 23:22:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6386e035f70fdca57edaaa0ed712975fe278516c07a65984b58cb50caa6ed4`  
		Last Modified: Mon, 17 Mar 2025 23:22:57 GMT  
		Size: 20.1 MB (20123813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ca7ebe0914e6f7ef8ecda20d46c1692ddaa78f34c8a1012878b31e7257b055`  
		Last Modified: Mon, 17 Mar 2025 23:22:57 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc5d90893960a28fbed32dbe825dd152f5ef8a348c397b231e91ed17973cfbc`  
		Last Modified: Mon, 17 Mar 2025 23:22:57 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1778f52baa09242b5bb27700fd3fb4cc2e731b6b4ac864ebf9f7c47da6df95f1`  
		Last Modified: Mon, 17 Mar 2025 23:22:58 GMT  
		Size: 12.3 MB (12276272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d9cb1c80ec9c2623a90e39fb65bdd2f2a1497f057e4a1bc018705741194266`  
		Last Modified: Mon, 17 Mar 2025 23:22:58 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b116c8459f57bedd5203bcd82ec4615ca2027180b8bfabb1099a63451b9c55dc`  
		Last Modified: Mon, 17 Mar 2025 23:22:58 GMT  
		Size: 11.4 MB (11422347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8ddda3587a04d1f2b9447af88bc04dad17cdea7ddde30903e8ff071eaa93b8`  
		Last Modified: Mon, 17 Mar 2025 23:22:59 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f432ea27fc70617896d7649c5e84841920d952f814a2d0542072579f973c4bac`  
		Last Modified: Mon, 17 Mar 2025 23:22:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5a37a900f389490b1e07974aa4d5dba839383cd8759a5685e00a95a8c8e657`  
		Last Modified: Mon, 17 Mar 2025 23:22:59 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcf53ee4a8629adcbddcb73590fb7d04a65458406f93b3a0568e08ae5ae2750`  
		Last Modified: Tue, 18 Mar 2025 00:20:21 GMT  
		Size: 26.3 MB (26254122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f55c24068b068acc58b3efa138701f86f46782a47c444571635069fa5941e4`  
		Last Modified: Tue, 18 Mar 2025 00:20:21 GMT  
		Size: 31.3 MB (31269654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2bc65255323b63ea0ced211bac2944030b0c4d24999d707da92a924d600ee0`  
		Last Modified: Tue, 18 Mar 2025 00:20:21 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e4c981b1f5a56e3af065526b230ae6d8dd23f3c1a86d50574db503e932a5827`  
		Last Modified: Tue, 18 Mar 2025 00:20:21 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0052a2c69e089d59c12b653f7d4e098be8e1bf0f6b8d2750a3c23f40549b9a4`  
		Last Modified: Tue, 18 Mar 2025 00:20:21 GMT  
		Size: 19.2 KB (19157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e36a642129da95be959a82943e9d32b19cc5fa84aa95dfcd40ed6d496d94802`  
		Last Modified: Tue, 18 Mar 2025 00:20:22 GMT  
		Size: 26.4 MB (26354696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c543e4d75e58d6b25b1fa959f6aef492fde873a254874874237ded15368a3bd8`  
		Last Modified: Tue, 18 Mar 2025 00:20:22 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3faba345ae3f62abff7aad3750e48b10a3027182120046529685e44477ecd3`  
		Last Modified: Tue, 18 Mar 2025 00:20:22 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2` - unknown; unknown

```console
$ docker pull joomla@sha256:a6545216153ab0a18e21696738c401ed358755c740f6fed0ac918c75ef122789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 KB (61109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296c08b751540c2ccc53acb8e6e2fd4cf84ee7e47a0acd59988016dbabec70e8`

```dockerfile
```

-	Layers:
	-	`sha256:9387b5677b800d862779ff8b04d44bca426a598a3ac7267a974ae12efac080b8`  
		Last Modified: Tue, 18 Mar 2025 00:20:20 GMT  
		Size: 61.1 KB (61109 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2` - linux; arm variant v5

```console
$ docker pull joomla@sha256:fad377b37aa492052f7d9308c096df421d1cb39b07c1fd227a03ff9017455e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.9 MB (229885637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2fd106b84673f21fc9998e539ad1aca3ea3ec7c5181aef13eb2f8502a032b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 19 Feb 2025 09:48:51 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Feb 2025 09:48:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_VERSION=8.2.28
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Feb 2025 09:48:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 19 Feb 2025 09:48:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
WORKDIR /var/www/html
# Wed, 19 Feb 2025 09:48:51 GMT
EXPOSE map[80/tcp:{}]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
# Wed, 19 Feb 2025 09:48:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
VOLUME [/var/www/html]
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_VERSION=4.4.11
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_SHA512=f72d4ed13388ad20c3a65542262414867a05e67360cd771d0526e09b907bb44f3ae08b9eeb2a0b98316b787352dce6a47452f8c4fbac970666908e5357d0e43d
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.11/Joomla_4.4.11-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3014e21b6e4396df02c7cc3c5f126fa29d531fa5a1ad0b40b80de6794ae2694`  
		Last Modified: Tue, 25 Feb 2025 02:51:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e0a56f6198eb0af5102ce28eda7b5a34384f5b54701b7346487229bff9e9c`  
		Last Modified: Tue, 25 Feb 2025 02:51:20 GMT  
		Size: 82.0 MB (81993202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24b0f2499da71327f565769347ea1f63e9070dfa8385025f0465d80e603c361`  
		Last Modified: Tue, 25 Feb 2025 02:51:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21a0010d00b089e3a34b60fddcac813cd3a1211368d868b76aa3c52acf85f39`  
		Last Modified: Tue, 25 Feb 2025 02:55:46 GMT  
		Size: 19.4 MB (19419190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836efc0ee062aca6556d741fb3e390ca6b509fc639049bef1cfc24e29616d566`  
		Last Modified: Tue, 25 Feb 2025 02:55:45 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb27253beef75bf260f9071d9fb96a1614335f2b1af270afddf706a8142cb7b`  
		Last Modified: Tue, 25 Feb 2025 02:55:45 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011930897f0e94f8908d35816b869c1916d4b7c5e69b013a14bd68af54513b64`  
		Last Modified: Fri, 14 Mar 2025 01:16:18 GMT  
		Size: 12.3 MB (12274462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9587ba2e3349206ea532f4464028c241e4ad1121298357feaccd286fca85d8fd`  
		Last Modified: Fri, 14 Mar 2025 01:16:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a585b6944c1433eff35267ab704ba7545360430398014d7bb676ae940a46c5f3`  
		Last Modified: Fri, 14 Mar 2025 01:16:18 GMT  
		Size: 10.4 MB (10406221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411a0c4868fccc79fa986919a6a2d409dc1b8ba5c006b941e9492a700c79ffcd`  
		Last Modified: Fri, 14 Mar 2025 01:16:16 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c8577ccb7b4d01bfe8006afd0838fc8d07519bd88b0f59867e8b3384427b27`  
		Last Modified: Fri, 14 Mar 2025 01:16:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b7bacb438358389faa51d6b6f86912db59267c3bfff4f8d02c547b4970ac24`  
		Last Modified: Fri, 14 Mar 2025 01:16:18 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48d2abef632da5efd679df3091688455df11e6ee6d0bc7f7265aa4ff260e0a0`  
		Last Modified: Fri, 14 Mar 2025 03:58:22 GMT  
		Size: 25.7 MB (25704054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92833a0890f29cf2bf0322a565204e1d3f1de0e546b8efb46ef22c02ee1fc309`  
		Last Modified: Fri, 14 Mar 2025 03:58:22 GMT  
		Size: 28.0 MB (27963059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633204ebd9276354a416476ffdbdbb048520cb3ecbe5f85cb1eb1f7a58a8a49c`  
		Last Modified: Fri, 14 Mar 2025 03:58:21 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737be24409df886c09272d3b2a4f8a1b0642422b80bfbbe34b1c0cc39c1958cf`  
		Last Modified: Fri, 14 Mar 2025 03:58:21 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f17af51d9be8dc526a00ec718d0dfede427f868a086089e4c0eaaa0ab3b899a`  
		Last Modified: Fri, 14 Mar 2025 03:58:22 GMT  
		Size: 19.2 KB (19155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393659547ccaa3bf8c4a6d9a18ef2caa590537f3e73c1dcc16c4ae0c8391bc3b`  
		Last Modified: Fri, 14 Mar 2025 03:58:23 GMT  
		Size: 26.4 MB (26354702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04e2690d045962f277b74348398d642d89b9014cfbc836c4bc323d7d2f97eff`  
		Last Modified: Fri, 14 Mar 2025 03:58:23 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23794385884bb134fc6a4a2d21737f46ba813b3eb5d67dcb2a0c5fe961b555ea`  
		Last Modified: Fri, 14 Mar 2025 03:58:23 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2` - unknown; unknown

```console
$ docker pull joomla@sha256:04c610b1be87dbb325c58692b0e36d645b8cdb4547e782a4258abc43ec703d71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 KB (61305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ae0fa6be8860fd44866995fdc932edf10b6457636d6aee7d1b9940c47e83c8`

```dockerfile
```

-	Layers:
	-	`sha256:bf1ad9dca9bb6d8d6e3586bc2dc35c8df51c42dd300908f444f2ab8295fb3a8b`  
		Last Modified: Fri, 14 Mar 2025 03:58:21 GMT  
		Size: 61.3 KB (61305 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2` - linux; arm variant v7

```console
$ docker pull joomla@sha256:9bfd12e5452f8eeb33920ee260e61a6cc42b21df442c306d34a1bca7c13381b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.9 MB (218890708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf538fcc76f4f9293f39f71ee1989588a614985f5b7e22be1550688d377a1ebf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 19 Feb 2025 09:48:51 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Feb 2025 09:48:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_VERSION=8.2.28
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Feb 2025 09:48:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 19 Feb 2025 09:48:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
WORKDIR /var/www/html
# Wed, 19 Feb 2025 09:48:51 GMT
EXPOSE map[80/tcp:{}]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
# Wed, 19 Feb 2025 09:48:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
VOLUME [/var/www/html]
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_VERSION=4.4.11
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_SHA512=f72d4ed13388ad20c3a65542262414867a05e67360cd771d0526e09b907bb44f3ae08b9eeb2a0b98316b787352dce6a47452f8c4fbac970666908e5357d0e43d
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.11/Joomla_4.4.11-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d7e09b1d1dfb9227526dbb14ab0477c0b3e235584b36c16282a130f9eb0f3c`  
		Last Modified: Tue, 25 Feb 2025 02:45:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195d4e13a8d04cec48669402c294b437f110e69a04f231bf7f4fb038ce009feb`  
		Last Modified: Tue, 25 Feb 2025 02:45:31 GMT  
		Size: 76.2 MB (76162862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86b4b4427af4c394c935ad45142cba4e205bc21eb933d83f2d2432a5bb3cb64`  
		Last Modified: Tue, 25 Feb 2025 02:45:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9b346bd0d0d97918e8cf0f24429f88856b2aa9caf305b66eabeebc6aa67c68`  
		Last Modified: Tue, 25 Feb 2025 02:49:24 GMT  
		Size: 18.9 MB (18857331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffc087e149899d6dd0d9896e9ad11e94fde980bb585468298c7ea4818bc83fa`  
		Last Modified: Tue, 25 Feb 2025 02:49:23 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7d03bc48135c9bb3b0743190bd1e7146614e74be185bd6df7aefdde677f36`  
		Last Modified: Tue, 25 Feb 2025 02:49:23 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca55268812e11194ac6da5f8dfe55c2a2bfe36bec36b6adabc948f37aef2441`  
		Last Modified: Fri, 14 Mar 2025 01:54:42 GMT  
		Size: 12.3 MB (12274399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658ead82e47824e201b84ce34dc6b30aa6f00e04046656ad32b891b16a2d48a7`  
		Last Modified: Fri, 14 Mar 2025 01:54:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093c3f72e12b9a6df9cf0b13861d867429085d00c23f1ae4ae75ee409070ada5`  
		Last Modified: Fri, 14 Mar 2025 01:54:42 GMT  
		Size: 9.8 MB (9835035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030631fb211d507b82460f46b15838a2640d677fb540609af2c9111a30dc0893`  
		Last Modified: Fri, 14 Mar 2025 01:54:41 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6e39de97c5da8ef26cef2a299a131321c156c7aad8bccc78fe803440f048e3`  
		Last Modified: Fri, 14 Mar 2025 01:54:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ddac072af4ba756e13d94184df50acb1689e261380eebadd74a7357b625944`  
		Last Modified: Fri, 14 Mar 2025 01:54:42 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d86c348cfefd62193b3e34b77ef189cfd07541cfed05dfbcc49105a975dda0`  
		Last Modified: Fri, 14 Mar 2025 05:19:21 GMT  
		Size: 25.1 MB (25077385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db6cb056d9d26f06ceb86d0fb38a2ddb99449ed4544db4a681e8c27c47ed7d5`  
		Last Modified: Fri, 14 Mar 2025 05:19:22 GMT  
		Size: 26.4 MB (26379152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c76463e34c055d0d25bea4fca24ece901eeeea46c50afb67a83a1c44f374f5c`  
		Last Modified: Fri, 14 Mar 2025 05:19:20 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa773d6fd0b5bc92e9cbbfb31783ff4040398023279f4054c41917f26870ddf`  
		Last Modified: Fri, 14 Mar 2025 05:19:20 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de3e179fd7fa2b45d07a6799983aa956088923fc1508db704770ac25b297aedd`  
		Last Modified: Fri, 14 Mar 2025 05:19:21 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2e211e885040160a5068c1da87f2eecf20b08ed8a97539442d2ec77b6f9238`  
		Last Modified: Fri, 14 Mar 2025 05:19:22 GMT  
		Size: 26.4 MB (26354696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e445911039d93931ef4dfa48a96d7c31bbd07581abc9a8beec58d8d81b44f9e7`  
		Last Modified: Fri, 14 Mar 2025 05:19:22 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30edac80baf0462e80d93407dfdb8a604f9850aeb63a2685707336cde438232a`  
		Last Modified: Fri, 14 Mar 2025 05:19:22 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2` - unknown; unknown

```console
$ docker pull joomla@sha256:0c9b8d08b8d8806a9259deefc8245f278a180e48816e7564d24a607a7dda9ea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 KB (61295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc993a8e11c298c48a3de02a8f52dff8dab4d3642e79ae60ac2255544363c721`

```dockerfile
```

-	Layers:
	-	`sha256:d3d2dc4267544058e06bd924c04192ff9a528ef2e54a9f2fd275c08cc353ceb2`  
		Last Modified: Fri, 14 Mar 2025 05:19:19 GMT  
		Size: 61.3 KB (61295 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:f0b2f03c33d6fef4f72c4866e276cbdc86d6d5610b0d8e9b696d169152e6ccea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.4 MB (251430814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1c8099463278a0079289844ef5e3d0288bf6a34b028b69f0af1bc7388be6b3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 19 Feb 2025 09:48:51 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Feb 2025 09:48:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_VERSION=8.2.28
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Feb 2025 09:48:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 19 Feb 2025 09:48:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
WORKDIR /var/www/html
# Wed, 19 Feb 2025 09:48:51 GMT
EXPOSE map[80/tcp:{}]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
# Wed, 19 Feb 2025 09:48:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
VOLUME [/var/www/html]
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_VERSION=4.4.11
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_SHA512=f72d4ed13388ad20c3a65542262414867a05e67360cd771d0526e09b907bb44f3ae08b9eeb2a0b98316b787352dce6a47452f8c4fbac970666908e5357d0e43d
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.11/Joomla_4.4.11-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffecde8bd985cf96f0467d70fccc665026fdab770dcac3f793be1deba85a30`  
		Last Modified: Tue, 25 Feb 2025 03:07:28 GMT  
		Size: 20.1 MB (20120919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab17c0b9534d8803a88e819a77b6257c8c52458e1501948f051ab897599e4bb`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d58237634f94d2abae7d95c65d651fb63692600b04577a084ebafecdf4289`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e90b2bd595f1b698405f17f0629ce419a792ba331dd2031c3f994e214f16ff2`  
		Last Modified: Fri, 14 Mar 2025 01:30:21 GMT  
		Size: 12.3 MB (12276121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0a74f9f5b89d073aef7d444978d000beff453a3100e413ebfd9725f834c08f`  
		Last Modified: Fri, 14 Mar 2025 01:30:20 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2bbce36a490befad63f47f89c0fc62d11d144ff038975543f4a9a56f0f94093`  
		Last Modified: Fri, 14 Mar 2025 01:30:21 GMT  
		Size: 11.4 MB (11427441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf401480833167873b10b6754698cb70d477aac3fd9ec55d5ca0a7825421b644`  
		Last Modified: Fri, 14 Mar 2025 01:30:20 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44947c08ce8d43a1f48190e260a0bfdff889b32ff0f23426da43c5412f0abdf5`  
		Last Modified: Fri, 14 Mar 2025 01:30:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bca8678cf40ddeba98ba19c1259f2ada833081e7f1e7681f718f60944f96d50`  
		Last Modified: Fri, 14 Mar 2025 01:30:21 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb842bf28cab4a9f5387e5c6d4b3dd22111c5cb104a5f4ce4ee89f3e4157608`  
		Last Modified: Fri, 14 Mar 2025 06:21:54 GMT  
		Size: 26.2 MB (26175470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a811af5ffe562f97702b7228e348b7645171b82d661e7a31536fcae8b65a09`  
		Last Modified: Fri, 14 Mar 2025 06:21:54 GMT  
		Size: 28.9 MB (28867166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bdeedd41cdb64b8f1c2186f1163dcd2138c15d460db4208210ab0e0400c6d2`  
		Last Modified: Fri, 14 Mar 2025 06:21:53 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:172772c83fdd3d8bd2f3cc386149cf6a5879ad42826028faa40fefa62dcbe692`  
		Last Modified: Fri, 14 Mar 2025 06:21:53 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e48e3a8f81833ae76b3cf5f77146fc758557c39fba708fed34064a082f5d6d`  
		Last Modified: Fri, 14 Mar 2025 06:21:54 GMT  
		Size: 19.1 KB (19149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2bc5276e9670b19afc037ffe1887fa7155e5a04109cec380c4ec912d3e65de`  
		Last Modified: Fri, 14 Mar 2025 06:21:56 GMT  
		Size: 26.4 MB (26354702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cf1286cd23b6f30ba5e0b99f298188799ab44e4aa7e410ff64394990234a172`  
		Last Modified: Fri, 14 Mar 2025 06:21:55 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dca4dbe0d2e786739bf9cf10145c09982967fcb9ed646e3d83106d1bfb7bfa3`  
		Last Modified: Fri, 14 Mar 2025 06:21:55 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2` - unknown; unknown

```console
$ docker pull joomla@sha256:ad2efa07ddcaf32d189b5b740927c8db1f66dd97c3c87b894c0b4fab3884656b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 KB (61375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d81dd83568501cb17817896492c70bb18a3478880fe39cd9fb0a93484f6a84`

```dockerfile
```

-	Layers:
	-	`sha256:15ab7b3a443c96a21650119383f157da11401ddd37802a411f467ae6c3b90541`  
		Last Modified: Fri, 14 Mar 2025 06:21:52 GMT  
		Size: 61.4 KB (61375 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2` - linux; 386

```console
$ docker pull joomla@sha256:2b9396bcb69449af6e9ea7014314963950421ec099aa85e95cb9774ee2336f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.9 MB (258914675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cc3c53a7616b6e0a69a2e18f1151ee37734cccb1ca554f236bb0a2b74bb0e7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 19 Feb 2025 09:48:51 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Feb 2025 09:48:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_VERSION=8.2.28
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Feb 2025 09:48:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 19 Feb 2025 09:48:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
WORKDIR /var/www/html
# Wed, 19 Feb 2025 09:48:51 GMT
EXPOSE map[80/tcp:{}]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
# Wed, 19 Feb 2025 09:48:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
VOLUME [/var/www/html]
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_VERSION=4.4.11
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_SHA512=f72d4ed13388ad20c3a65542262414867a05e67360cd771d0526e09b907bb44f3ae08b9eeb2a0b98316b787352dce6a47452f8c4fbac970666908e5357d0e43d
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.11/Joomla_4.4.11-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de4ae9b4e633726ebe402026517c1ebaa63f96cc9c943c2c313846eee3894bf`  
		Last Modified: Mon, 17 Mar 2025 23:31:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2baf4c24a8f037eef9945e02415a12e6a6807cc13260e3d10e57a2fc0ecd30`  
		Last Modified: Mon, 17 Mar 2025 23:31:53 GMT  
		Size: 101.5 MB (101513248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a97d9453de48641c0771f5fd0491e255d4994cc829f78cef64c62d4d81de11`  
		Last Modified: Mon, 17 Mar 2025 23:31:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:748c9e89e2e6759c6e9c1b1dd65924bd1955fdf4d483738cb38fae06d83dbd26`  
		Last Modified: Mon, 17 Mar 2025 23:31:51 GMT  
		Size: 20.6 MB (20638457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd666fc2d3b75db5c4719d0dd622883db9de2405e27dc8305bdfa00199df20a`  
		Last Modified: Mon, 17 Mar 2025 23:31:50 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60eefd2aafb8b2c11b8ce1ebfb0b2ec72b9a7dbbdddd69cd96d27bbd10eb04c`  
		Last Modified: Mon, 17 Mar 2025 23:31:51 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c86a46bb7237989dfcb2ba43ec9c8994c83b0869fed0fa1ff0a0bb331117463`  
		Last Modified: Mon, 17 Mar 2025 23:31:52 GMT  
		Size: 12.3 MB (12275350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197b4b97b23b48959a8f0e609d0c1849de230e28617112007f9c3d114b40b42c`  
		Last Modified: Mon, 17 Mar 2025 23:31:52 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:117fff21041189786d2c20f799535022cc5698635d1791ced84f3b858ee15c17`  
		Last Modified: Mon, 17 Mar 2025 23:31:52 GMT  
		Size: 11.6 MB (11649558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6784e28cca219d4c80bd9c064d3010a34c49f3eaf17881e1e75439fec204b0`  
		Last Modified: Mon, 17 Mar 2025 23:31:52 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f501c7a36787e6448ae02da9419dac1d690f1f624cc474f6d52f7d7d315f8e45`  
		Last Modified: Mon, 17 Mar 2025 23:31:53 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3642e7e36795815bd132a66a6719808fe841c5f6a1135cd8a0f107cce063fb`  
		Last Modified: Mon, 17 Mar 2025 23:31:53 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e324ee74efa0c01b079270ee11180d84dbc3823414169367ab224dd4dcedd8`  
		Last Modified: Tue, 18 Mar 2025 00:20:39 GMT  
		Size: 26.7 MB (26700507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35360af2bde470edd96992ae5430fe04d4a3f493da63599e8ce992ec3efa2e9d`  
		Last Modified: Tue, 18 Mar 2025 00:20:40 GMT  
		Size: 30.6 MB (30563243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7413122d7cc0044a21d6a3e2aef068605f642b9689f7e23ae8832de016293017`  
		Last Modified: Tue, 18 Mar 2025 00:20:38 GMT  
		Size: 356.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fdaee79c6949cbfeebb409a885030e909d66e9f20e0f9ad9517ed056b320f9`  
		Last Modified: Tue, 18 Mar 2025 00:20:38 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:584fd0bdcace21bfd9228e532f636a0997b9b2f3672d0b43db2b60816c559723`  
		Last Modified: Tue, 18 Mar 2025 00:20:39 GMT  
		Size: 19.2 KB (19158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cdb5fa92fdd82ff9e43c86278f50e1e86f19ef8a6b753ef4379142477170f5`  
		Last Modified: Tue, 18 Mar 2025 00:20:40 GMT  
		Size: 26.4 MB (26354696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90eacd017ee80b4964f576184f03870ae8383a7bb0cd1f90bedb8d555832908d`  
		Last Modified: Tue, 18 Mar 2025 00:20:40 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39947a92cd1fb51a5f8925e2f76686a1a28805416e8e42b57af09ef451348085`  
		Last Modified: Tue, 18 Mar 2025 00:20:40 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2` - unknown; unknown

```console
$ docker pull joomla@sha256:1a65856eeba1d8b4359945d292c09a3905f05234b42e16936ae7e8a8248d4bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 KB (61027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b26f2a074f68fd53fa84d133e182000272d316f359b1e9ba99149634c16ab7c5`

```dockerfile
```

-	Layers:
	-	`sha256:cb6db2094fa46b8160135ea6060f59b6d781ca8b4017fdb555fa003d8baae5b6`  
		Last Modified: Tue, 18 Mar 2025 00:20:37 GMT  
		Size: 61.0 KB (61027 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2` - linux; mips64le

```console
$ docker pull joomla@sha256:6c27d978cdfb05a007b2d8f71d817aa44663790e6b79c2db8b9541ccd5e41bcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (232995763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b67e57f6c5c8f4fc941b3abb9479b6e2c8964d0279b2e6c287dfb6db3c0f69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 19 Feb 2025 09:48:51 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Feb 2025 09:48:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_VERSION=8.2.28
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Feb 2025 09:48:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 19 Feb 2025 09:48:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
WORKDIR /var/www/html
# Wed, 19 Feb 2025 09:48:51 GMT
EXPOSE map[80/tcp:{}]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
# Wed, 19 Feb 2025 09:48:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
VOLUME [/var/www/html]
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_VERSION=4.4.11
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_SHA512=f72d4ed13388ad20c3a65542262414867a05e67360cd771d0526e09b907bb44f3ae08b9eeb2a0b98316b787352dce6a47452f8c4fbac970666908e5357d0e43d
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.11/Joomla_4.4.11-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d36a7b1e0c4904256c3222f554e2f9053a6ce6cb06dac686a36004c2968943`  
		Last Modified: Tue, 25 Feb 2025 04:23:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878fe44e60469208a4e6a6cc56a06ba4bd6418ae0d09468c66a29bce7fc35e03`  
		Last Modified: Tue, 25 Feb 2025 04:23:25 GMT  
		Size: 80.7 MB (80668722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03653780888887368ef36859920d833d269d38c1e54ffb86bae392b6bfcfde65`  
		Last Modified: Tue, 25 Feb 2025 04:23:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d16225b42033fad2e17de37197d7ddf58740cc1e834d88386251e1203d6bc`  
		Last Modified: Tue, 25 Feb 2025 04:43:12 GMT  
		Size: 20.1 MB (20069161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0240d2561c08c1860eeebaa66951069a40fc7b7c112653504c26fe56fc8e30`  
		Last Modified: Tue, 25 Feb 2025 04:43:09 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f085555607131ca41617fae1213ab0cb04ab6a67ce34f84c32f46a658c22f736`  
		Last Modified: Tue, 25 Feb 2025 04:43:09 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7fda57db4a7596c454b37ed5539916d47b53aeb7a82bd7d4a789f17503fc1c`  
		Last Modified: Fri, 14 Mar 2025 03:02:50 GMT  
		Size: 12.3 MB (12274112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cae38a1d0b5afe7be71c3ccfd6f788347c9bcf7c42259f5c7ee452b4e2d61f`  
		Last Modified: Fri, 14 Mar 2025 03:02:48 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2209d08119f471a5f5b059306cd93fda84f84661773ed5f9389e73fa276907d1`  
		Last Modified: Fri, 14 Mar 2025 03:02:50 GMT  
		Size: 10.5 MB (10501035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c445d4f9a89d85c1447aa33161ee8ae8dceec8efce79ec21ffad2e6e103b1586`  
		Last Modified: Fri, 14 Mar 2025 03:02:48 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f531e7ee93f4522c50fd01e97fc8300f24d4c928a72aed6f26cdc13a3a8626b4`  
		Last Modified: Fri, 14 Mar 2025 03:02:49 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f05638e1c1b96ddda63d0c6406d889deac49c985c42e51d22a9c1bf2f77b7f`  
		Last Modified: Fri, 14 Mar 2025 03:02:49 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d949a4549f0ce3b64b046f8efa7ccf4a918de80556572cc63742a2e88374757`  
		Last Modified: Fri, 14 Mar 2025 18:18:26 GMT  
		Size: 26.0 MB (26022238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc718fb65c827d9278061a9f7542c4db0bd4a8c7aac445fdb66c2a5c2df4af7c`  
		Last Modified: Fri, 14 Mar 2025 18:18:26 GMT  
		Size: 28.6 MB (28581954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fea0f9bdc045da392553cd8404013c8b93a6cabccd404769a99220d35724476`  
		Last Modified: Fri, 14 Mar 2025 18:18:23 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caeb6aced0d3e8337ae1316d4e9bc5bcc602ad41b9bc08d1e87be5f408ca7369`  
		Last Modified: Fri, 14 Mar 2025 18:18:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31b5480ce09226cfdfcb07c4442b9a084325af1dff5843be2157226e28671e6`  
		Last Modified: Fri, 14 Mar 2025 18:18:24 GMT  
		Size: 19.2 KB (19168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2578045a4058d56faa4788b602752b82a54b8e16bebc0bcbaa8300f87d2f72b8`  
		Last Modified: Fri, 14 Mar 2025 18:18:27 GMT  
		Size: 26.4 MB (26354701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2444c8c9ee137f704c87547e633e9ebcec7fe62b74f8c8f0f7c40e34700fd5ab`  
		Last Modified: Fri, 14 Mar 2025 18:18:25 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4756d1e64c151d0f8aaef09967d44b95f064f3a9b7b2f814e4b479c02d7f9c5f`  
		Last Modified: Fri, 14 Mar 2025 18:18:26 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2` - unknown; unknown

```console
$ docker pull joomla@sha256:7accea1e77f2479301c8691a3317dd91ce3aea108c553e6bdc3458da161bf85e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 KB (61253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e336f502b99c17a4dd3ea65d9774995c5f4a1745846457ddfe4b6c76e341bf`

```dockerfile
```

-	Layers:
	-	`sha256:99c73d27e5040dbbf411bb0f14e3036f55a7cea6cfd6b56e078fb179dc2eb22f`  
		Last Modified: Fri, 14 Mar 2025 18:18:23 GMT  
		Size: 61.3 KB (61253 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2` - linux; ppc64le

```console
$ docker pull joomla@sha256:4f3b7e4b3ac6f50ed4ef9c36830b13259464ed1a0a9d068cbc3a23613b00cf5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265908526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d4eb624925a995f2ca73464d4f1cbfa6239ecd39eb885249fdcafd74cd5128`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 19 Feb 2025 09:48:51 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Feb 2025 09:48:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_VERSION=8.2.28
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Feb 2025 09:48:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 19 Feb 2025 09:48:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
WORKDIR /var/www/html
# Wed, 19 Feb 2025 09:48:51 GMT
EXPOSE map[80/tcp:{}]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
# Wed, 19 Feb 2025 09:48:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
VOLUME [/var/www/html]
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_VERSION=4.4.11
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_SHA512=f72d4ed13388ad20c3a65542262414867a05e67360cd771d0526e09b907bb44f3ae08b9eeb2a0b98316b787352dce6a47452f8c4fbac970666908e5357d0e43d
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.11/Joomla_4.4.11-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bbbae4d2dc0350f7df1634e33daf64fe78cb672182650c700a26750b33b64c`  
		Last Modified: Tue, 25 Feb 2025 02:59:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f7bed916e76b3a3b176b4e6a5bcfe6e10e39a6c423be8fc3575115d7b1e06`  
		Last Modified: Tue, 25 Feb 2025 02:59:28 GMT  
		Size: 103.3 MB (103323545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9943a0d5cef1bf22e1a6d5df4b38af8052474c28fe7d9188d33c9e0190742`  
		Last Modified: Tue, 25 Feb 2025 02:59:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5eba5668f315d2ef7f70338fc89daecbca191bf9b5b6622280439ff5ceb4a7`  
		Last Modified: Tue, 25 Feb 2025 03:04:11 GMT  
		Size: 21.3 MB (21308442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bec4fde36a5fc026717bc0e1c4a8f85c6397c11d730b4d345fdb0b5014cc45`  
		Last Modified: Tue, 25 Feb 2025 03:04:06 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca66cb544073b521bd3bcd518135c4cf977a5939323c5191473a1b8a2a09cd05`  
		Last Modified: Tue, 25 Feb 2025 03:04:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4250556fa8417334da5be4ff65e43885cb11a4aefa7d255ddcedadfb60e1e4b`  
		Last Modified: Fri, 14 Mar 2025 01:15:16 GMT  
		Size: 12.3 MB (12275866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc1dc2ea55f95178ec13fe2b851029d78f5e0d2f3a6c8390fe1a234a9f2e9cf`  
		Last Modified: Fri, 14 Mar 2025 01:15:16 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afa4c68853b68dabf1bd8e64549df9d94bcf4c95ef043f559e0eefabff7ff8f`  
		Last Modified: Fri, 14 Mar 2025 01:15:16 GMT  
		Size: 11.8 MB (11834942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a58ec0c7a28b79ecb2761aea3a7ba1c7e11a569cdefcbc08ed0bf5bc5fb74af`  
		Last Modified: Fri, 14 Mar 2025 01:15:16 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4920622eb8cb7077f99589eb65bebd3e0264d1474c6bc0a48e5c79e7629376`  
		Last Modified: Fri, 14 Mar 2025 01:15:17 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8370a02df23f733617d749f69df800919185839d44c681f4c9ec95e9b5531d10`  
		Last Modified: Fri, 14 Mar 2025 01:15:17 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82d353214552289fc5c79f56ebc1cd6d5de997d26aca15bc6487fd40bc875c4`  
		Last Modified: Fri, 14 Mar 2025 05:26:20 GMT  
		Size: 27.3 MB (27339037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1bf67b0855f470bc5ce838e8da7dfb50aad158de966539192c65122d9849354`  
		Last Modified: Fri, 14 Mar 2025 05:26:20 GMT  
		Size: 31.4 MB (31389597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218dd5fbec32e078492222e1d61d507efd9047956c7c79f85a1b056de56228a9`  
		Last Modified: Fri, 14 Mar 2025 05:26:18 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3675c46503e66a8340c5317e048910ce543ded70d74c315482dda4e47b3ce64`  
		Last Modified: Fri, 14 Mar 2025 05:26:18 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a12382724d8532b7fdbc9791c811b32f7fa20c4e20bdaaf6dd08caa9890df94`  
		Last Modified: Fri, 14 Mar 2025 05:26:19 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2307017960b4ff4a2c861c576074a277909f18e9c477ab6037bde9a4771f19`  
		Last Modified: Fri, 14 Mar 2025 05:26:21 GMT  
		Size: 26.4 MB (26354653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d6e18786c07ec7b4ef45ca707e168beb03c7e622eff03b5cba2fe797c709f0`  
		Last Modified: Fri, 14 Mar 2025 05:26:20 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7285f0b79f8ba92b15fd9217e9b78527a9a4cf08127fbdd82d0be0d913d126c6`  
		Last Modified: Fri, 14 Mar 2025 05:26:21 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2` - unknown; unknown

```console
$ docker pull joomla@sha256:0fa750a8b729f45eacc47d83e91ed2894a31c82f385d88f1e69151856ba7d272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 KB (61211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0d9966cb78b64844b7bf56517d1224ce4094d466d93a8391299c4db2f64357`

```dockerfile
```

-	Layers:
	-	`sha256:156ce36df0328b9ea2c91c89476e56dee371ccf7be7a78f7fd1e7f8b94c75e14`  
		Last Modified: Fri, 14 Mar 2025 05:26:18 GMT  
		Size: 61.2 KB (61211 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2` - linux; s390x

```console
$ docker pull joomla@sha256:8bc9a3abafa2cb30840eb3e28d14fa761589dde506b7b28faa931a51a445d6ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230757766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:198ada25719f0d434e93e6a7140dba8e219303fcd022c84b17a308850b830bcd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Wed, 19 Feb 2025 09:48:51 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Wed, 19 Feb 2025 09:48:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 19 Feb 2025 09:48:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_VERSION=8.2.28
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 19 Feb 2025 09:48:51 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 19 Feb 2025 09:48:51 GMT
STOPSIGNAL SIGWINCH
# Wed, 19 Feb 2025 09:48:51 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
WORKDIR /var/www/html
# Wed, 19 Feb 2025 09:48:51 GMT
EXPOSE map[80/tcp:{}]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
# Wed, 19 Feb 2025 09:48:51 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
VOLUME [/var/www/html]
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_VERSION=4.4.11
# Wed, 19 Feb 2025 09:48:51 GMT
ENV JOOMLA_SHA512=f72d4ed13388ad20c3a65542262414867a05e67360cd771d0526e09b907bb44f3ae08b9eeb2a0b98316b787352dce6a47452f8c4fbac970666908e5357d0e43d
# Wed, 19 Feb 2025 09:48:51 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.11/Joomla_4.4.11-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 19 Feb 2025 09:48:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 19 Feb 2025 09:48:51 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f83dfaf87e0f897b620f8faafcd35d93785d305460fb8a1f24f178152dc8ef4`  
		Last Modified: Tue, 25 Feb 2025 02:47:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382c1a79d42d9a6f73ff6106cec8445a8fb8bc6a78380c02024ff5e71c740938`  
		Last Modified: Tue, 25 Feb 2025 02:47:06 GMT  
		Size: 80.8 MB (80817122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd5ce3ea58656e03c29355d087376523130702c7a182e93a6e6c775d2e795dd`  
		Last Modified: Tue, 25 Feb 2025 02:47:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ca9e9fc0029c44454cc7b3021d275f272be12d935e5bcbf513a001e160df1e`  
		Last Modified: Tue, 25 Feb 2025 02:50:57 GMT  
		Size: 19.9 MB (19895168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312727822926b01c3ea7b38ae79e9f14f546dab08bbfd780821249610ae4aa7e`  
		Last Modified: Tue, 25 Feb 2025 02:50:56 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d51730a67b490b800306ddce51f95b7fc9ec61621c6c0c350bd502364beda8`  
		Last Modified: Tue, 25 Feb 2025 02:50:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608f3449f17fac836f00e95c11cf6677e5c8dead7862c295c002347ee3166642`  
		Last Modified: Fri, 14 Mar 2025 03:10:30 GMT  
		Size: 12.3 MB (12274733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc109b8aa64531118deeee4d53dc37e783f34fedcbc8dad91d851af657e7cd4`  
		Last Modified: Fri, 14 Mar 2025 03:10:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bdefc7fc3e1fc66be0d03e2d1d4e957369faba12d4fd56e864181079422cce3`  
		Last Modified: Fri, 14 Mar 2025 03:10:31 GMT  
		Size: 10.7 MB (10652670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c13436f750f3be8b240a5f21fe804cd624fc063b6c9e97d24e93bc1b34eede7`  
		Last Modified: Fri, 14 Mar 2025 03:10:29 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4213e4bab64c562d812fa4f5cecb963fb14605db6da9b4da5f96e9695802b664`  
		Last Modified: Fri, 14 Mar 2025 03:10:30 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382b3ccafdb9b1cc929f92a2a173358c27c9d5d6952b1a3133104e8ca6354e8d`  
		Last Modified: Fri, 14 Mar 2025 03:10:30 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43ceaf406daf1cdd6e98a8d59fb8c79b0b489f67576085589ae68b024ade299`  
		Last Modified: Fri, 14 Mar 2025 13:40:26 GMT  
		Size: 25.9 MB (25899170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5df1626352a5841227f2e6e9581a7f736cedb4d511c8790b1d2a8d712109c8`  
		Last Modified: Fri, 14 Mar 2025 13:40:26 GMT  
		Size: 28.0 MB (27969239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb8c0f590401c984a9d521b3397047cd9dea912f70c1ff8833edcfbbfc33326`  
		Last Modified: Fri, 14 Mar 2025 13:40:25 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feea7d57f7adfa75ac1c1f574018981221a43ae3046aa30018f12c0e219239f`  
		Last Modified: Fri, 14 Mar 2025 13:40:25 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a0ed6fdbf23ab2e338cdffeea6d9e9109da8a484d4a4d86415c0f99f65b1424`  
		Last Modified: Fri, 14 Mar 2025 13:40:26 GMT  
		Size: 19.2 KB (19156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a8199745937b0196f2a0fbd10a1063ce320dd9571afe783da9bc882fbb9194`  
		Last Modified: Fri, 14 Mar 2025 13:40:27 GMT  
		Size: 26.4 MB (26354701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005997c98dad6f7439e3c84497db8fa1daa0b2400067727e7ce1916f221d12f1`  
		Last Modified: Fri, 14 Mar 2025 13:40:27 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7780c91e340da92fd34539df59c5582f46be98b1a5ef97a7ba7c4e85740978b3`  
		Last Modified: Fri, 14 Mar 2025 13:40:27 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2` - unknown; unknown

```console
$ docker pull joomla@sha256:2b49b8d9bba5099f5ab3d1c96aba6433dfd132899812f46e19834b5d7c931192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.1 KB (61100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35440200a1b6380154fd7030da399f714aaac7e92cee1cfb518eefdf54ce0be7`

```dockerfile
```

-	Layers:
	-	`sha256:5ec984a59a809e1cf9da3eb4663135eeac60f03561bb0d9dab498f3c1b98a426`  
		Last Modified: Fri, 14 Mar 2025 13:40:25 GMT  
		Size: 61.1 KB (61100 bytes)  
		MIME: application/vnd.in-toto+json
