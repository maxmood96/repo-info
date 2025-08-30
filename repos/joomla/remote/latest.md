## `joomla:latest`

```console
$ docker pull joomla@sha256:7a51d753e42042ea227437c7a0f0a0a6ed05e63e07a91d44f9098359063898a1
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

### `joomla:latest` - linux; amd64

```console
$ docker pull joomla@sha256:b2193a63cb11855b1ecdd77d680d87f9282084929ea84e928ca9e2c7576060fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273907878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69624593a75f1083e7ce9b24e96fce328c7c9e75ee9b7ffe3350c7a8e12d1539`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 22:37:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_VERSION=8.3.25
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 22:37:33 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 22:37:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 22:37:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3943170be4857750e6e5e7e6acf05d57165d9dc5ef028f9aaa455cc91ec8a90`  
		Last Modified: Thu, 28 Aug 2025 18:19:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5315d6b3b12232520bd1bdc571d6dd946f31e52b9efe493a061ba98c638683e4`  
		Last Modified: Thu, 28 Aug 2025 18:19:19 GMT  
		Size: 117.8 MB (117833773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe9c170c7bcd064b869e0672c845256fea4ef18f73b9ec4f61d94bf1d2328fd`  
		Last Modified: Thu, 28 Aug 2025 18:19:04 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc20c6d0eaf0160abe8ac69f38b7b8059699bf61dc0377bb9cb358c81605f3b7`  
		Last Modified: Thu, 28 Aug 2025 18:19:04 GMT  
		Size: 4.2 MB (4223770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c45bb011d27a45f216a8c5c6f1f35f9ae8b4f51347820c74234892dacd69ee`  
		Last Modified: Thu, 28 Aug 2025 18:19:04 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186e3083bc1cda5d78f949ec6f2caaee7c83231e6acda1bc41c2bbadeac6daeb`  
		Last Modified: Thu, 28 Aug 2025 18:19:04 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46e6dbd96a3ef42fcaebcdd25a64b2a540efb2f363de761c1c42d5d3552b9e9`  
		Last Modified: Thu, 28 Aug 2025 18:19:06 GMT  
		Size: 12.8 MB (12750074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc578c8740d2d943d50722491217212a526fb0bf073899bf5de272f16f0b0ad`  
		Last Modified: Thu, 28 Aug 2025 18:19:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897e2f25eeb94623085a014bd6498bac48dba995f78bbac9ba63a1f06df70319`  
		Last Modified: Thu, 28 Aug 2025 18:19:05 GMT  
		Size: 11.7 MB (11705468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa14450030188c6b588c507cc335df4a38ea2b015fe7b0aff94ee545a94fbc7`  
		Last Modified: Thu, 28 Aug 2025 18:19:04 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b55ea1cc72eb468070317441dbf53761b0c426602615baf5eb235bd1a33916`  
		Last Modified: Thu, 28 Aug 2025 18:19:05 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64ee67ce7baab9c2194f2d2a47fd74f27a8a66f8abbd2682d8264095f695b90`  
		Last Modified: Thu, 28 Aug 2025 18:19:05 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2080e4bcc9abf40f82350e4776478d36efbe184332ad611f352f69e67a8c4b4d`  
		Last Modified: Thu, 28 Aug 2025 18:19:05 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc791af5c6435bbb6c003c2671eb45278abc807d4bb6a90ad0938b6027ac702f`  
		Last Modified: Thu, 28 Aug 2025 18:58:53 GMT  
		Size: 27.3 MB (27271169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a4413b5fe2bcdeb8070bad79b1fd5c15f1dbe06df24734ef17324bf6453309`  
		Last Modified: Thu, 28 Aug 2025 18:58:56 GMT  
		Size: 45.2 MB (45202357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13dad0926aed0671fb84a440516189d09674cc7c63012ee4bc1cbafb13bd3715`  
		Last Modified: Thu, 28 Aug 2025 18:58:51 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49ae8fbac49365742a8cede137cd713e3ebcb22d7acde3a8aef38926c4d40a7`  
		Last Modified: Thu, 28 Aug 2025 18:58:51 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d92354e5c1e26eb13ec78f292a0362558dc12f04a4406eace07508635fdb8e`  
		Last Modified: Thu, 28 Aug 2025 18:58:51 GMT  
		Size: 18.8 KB (18796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e515af94138f3d1fc08de04b3201d7d9c1409f1cc4def97802ce7990913163`  
		Last Modified: Thu, 28 Aug 2025 18:58:53 GMT  
		Size: 25.1 MB (25118036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5890a2385b91beb2590e62e3ce785b6d7a93342575c624919b427dd8eec09e35`  
		Last Modified: Thu, 28 Aug 2025 18:58:52 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751c52894fb9cff562167c4c0bdf82cc2364125b2d1e967c8346c5ff1b267477`  
		Last Modified: Thu, 28 Aug 2025 18:58:52 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:latest` - unknown; unknown

```console
$ docker pull joomla@sha256:ca75808f578ca9984e8f67f9d05d526a31fbc656aa6648db691fe82151bb9727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 KB (61434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eee8bfdc558f06443c4c2bcd341eedb09e8104cf996f8ab95a9370351d222e4`

```dockerfile
```

-	Layers:
	-	`sha256:68f44f2154df855059921ab7037939181a468b7a77a7fa4a9bba229ff5eca391`  
		Last Modified: Thu, 28 Aug 2025 19:43:29 GMT  
		Size: 61.4 KB (61434 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:latest` - linux; arm variant v5

```console
$ docker pull joomla@sha256:41c292a92af6c0694d256d3ba591f383e94746479726b715cdafbf7fd48aa0d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.0 MB (244986259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3192e6af56dd8b316d298a7fd79e11783947ffe38bb76f3366d5f4b32bd9d30a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 22:37:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_VERSION=8.3.25
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 22:37:33 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 22:37:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 22:37:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b826fc1a1d535eacc028e3d956ad4684d2277457bc010244dfb267e133817510`  
		Last Modified: Wed, 13 Aug 2025 02:04:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5554cad66c2c0be3db0dee9e2828bb1216178113d28498a470e272f7c87a2e`  
		Last Modified: Wed, 13 Aug 2025 04:31:51 GMT  
		Size: 94.9 MB (94871877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bad6001493531fd836717f5de4d6b19cb18c7fe4e2c9d0cbbcb80e66609bd4b`  
		Last Modified: Wed, 13 Aug 2025 02:04:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b50afdc142e6451ef7d9c32421123cfbe0fab27ee11ac3d01ad799f077fac415`  
		Last Modified: Wed, 13 Aug 2025 01:57:53 GMT  
		Size: 4.1 MB (4081709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17530c1a395b92b1493543369514c8f70e81f42721c7499a87f81b39f1f89d21`  
		Last Modified: Wed, 13 Aug 2025 01:57:52 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb201a9f7aa65c612ce8382e34904f44e078b655ce6f72b1852a84c50f00e8f`  
		Last Modified: Wed, 13 Aug 2025 01:57:53 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278470849436c624da61a1c505f1aa250ab0c4b6f78a7a5dee8ffce015b40b02`  
		Last Modified: Thu, 28 Aug 2025 20:24:52 GMT  
		Size: 12.8 MB (12760585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4c6a4900f6897b1a9547940c02fee77e87e538392cd6f9c93a941ce833587c`  
		Last Modified: Thu, 28 Aug 2025 19:30:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1bf5f26038d922297f28a21e947707dadd433701fbd5580c0fa0a6516c7bdbe`  
		Last Modified: Thu, 28 Aug 2025 20:25:13 GMT  
		Size: 10.6 MB (10588849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994331e7462dedfa5bc265217a0e7529bf10013f95904c6607dbb6bcccb5586b`  
		Last Modified: Thu, 28 Aug 2025 19:30:32 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7574dc15d322356a42a21ec1042b6065c0dc0fd024108f9f8e447e9dab19dc2`  
		Last Modified: Thu, 28 Aug 2025 19:30:36 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bc7c416096fbaf471f7df41742406efd943d4013650c6ab6be795e9bcc2291`  
		Last Modified: Thu, 28 Aug 2025 19:30:39 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d97c95d1f4e1596d6f7318d1e38595d71976c3b5c5ab6f8c8090b3fafecb597`  
		Last Modified: Thu, 28 Aug 2025 19:30:43 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c1f4fb631b1538c373f3c2d7c330300f7d5c8fd1974adf8050fec75e774ab7`  
		Last Modified: Thu, 28 Aug 2025 20:31:51 GMT  
		Size: 26.7 MB (26703369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9d5b19da8835e69e339f3d21ddeb96c33a025bc4c635d85689b09289dbc961`  
		Last Modified: Thu, 28 Aug 2025 20:31:52 GMT  
		Size: 42.9 MB (42890173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4c3d8f6c36ef450e199d594614bbd8cb131b00d0e8f843e70f7b5c73e3faab`  
		Last Modified: Thu, 28 Aug 2025 20:31:48 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a0bd97e7043a4c7b8a2e1b125acbd2126f468cd65af9fd0a113bbfd6a86edb`  
		Last Modified: Thu, 28 Aug 2025 20:31:48 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35ddfd80b817de9121fddd19cb75a143d2c36ff86324bf55e381822128e6711`  
		Last Modified: Thu, 28 Aug 2025 20:31:48 GMT  
		Size: 18.8 KB (18800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58fed012276f313d9847877279125269abf64e7ea50dc3def232c400d4afdaf2`  
		Last Modified: Thu, 28 Aug 2025 20:37:14 GMT  
		Size: 25.1 MB (25118023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4653ec5c95180a100154e1e1e7af1a80ee92c1359a81c30fb338c15f5bc014`  
		Last Modified: Tue, 19 Aug 2025 23:29:10 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e090957170b9146c20fd3c793e063dbf2ed32175e79c66cc9601065852ef5d6`  
		Last Modified: Tue, 19 Aug 2025 23:29:10 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:latest` - unknown; unknown

```console
$ docker pull joomla@sha256:4fb7003fa3b5b6158692e327e4824c8f213d4d125b1ce9b7f3a0742f50c26381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 KB (61662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:634392becf0a79b73016f02ab91ae38fbf96b133a53c0fb8e9615dba31f4efef`

```dockerfile
```

-	Layers:
	-	`sha256:2c4be672607442395fcd3c4e8b2b496e98037beced820f3d6bde9aba3348df1f`  
		Last Modified: Thu, 28 Aug 2025 22:43:43 GMT  
		Size: 61.7 KB (61662 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:latest` - linux; arm variant v7

```console
$ docker pull joomla@sha256:c1c0e51a311ab86bb6752dcaa662d75dad442bf322aa4a8d44a0458d1e7cf133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.4 MB (231374858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc9e4aabdc9ba999a51e7e4d4ad7213ce10a55be3d18d4909788a0e13ce22e3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 22:37:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_VERSION=8.3.25
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 22:37:33 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 22:37:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 22:37:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f783066fe233d49b725a424d9e4e2edf03ec368e8008a7100235b31d55c72428`  
		Last Modified: Wed, 13 Aug 2025 03:03:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def7928390388cc2020246549215f695478752f6ae67568af1344eee2f6088ce`  
		Last Modified: Wed, 13 Aug 2025 03:03:28 GMT  
		Size: 86.2 MB (86243176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5decd14e90655d8988225e174f3bef3fbd8abee342388203104f64e9516432f7`  
		Last Modified: Wed, 13 Aug 2025 03:03:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372110111ee86e66c1b99c7148a9a3a4e350c9b9c4843f501f3c831128011fe3`  
		Last Modified: Wed, 13 Aug 2025 03:08:13 GMT  
		Size: 3.8 MB (3751774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721b3bcfb16aff30d3a16d797f1847f5686541c5e5390e6d2d1d8e947baa2f68`  
		Last Modified: Wed, 13 Aug 2025 03:08:11 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fb1db8d532ffaa5e1f6b0f06e0e76396d505ed544ca2b1636fa7de235e998e`  
		Last Modified: Wed, 13 Aug 2025 03:08:11 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ccf0d4d6b9ac0ccd7aa813e905423d4a4839430b6c1400db4cd27029af0efc`  
		Last Modified: Thu, 28 Aug 2025 19:39:39 GMT  
		Size: 12.8 MB (12760652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb98e22e610e7b4dc8b07afe20e1f77abb01088bd465803b4b5196ebd8bece2`  
		Last Modified: Thu, 28 Aug 2025 19:39:38 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9f1b0a345b9629462353ed6f9acf424237ef83945ace275d3fbb45cada111e`  
		Last Modified: Thu, 28 Aug 2025 19:39:42 GMT  
		Size: 10.1 MB (10061886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244f82398afe50470390de4812d35eeea83e352a3dec199c0b3f2bc8f749cd60`  
		Last Modified: Thu, 28 Aug 2025 19:39:38 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e6e47ff547d1872284c9b630691f392c4478ac58c732ed2b7052e7beb950c`  
		Last Modified: Thu, 28 Aug 2025 19:39:38 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf8bd6668f48840bcde147c71a744b23eb5b0a8975044985a9681b4144b23b9`  
		Last Modified: Thu, 28 Aug 2025 19:39:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:138247504b55d701d061e956141d510bb1dcf47361dc841a062ef74af099901e`  
		Last Modified: Thu, 28 Aug 2025 19:39:38 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53b25653e7996f184be5de753db42ca68de8d05f7ae9bd1d0ebf7954c7e0c62`  
		Last Modified: Thu, 28 Aug 2025 21:01:51 GMT  
		Size: 25.9 MB (25925091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04d4de92b3271fc5894b75f63cee140c5316b52fd3a76c84d1cb6838d3306118`  
		Last Modified: Thu, 28 Aug 2025 21:01:53 GMT  
		Size: 41.3 MB (41276783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce56f5f993925bd5d9c7e3f1fa7fd4c059a119580fad2076656dac668b65e89e`  
		Last Modified: Thu, 28 Aug 2025 21:01:48 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cd18f56084a72d9bd25e92b9170cca328dcf4137fa75bf7c9cb39616b36aa0`  
		Last Modified: Thu, 28 Aug 2025 21:01:49 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5088408ce6393eb367303496bdb9bdca1503a780e604df2a93536f1b5b6b01c`  
		Last Modified: Thu, 28 Aug 2025 21:01:49 GMT  
		Size: 18.8 KB (18802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39a305c25250e06649c2e5445f4e5df7e9e3340dc164bbceb20cccc02b58a67`  
		Last Modified: Thu, 28 Aug 2025 21:07:35 GMT  
		Size: 25.1 MB (25118029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3f0241af5e9f9edffaa918008372b56dd474341637b85ce3d64a170b353c37`  
		Last Modified: Thu, 28 Aug 2025 21:07:33 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3cc75111fe0bfd855ab9599ccd89a7092d9bab67a7c171fcf3628857ecf7c0`  
		Last Modified: Thu, 28 Aug 2025 21:07:33 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:latest` - unknown; unknown

```console
$ docker pull joomla@sha256:fbb1a3d0fc196ed22b4819c8e5caf42075f741fda485b7680f51685cbacb3cdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 KB (61662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b8f01e52828d1783b2c3af700a529666818181bbe62e5bd6b0cbb11327c13d`

```dockerfile
```

-	Layers:
	-	`sha256:d40e03dda5d012de8986a6bed41aa4a6999c766c10233f70183a33dfc8e71e68`  
		Last Modified: Thu, 28 Aug 2025 22:43:46 GMT  
		Size: 61.7 KB (61662 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:latest` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:416863fcae1d8708676cd17880b3fe719bb8a2c10bec68acfc741fbeb2ebf659
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.4 MB (265449526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6005c79f7a0e49f32a83ef9fc78f650b733e32053870e594ff3368c1ea33c38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 22:37:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_VERSION=8.3.25
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 22:37:33 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 22:37:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 22:37:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ee6d029e615fa2b873890f1011a42f1c5f78b2d100eaed3bc1df5bb73d212`  
		Last Modified: Thu, 14 Aug 2025 22:21:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a472e922e809f2164e7de33f1a04d157980da1614d66407be60d248980ca8453`  
		Last Modified: Thu, 14 Aug 2025 22:21:38 GMT  
		Size: 110.2 MB (110160334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fe053e93cb40a6c44acd9d0ab0ee960880abe08bd106a21947710df1e0399e`  
		Last Modified: Thu, 14 Aug 2025 22:21:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc43ae40cfafdbc816c6ef33e29cb3a5b1fcd866e77ed316da93e7ac7be457bc`  
		Last Modified: Thu, 14 Aug 2025 22:29:04 GMT  
		Size: 4.3 MB (4301251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0c909ee690af4ad403bf2728df6cf54495afc197ec0612503debdb1a0d47a`  
		Last Modified: Thu, 14 Aug 2025 22:29:05 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5af3640212feddb52a07b6b7e3a5ba254dfe8302593969022dfcddb394f0e87`  
		Last Modified: Thu, 14 Aug 2025 22:29:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b665425619045050bd496d421bb389bb381189ce61fbcb90a9ed9b13c064eb3`  
		Last Modified: Thu, 28 Aug 2025 19:19:37 GMT  
		Size: 12.8 MB (12762710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e0198101926bb4f04c6632eff6855a5071dc515932213a0077cb2def736b51`  
		Last Modified: Thu, 28 Aug 2025 19:19:35 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf76d0197768bd65adb457cbb82cb4fb482866c80dff385a217573fc902f1ab`  
		Last Modified: Thu, 28 Aug 2025 19:19:36 GMT  
		Size: 11.7 MB (11727280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c032600758105559be9ff8daa39cd4c71aa3e63c6c414f5dddd732fee71e83`  
		Last Modified: Thu, 28 Aug 2025 19:19:35 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c293d67932722d7e0c09907e26d6191d6705f486163975a6b7bfec649d2568a3`  
		Last Modified: Thu, 28 Aug 2025 19:19:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf8da13eec602aa9ccdb87b3f45aa250d1f0b365527c81da6408c9af4c058cc`  
		Last Modified: Thu, 28 Aug 2025 19:19:35 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a91ab10aef2ff2ebae34198ea89776200382dd48b440db97e302b70fbb4822`  
		Last Modified: Thu, 28 Aug 2025 19:19:35 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00f9a6b0fcdbcc067ec8f67ecb9e6c07176d520603027e291cbb662baedcdd88`  
		Last Modified: Thu, 28 Aug 2025 22:04:16 GMT  
		Size: 27.1 MB (27097673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dff8bd4010e85caa55d5d10dff28fe8a70ca46fe456bd31c6c76b1b5a3a87eb`  
		Last Modified: Thu, 28 Aug 2025 22:04:19 GMT  
		Size: 44.1 MB (44116231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9df1992ab7069139cac71cb153cad62b2af6474ae3cfd661134a667ecb1aaf`  
		Last Modified: Thu, 28 Aug 2025 22:04:14 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5620f1d98c4ca38b35ba47752ea3ff6f64e6a178f9f0114edf4011749026897d`  
		Last Modified: Thu, 28 Aug 2025 22:04:14 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ace92d859f132a6a0d8f70ca798f814e30a56f0a1f7d283fa42c4381d0e9a5`  
		Last Modified: Thu, 28 Aug 2025 22:04:14 GMT  
		Size: 18.8 KB (18801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12245c0dd48c4e9e8300ac579d616971f5e04354fc55cfb83c4c1211dd7e3acf`  
		Last Modified: Thu, 28 Aug 2025 22:04:16 GMT  
		Size: 25.1 MB (25118035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bfa1d43a67b23266cbe2cbae11cc4608cb701575b612e2755ed85d63abc1b6`  
		Last Modified: Thu, 28 Aug 2025 22:04:14 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b467fd66dfa75a36d32d5efc4207dcd8edcd34e7a6815eed1650d58cdbcec555`  
		Last Modified: Thu, 28 Aug 2025 22:04:14 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:latest` - unknown; unknown

```console
$ docker pull joomla@sha256:88187c3d130d0fb4bb0e764003726376d284cf2d29992b4dad06851d6d31b738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 KB (61757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeff75aea54eea7de34fc829729acbd3af560af73cba105a9d87491672840277`

```dockerfile
```

-	Layers:
	-	`sha256:1cce6d5e057269f0b6d0e14748974277747df91921cefc9cd7a07497cac5844b`  
		Last Modified: Thu, 28 Aug 2025 22:43:50 GMT  
		Size: 61.8 KB (61757 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:latest` - linux; 386

```console
$ docker pull joomla@sha256:61e47a3d4835efc3cedd1f8caf56eccf833b897ae0db8cae23e5dadb92f2a061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.8 MB (274805413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b77e6be7d2851d8156ec5debb3f826fb71af69501efe00c57227dc7c0c023dc0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 22:37:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_VERSION=8.3.25
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 22:37:33 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 22:37:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 22:37:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:346d0c953bdbc38917a27a6f30726e5b46419d98ecaf4d2d8f201bc3b7025e57`  
		Last Modified: Tue, 12 Aug 2025 20:45:00 GMT  
		Size: 31.3 MB (31289378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ead0c54de1c198c145602397791a419cd680de6ce80ae93e96401c9716b2d`  
		Last Modified: Thu, 28 Aug 2025 18:18:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e602826baeb4e55bc8da76777fcda275cc51ee68524ebaa16e389219ac5d0b5`  
		Last Modified: Thu, 28 Aug 2025 18:20:06 GMT  
		Size: 116.1 MB (116135368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b52e68c4d3ccd7c00515e0708ce0f4dab97a9f5a9a15d06fd4e59c859e498`  
		Last Modified: Thu, 28 Aug 2025 18:19:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cba8a5b31ccfeb33820e1648ff43440d639bb44b53c7274303792d723bf6156`  
		Last Modified: Thu, 28 Aug 2025 18:19:51 GMT  
		Size: 4.5 MB (4455098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f9e1426c315f2158837a90060926b122c110ad681b321f364587c9bc1b247e`  
		Last Modified: Thu, 28 Aug 2025 18:19:51 GMT  
		Size: 425.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ccc880d325dd9c707c9f03c89524eab6fa9e2559a8e89ff6251e386d957f9e`  
		Last Modified: Thu, 28 Aug 2025 18:19:51 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1744e55433b0019bcb574f186f423f028f0e15267668da8e4b0fe3151a4211`  
		Last Modified: Thu, 28 Aug 2025 18:19:52 GMT  
		Size: 12.7 MB (12748704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd86d2a028b8b654a61946ae0fbdace2a15f1b6691420652096ffbcdbb58eeff`  
		Last Modified: Thu, 28 Aug 2025 18:19:51 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e39c4e9b3b0ae5cca5f7d7a2c2e7fbfe01194a3db99967fd1b3722871d6084`  
		Last Modified: Thu, 28 Aug 2025 18:19:52 GMT  
		Size: 11.9 MB (11915994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3da7ebb3d36a59026aec7ade3e96c1761e3567eec39a6548917fc6d42b3871d`  
		Last Modified: Thu, 28 Aug 2025 18:19:51 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847a993688b81e2a5c31e75a9cec6e6107d7701dee020c17df4176290780df43`  
		Last Modified: Thu, 28 Aug 2025 18:19:52 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff98d84b4c9ceda7057a2dff78118a1dc414a4197d880e47ea0c73f688b10591`  
		Last Modified: Thu, 28 Aug 2025 18:19:52 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4a39dee11f4ee1bb774220f1c8a5ab64876ea63241406b11cdec90cc3f7d7f`  
		Last Modified: Thu, 28 Aug 2025 18:19:52 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5960c6c021288f419e2dabc9d3a466e35f02acd09182c230f0c9241e1ab389e7`  
		Last Modified: Thu, 28 Aug 2025 18:58:55 GMT  
		Size: 27.7 MB (27712234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:194c65614d37c7c0396edca8abc22f0592ccfb5634c23ee8a8a4c4c87fcbfc8b`  
		Last Modified: Thu, 28 Aug 2025 18:59:03 GMT  
		Size: 45.4 MB (45400672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2978ce354e7d48fced0ca353327f7978f1f2ea46de9d3996310b53a673ace8e`  
		Last Modified: Thu, 28 Aug 2025 18:58:53 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbbd12f36371cc9d11ca294fded6cae7ce0a34deb173d79be4d02cd2af08230`  
		Last Modified: Thu, 28 Aug 2025 18:58:53 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1109d45c4a83e275357efa8c58a6c921fdb030d7c2fbb3e7a89b466de0471134`  
		Last Modified: Thu, 28 Aug 2025 18:58:54 GMT  
		Size: 18.8 KB (18791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1a044dd245f96a079a293976c9578c8c3022e807b04eb339922b9dba13ab97`  
		Last Modified: Thu, 28 Aug 2025 18:58:56 GMT  
		Size: 25.1 MB (25118030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd51930907ca3292901ab041d8f2ab5ba04ad0f608a9dcd61b0f4ff779d6563`  
		Last Modified: Thu, 28 Aug 2025 18:58:50 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41b8f045dd1350575efa9a225843d02e9d2acd3ee019f780f573fbbfab0e902`  
		Last Modified: Thu, 28 Aug 2025 18:58:50 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:latest` - unknown; unknown

```console
$ docker pull joomla@sha256:a18921217669a962d25b8d74df2dfcb2028496e89b7ac49448a7a74e03d0c7e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 KB (61331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a4d7fd6702a48ccc0e20b99525aaf4334bc745fea4f607cfe817c629704b83`

```dockerfile
```

-	Layers:
	-	`sha256:65681dfe5931b6a6f4af846dbb16854d6573b39b3441bf187edf4850adf92a2a`  
		Last Modified: Thu, 28 Aug 2025 19:43:39 GMT  
		Size: 61.3 KB (61331 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:latest` - linux; ppc64le

```console
$ docker pull joomla@sha256:b5af4907b3cf61f695ad8bf3f1c05639ff0d1c2d17b0c64f328366e9e9b4f3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.5 MB (273487003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a5419f94a46d2ed6e2d226085b6a06a5748dcd87119637d9ef4378e1bca0be1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 22:37:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_VERSION=8.3.25
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 22:37:33 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 22:37:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 22:37:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe95aaa1875d4c50c764ba29c6f95cc470f62d9ac88ad9109e0cd4505d319b5`  
		Last Modified: Wed, 13 Aug 2025 05:31:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0ffef807c2273a22858b85bf52a5cbb82101766a6dfce24ba2f8e3ca25f228`  
		Last Modified: Wed, 13 Aug 2025 08:03:15 GMT  
		Size: 109.6 MB (109595127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e8a64ac10b73fd871320ade0ad956a6b2aeb6e2c3151d32095cad855bbccb`  
		Last Modified: Wed, 13 Aug 2025 05:32:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd42c19a20ac483aec1baacbb7b775bf9031104d0a0f064b9f0867d3ccc76220`  
		Last Modified: Wed, 13 Aug 2025 05:31:06 GMT  
		Size: 4.9 MB (4875422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfcf6e5878ff7716cc38c54c9c5482a97442ddcdd8c0aabd868a7d11ed49b7e`  
		Last Modified: Wed, 13 Aug 2025 05:31:07 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983399591a61da466bb4e672cad02d507232883ed14732dd13f80ac851284879`  
		Last Modified: Wed, 13 Aug 2025 05:31:02 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a375a8fa977f9dd168e5c6a71cb066b51b3f13483cd6049005aa64e9d587cdb`  
		Last Modified: Thu, 28 Aug 2025 19:27:10 GMT  
		Size: 12.8 MB (12761974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44552ad427d380a7101a527c03f9b220697af4f2f9800706dbdecc1363515aac`  
		Last Modified: Thu, 28 Aug 2025 19:27:09 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3f5836944e61ffa759b9c5a75dffd16341b5775e142b9a316ee71068f50c70`  
		Last Modified: Thu, 28 Aug 2025 19:27:10 GMT  
		Size: 12.1 MB (12115466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cfc04f7d7c25be0a945551087bcd5ecf469db1174a2a67cbafd7d1f08f0002`  
		Last Modified: Thu, 28 Aug 2025 19:27:09 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e1964957ac917aca093e8a57a2f06756e88426d3e66461aeaa91651d15e903`  
		Last Modified: Thu, 28 Aug 2025 19:27:09 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53341fda939d52e6a3a6d196acb425d2e9d0bd62d738d7861dfb5a63a31992ab`  
		Last Modified: Thu, 28 Aug 2025 19:39:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f3b85dd846ec112e99be6bc653d5623b66e442c7a17be942028055eeabcf2e`  
		Last Modified: Thu, 28 Aug 2025 19:39:48 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df71a3c7dd9955c4f758656d3b55f571a1db6499566c208b7604280ff7ebeeb3`  
		Last Modified: Thu, 28 Aug 2025 22:33:33 GMT  
		Size: 28.4 MB (28416939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85bc47117e3021e437b2f46c3b6a0d86b10623bfc7e0f92c5fc2338227bb64b`  
		Last Modified: Thu, 28 Aug 2025 22:33:38 GMT  
		Size: 47.0 MB (46979842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61e7cc036d9a25720545669ac67fd6c11afee0f1390e03928ea00ee4881df78`  
		Last Modified: Thu, 28 Aug 2025 22:33:30 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5c6a318ffbcef2d269caadc4eb7950048adb1b217dce663e94b1eb1188dd72`  
		Last Modified: Thu, 28 Aug 2025 22:33:30 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48d7a69d57e083d243d56b9a964d0da2d2c612515d060c0342df1fc4fa98ba0`  
		Last Modified: Thu, 28 Aug 2025 22:33:30 GMT  
		Size: 18.8 KB (18795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f75bae3b61c85d40c01db2b48a180b935761a7aab46196b5066bb93583bb9ea`  
		Last Modified: Thu, 28 Aug 2025 22:33:32 GMT  
		Size: 25.1 MB (25118038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9445fa1566535655f5d9e47e497e89ddfc161e175c29c66056c14423aca4ae0`  
		Last Modified: Thu, 28 Aug 2025 22:33:30 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a7e5549bdbf2131e3762bbc85e3287d70782529162b5d47a7809817f76592d`  
		Last Modified: Thu, 28 Aug 2025 22:33:30 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:latest` - unknown; unknown

```console
$ docker pull joomla@sha256:d6df9be6e93a213eeb7f633c6c2b07e4872bd11e6bbed4b7fe1daa8f6ccd7d95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 KB (61560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da45faad3eb07d5bb4b4a967ea89771ba994cca861c480aa591e0451b59f69a`

```dockerfile
```

-	Layers:
	-	`sha256:69bcfb4d405c8c5eeb14be4ea6d51cf96b6af7ae4d7a0de2d07d7557cd24cd67`  
		Last Modified: Fri, 29 Aug 2025 01:43:30 GMT  
		Size: 61.6 KB (61560 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:latest` - linux; riscv64

```console
$ docker pull joomla@sha256:7db2ef6377484697811f2cf8049f8cdce08a8d15987246ad80e21d219e23d12a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.9 MB (308903739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bd779e541152e3d8bf142c7798d2dc6a89bffe9d9c1a331b5bfb8457ae0ad74`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 22:37:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_VERSION=8.3.25
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 22:37:33 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 22:37:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 22:37:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e74ecc2368ed7bf14f15784d294255a507b61c121584b8889b54497f586460`  
		Last Modified: Wed, 13 Aug 2025 11:14:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ba9332bf4f75d23eae5411f58fe1a55971f98de6873eba08746a8a1042d175`  
		Last Modified: Wed, 13 Aug 2025 11:43:11 GMT  
		Size: 146.6 MB (146577824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05acfa088a6e9eb3845fc5011b31ba6a62983f44944e2347f32361bf21d8f85`  
		Last Modified: Wed, 13 Aug 2025 11:14:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:437ee082f6fa69e7faad8700545098a6fe52d7039873614c52058e758703420b`  
		Last Modified: Wed, 13 Aug 2025 11:57:42 GMT  
		Size: 4.0 MB (4025653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5398f81f2b0b9d166065f2794959e13fe5cef571690a888e526a297344cb648`  
		Last Modified: Wed, 13 Aug 2025 11:57:42 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7320c702209633ef3bb6abda50aa7d4faab29f17f69247e387513e5af1004ed`  
		Last Modified: Wed, 13 Aug 2025 11:57:42 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6963a3b12e174db5e1bddc7417500adbede3f4d807b9e30405718d7d6b3564`  
		Last Modified: Fri, 29 Aug 2025 06:00:56 GMT  
		Size: 12.8 MB (12762171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40be50c4a4d1ac59b103e4415b902a9051af11fe7bb190638eab1fd706981453`  
		Last Modified: Fri, 29 Aug 2025 06:00:51 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1077c963062ef74a9ee8debe8860c4feec70fd2ab644278c999118d3bf0c2263`  
		Last Modified: Fri, 29 Aug 2025 06:00:52 GMT  
		Size: 11.2 MB (11249111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59186cc3a6c1a9337fe1df973c758c45ee79395c696f96deeebf70fc7f7b3ad4`  
		Last Modified: Fri, 29 Aug 2025 06:00:52 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0d853f6c4e3ad2b85a59a3c96ac506caa6b6f622ad3edff3775aca1ffb858f`  
		Last Modified: Fri, 29 Aug 2025 06:00:51 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3e52884e2f8bd1abe45ffa6acc1513c2071fa131fa88bfd6e9c148e878ced7`  
		Last Modified: Fri, 29 Aug 2025 06:00:51 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994af4e10d0f1e44a3d3ef1b92c0501c03e66f297ea4cf3b44512e6ed987a441`  
		Last Modified: Fri, 29 Aug 2025 06:00:52 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b876dafe16fe3fbf8d70a30f43c03520f21ff79c57165ce1e259db84e9814b51`  
		Last Modified: Sat, 30 Aug 2025 10:38:36 GMT  
		Size: 27.2 MB (27206448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd457f63ea40115b37e251d44f91e53d217e394c34f32a641017ce3d6a909166`  
		Last Modified: Sat, 30 Aug 2025 10:38:40 GMT  
		Size: 53.7 MB (53662824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068e2576c3b31e3e577221b47d2df4bf52461cb4b36ee88c6c04f026e0cae416`  
		Last Modified: Sat, 30 Aug 2025 10:38:37 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f736fae95a1f721bc6e451f2cfb07c8d3721e017c8629d6401146b455edb6fba`  
		Last Modified: Sat, 30 Aug 2025 10:38:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3481ba52b731bf3d826e4b00e7b262df91db4b81ad00526c712288fbb6d8cf`  
		Last Modified: Sat, 30 Aug 2025 10:38:36 GMT  
		Size: 18.8 KB (18819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef102602542f7d3eedd0fadbccea41a1447bf13eaa61ffe50e64e5a71ff2187`  
		Last Modified: Sat, 30 Aug 2025 11:51:39 GMT  
		Size: 25.1 MB (25118050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c65a536b1c9c8023d83f70ea31e4e1752ab220997a84d3a6ebcdaf3d0300f4`  
		Last Modified: Sat, 30 Aug 2025 11:51:36 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bbf03928efcd75d910c4b80425e95c660c6a61161cb936b873bf4cd81b12e5`  
		Last Modified: Sat, 30 Aug 2025 11:51:36 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:latest` - unknown; unknown

```console
$ docker pull joomla@sha256:752a857e1374a39696be3eb66ce49e9493403a4b5f3ccb2c2cba61f159aa2dce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 KB (61560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be866b9394ca39d9b41460f46f8febbcc1caf70fe674cfefff834942a37d52ac`

```dockerfile
```

-	Layers:
	-	`sha256:e1841187879ce0f0aed9165b8b6704d1a4a330771527ed519789ba6ce74651ea`  
		Last Modified: Sat, 30 Aug 2025 13:43:33 GMT  
		Size: 61.6 KB (61560 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:latest` - linux; s390x

```console
$ docker pull joomla@sha256:4774b40e9fba6be9455c5e8c6211b157d412e0c64f1166835c37b7159666b3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **248.5 MB (248467165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01670eae8efc9cbc87e6898b1e3a464e2dcfb092d9da1d86b4ad66ac616fb729`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 19 Aug 2025 22:37:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 22:37:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_VERSION=8.3.25
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Tue, 19 Aug 2025 22:37:33 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 22:37:33 GMT
STOPSIGNAL SIGWINCH
# Tue, 19 Aug 2025 22:37:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 22:37:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	a2enmod rewrite expires; 		a2enmod remoteip; 	{ 		echo 'RemoteIPHeader X-Forwarded-For'; 		echo 'RemoteIPInternalProxy 10.0.0.0/8'; 		echo 'RemoteIPInternalProxy 172.16.0.0/12'; 		echo 'RemoteIPInternalProxy 192.168.0.0/16'; 		echo 'RemoteIPInternalProxy 169.254.0.0/16'; 		echo 'RemoteIPInternalProxy 127.0.0.0/8'; 	} > /etc/apache2/conf-available/remoteip.conf; 	a2enconf remoteip; 	find /etc/apache2 -type f -name '*.conf' -exec sed -ri 's/([[:space:]]*LogFormat[[:space:]]+"[^"]*)%h([^"]*")/\1%a\2/g' '{}' + # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d672c8320b5c626e155e165336b2569c5c22cfbda44788e2e9dd0b175c8a1e`  
		Last Modified: Tue, 12 Aug 2025 23:44:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06790e9e58c7a87421168e1b912411e592f3adbcdce2412a5541e72fa8de3f1`  
		Last Modified: Tue, 12 Aug 2025 23:44:49 GMT  
		Size: 92.6 MB (92562072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019838dc72213baa0c7fefd5773b69a921a755553c45ef473aea40f478c95cb3`  
		Last Modified: Tue, 12 Aug 2025 23:44:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7420b950475ba12842aacb09ab6fc12c17aed6a94e8f7425f2d9023a527d61d9`  
		Last Modified: Tue, 12 Aug 2025 23:51:06 GMT  
		Size: 4.3 MB (4320335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2286236b154642f4dfec098836badaf56b6f5891dfe3de1dd729e687339006a8`  
		Last Modified: Tue, 12 Aug 2025 23:51:05 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d32f90a36507f204f3058a0f5e737aa20705dbfb0fceb4bbcaba30b59ab9c8`  
		Last Modified: Tue, 12 Aug 2025 23:51:05 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae59372dc49193e4b58948290794a2f556265214054685096719e40c00eebb64`  
		Last Modified: Thu, 28 Aug 2025 19:40:54 GMT  
		Size: 12.8 MB (12761466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232d1dbdb1cbb25df7d7aeed070bcd0e201f0933ed4213d6b76431436b89476c`  
		Last Modified: Thu, 28 Aug 2025 19:40:53 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a555ffa6a5bc9b92d92cdbb402d2c0e2b0f50426656edab743b4be9383ad4450`  
		Last Modified: Thu, 28 Aug 2025 19:40:55 GMT  
		Size: 11.6 MB (11560421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f956f604c21cab4bb539715f09151dd9dd270640e9d9fb344f4bad60f61ee5f`  
		Last Modified: Thu, 28 Aug 2025 19:40:54 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d780e1a0957c730a0ac4ed9f2e2e7c549dc42fc6ecf0585f74ad7aaec3bcb0`  
		Last Modified: Thu, 28 Aug 2025 19:40:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98f61a85c8e5b3657fd0475dbbf8d05d7ceadf7576d8b5fe719d69155bc1029`  
		Last Modified: Thu, 28 Aug 2025 19:40:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92c6c880f8d8d8050a5ac76e04997f5501d3085c1fb2ca3a81e69ada870d361`  
		Last Modified: Thu, 28 Aug 2025 19:40:54 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c17a2668a91fcec854df55153f7e302dc72972b56f04844b0cc9eee3d36e47dc`  
		Last Modified: Thu, 28 Aug 2025 21:48:14 GMT  
		Size: 27.6 MB (27551971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ef2361aa73bc4bf8f0c8a80dd798286998cad3429e2b9a3af9be98a5ff3dc5`  
		Last Modified: Thu, 28 Aug 2025 21:48:14 GMT  
		Size: 44.7 MB (44729826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f32c56b667156787267efae82a7df10f4015a67e350fc918b969fee727029094`  
		Last Modified: Thu, 28 Aug 2025 21:48:08 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:301d38865434b0a504559dac7359f2aef003632cf26daac5625d5156771c32da`  
		Last Modified: Thu, 28 Aug 2025 21:48:07 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8039f0b5718a9ab06969a38862dc59d6db97fbffd21d773ba914e61b154361d`  
		Last Modified: Thu, 28 Aug 2025 21:48:07 GMT  
		Size: 18.8 KB (18815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f94c012eede5be2dfd6def5a9d25a5bd003a13572a50536174354f64bbe42c`  
		Last Modified: Thu, 28 Aug 2025 21:48:12 GMT  
		Size: 25.1 MB (25118038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd22412c480c31ef1dec623c73ec8b66032389fe45949e967f5a1fbfed6e6ce`  
		Last Modified: Thu, 28 Aug 2025 21:48:07 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952fe09ca2e1452a413d5a6f87af57f07f79b20987e4f565f3493021ade95c27`  
		Last Modified: Thu, 28 Aug 2025 21:48:07 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:latest` - unknown; unknown

```console
$ docker pull joomla@sha256:27da30fcc1d96667d582770c8743773fae814dd259ba315c15e2bd2f5a227ee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 KB (61425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62db3b7560e78a8732030aeb5b60be325eae9874226aaa9293e9f361614decd6`

```dockerfile
```

-	Layers:
	-	`sha256:44dbca546f30e0df5fd537a294ac1d6fa86bd75a33a955f22499e2ad1001fe07`  
		Last Modified: Thu, 28 Aug 2025 22:43:59 GMT  
		Size: 61.4 KB (61425 bytes)  
		MIME: application/vnd.in-toto+json
