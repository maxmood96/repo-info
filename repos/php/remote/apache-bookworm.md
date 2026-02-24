## `php:apache-bookworm`

```console
$ docker pull php@sha256:5c97fc351a1ce6f471d73549f59bb77fe4108b9633b87b4028d7bab77f2a6aa0
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

### `php:apache-bookworm` - linux; amd64

```console
$ docker pull php@sha256:d46ceca31496b69d6d47be3db35652e758d7f95e83c71d7a89c35a004aa4ac59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182145697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4917ca87c6801c08e0ca28394d66faf87b2953de2fb798c66ae39e74c9756a04`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:05:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:05:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:05:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:05:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:05:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:05:44 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:05:44 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:05:50 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:05:50 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:05:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:05:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:05:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:05:50 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:05:50 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:05:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:05:50 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:05:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:05:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:08:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:08:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:08:36 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:08:36 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:36 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:08:36 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:08:36 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668fee85222fb59f90b61acb2f2707bb66144f65f8fbaf26e3af20b6bf16c074`  
		Last Modified: Tue, 24 Feb 2026 19:08:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e4f6395501a7226d4a4347b62ca9ded14373dec3f688d2d2962d9536c4cb98`  
		Last Modified: Tue, 24 Feb 2026 19:08:58 GMT  
		Size: 104.3 MB (104335908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86299eabc6f141cffd59d07dbf455ef70189df32328855c434336fa6b7552c2b`  
		Last Modified: Tue, 24 Feb 2026 19:08:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:168f3fe7ab1a23015919cd44e2ae72d684a93d926716983931f1942b19ffa630`  
		Last Modified: Tue, 24 Feb 2026 19:08:56 GMT  
		Size: 20.1 MB (20141473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb64425e17ed0230b21b65d570cd2ecbf946169e961bdea891f71eb7a65156dd`  
		Last Modified: Tue, 24 Feb 2026 19:08:56 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93565b0682eb7cf1f611a4df9e5b5115f2db5f590d433623ee7d180836af8c2`  
		Last Modified: Tue, 24 Feb 2026 19:08:56 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa6258456203da003bbf1dce293beca0d48c84bb524591be022a8c7d02a77f4`  
		Last Modified: Tue, 24 Feb 2026 19:08:58 GMT  
		Size: 14.5 MB (14462523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0aa23dc866fef692bdacef8d999a97d7cd46112fd47ca50740d2ef873225636`  
		Last Modified: Tue, 24 Feb 2026 19:08:57 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc10efac880ef87f532eff8ea62a0662c182e9c7f9ae85223975c895a77fbf4`  
		Last Modified: Tue, 24 Feb 2026 19:08:58 GMT  
		Size: 15.0 MB (14964034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0045931e4d1fdd8f060822ffc2dcd594f803668bc8dd4bff0aad59aa87a30eee`  
		Last Modified: Tue, 24 Feb 2026 19:08:58 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e6d5eaf1222aff2f418b81f51c2702eb95ed939d6366889aaa7f6bb7ff3d8e`  
		Last Modified: Tue, 24 Feb 2026 19:08:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141c6e514078bb65d492bad6587aaca3b810e079970d126ad2a87fc2cf8224de`  
		Last Modified: Tue, 24 Feb 2026 19:08:59 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:28d7cd97e4a0ca63faf32fb17fbde727b97cea9278a7dd9e30e42bdfb4a2de71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6990275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2505047a2639bafe8b05dca21b408d81bf05a006ee0dd9ba05633f2ddc7b4d80`

```dockerfile
```

-	Layers:
	-	`sha256:1ad554219f3f4045247f26474a90ce95ed3a700431ec59777096d343c89a1bc6`  
		Last Modified: Tue, 24 Feb 2026 19:08:55 GMT  
		Size: 6.9 MB (6931641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd847236ba62f7f5a44c91de79cc36a759c082f3e7aa7447dd73f989f47df7b3`  
		Last Modified: Tue, 24 Feb 2026 19:08:55 GMT  
		Size: 58.6 KB (58634 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; arm variant v5

```console
$ docker pull php@sha256:642d227fb4cf8b92555f2846dae1cca43c42a4eee0c3a1d171e297f6803bbe00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154781536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c7a4ce252e5fb25e133c032eb0a323c8d6ec3e84f48bd9a2202897930728ab2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:05:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:05:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:05:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:05:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:05:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:05:32 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:05:32 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:05:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:05:42 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:05:42 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:05:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:05:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:05:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:05:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:05:42 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:05:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:05:42 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:05:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:05:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:08:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:08:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:08:57 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:08:57 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:08:57 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:08:57 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:08:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0355804b1a863607635e8e60f82ed6fec21aeb11cd0f281ea39f54208fab3bb7`  
		Last Modified: Tue, 24 Feb 2026 18:41:57 GMT  
		Size: 25.8 MB (25765637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4764e0a74e6b9ce4338b3acba432a925dee398daaf0b93e667302582647bc996`  
		Last Modified: Tue, 24 Feb 2026 19:09:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19991f2dfd8c4bf3a1920d96419f59d6812b875f71648e022e695a035ac1b7fb`  
		Last Modified: Tue, 24 Feb 2026 19:09:17 GMT  
		Size: 82.0 MB (81984124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30912e409a72ceb61a16d4069ddc2826a23f2d667567a4b78998806861d7aa3b`  
		Last Modified: Tue, 24 Feb 2026 19:09:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07d525cf6b3d921193132b91dae379004e5467b6b081c64a8540dda9d67db01`  
		Last Modified: Tue, 24 Feb 2026 19:09:17 GMT  
		Size: 19.4 MB (19421367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c654513ca9b1bb6619c6c0d663757b308f8ebc3c3016f773e42a3ebef95b0c0`  
		Last Modified: Tue, 24 Feb 2026 19:09:16 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2059c4e2eb684f8ff21667d8e724f6aa92b7677f48c9bc5975cd0fd374acf604`  
		Last Modified: Tue, 24 Feb 2026 19:09:16 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56104947c4b86c524d2a164b84fb24052976c5d788b87b460b9fc8186b6f7997`  
		Last Modified: Tue, 24 Feb 2026 19:09:18 GMT  
		Size: 14.5 MB (14460387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c45c5d7e46907ffcce56d38fc483d6f69dd7da8acd88041e887bba753012d7e`  
		Last Modified: Tue, 24 Feb 2026 19:09:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:933950cc70d2763ec755cfab581e358690f7e7ab907ec94506cc013bf39df68d`  
		Last Modified: Tue, 24 Feb 2026 19:09:19 GMT  
		Size: 13.1 MB (13144546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9ada62a66ee3b02bccd4fd6bb7d50507fff0a08a7d565cd1590e4e09488fd4`  
		Last Modified: Tue, 24 Feb 2026 19:09:19 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbc3e41e5512f829d98e2bccddb4f769342198c193d090bb4b07e97f41c1703`  
		Last Modified: Tue, 24 Feb 2026 19:09:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7870ea4f51a731a42a56e227340adb64f6fd24e63f256135abd5b82f50a233`  
		Last Modified: Tue, 24 Feb 2026 19:09:20 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:097630e245f11508603d058b607e870d86184d6e3353f4cbaea877cc9d2de309
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6799789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc35e282a518b2b7708bb138004e444a985383e00a1f4eb0959f1c4f9dd8642`

```dockerfile
```

-	Layers:
	-	`sha256:2808360bfc24b23f2321697289006090d4fed7a0fe4e7adfd4c80aa57da56746`  
		Last Modified: Tue, 24 Feb 2026 19:09:15 GMT  
		Size: 6.7 MB (6740983 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21ccd4c1f9f58aedb8ee452708fd15e41359ac50661b9e750b244e0179cfbd2d`  
		Last Modified: Tue, 24 Feb 2026 19:09:15 GMT  
		Size: 58.8 KB (58806 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; arm variant v7

```console
$ docker pull php@sha256:a57b7012adefd7b8c8d4a0f3f3d170d5a6ab19437db2f4cd37ebf00dddb33011
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145896427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10423d7b8edb7b409d07d048070af3b03dfad1e7a009d5adeb0257d1704cc0f1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:09:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:10:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:10:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:10:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:10:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:10:01 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:10:01 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:10:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:10:08 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:10:08 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:10:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:10:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:10:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:10:08 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:10:08 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:10:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:10:08 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:10:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:10:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:13:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:13:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:13:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:13:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:13:07 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:13:07 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:13:07 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:13:07 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:13:07 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fa3a48ce9256276c0109937eac189d16b2e2fbe93cf8606c77fe3f68cee49e`  
		Last Modified: Tue, 24 Feb 2026 19:13:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c3a5bda1260cd7b803040797b179cb927b05cb6bf53b89c51916a7d2b40d7b`  
		Last Modified: Tue, 24 Feb 2026 19:13:34 GMT  
		Size: 76.2 MB (76154208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c1c70025682dd699f2927e2abc746e3cce6ca1011d72bb215e0f7a2c4f581b`  
		Last Modified: Tue, 24 Feb 2026 19:13:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787e50b72fa6c7ad9a362edf4567657ae20c3f8f32096b45d1b62db89ef54c58`  
		Last Modified: Tue, 24 Feb 2026 19:13:26 GMT  
		Size: 18.9 MB (18850592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d754346af9385f28f9d1179d63a4b22a071b7be655699d32f9e2eb38b1f55d3e`  
		Last Modified: Tue, 24 Feb 2026 19:13:25 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f352208328be43e73637664a810e37d01e7b1eeb2b1183b3c3de6687b76e383d`  
		Last Modified: Tue, 24 Feb 2026 19:13:25 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6cbea765aeeecddca300c9b09fbb8c383ff50bca858679dde521f6abfc56ba`  
		Last Modified: Tue, 24 Feb 2026 19:13:32 GMT  
		Size: 14.5 MB (14460331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ca17afc7f7f052706cd48677585a1621e6b71ede78bce259be0a83861aa83c`  
		Last Modified: Tue, 24 Feb 2026 19:13:28 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a16035a577185dfe2531ad2254d95a7ee2437950db0aace08cedd23ac2bc2c`  
		Last Modified: Tue, 24 Feb 2026 19:13:33 GMT  
		Size: 12.5 MB (12484403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909a78892421b1757f0c42087d1ed3d1ac522c077a5274db11292c8c0a0f0b01`  
		Last Modified: Tue, 24 Feb 2026 19:13:32 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873f04d6c9f6e67551dd6bd262906398f4379c2b8840792744f02c2b783c64f0`  
		Last Modified: Tue, 24 Feb 2026 19:13:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a388071726988657cae43763d7c568fa00a377214fdc27c5414dd34ccbf5cd3`  
		Last Modified: Tue, 24 Feb 2026 19:13:34 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:3fb8b512d7d413bb774a33d588fcbb64d5fb3e18242d086e3639d98f56329957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a371d42e7314d14cf91eb180857f39ca9213909cab7ffd7aac8ed42c0f98f09`

```dockerfile
```

-	Layers:
	-	`sha256:64a353873dee457c9d98fa2d9eb173afec839e9b9657bd915d9af99474609d1e`  
		Last Modified: Tue, 24 Feb 2026 19:13:24 GMT  
		Size: 6.7 MB (6744959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e257b893efbdca5341393746902f032a6fa76398594cc3188faef3e3b0cb6af`  
		Last Modified: Tue, 24 Feb 2026 19:13:23 GMT  
		Size: 58.8 KB (58806 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull php@sha256:bf0df43601c655044f4320b2af478c043bc97335ced627908d3f6fd8db8c008a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175426634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9966fa66be56f6006db12b74c9cbc9c71334128fd988753eaa95537ca9a4e017`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:08:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:09:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:09:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:09:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:09:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:09:09 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:09:09 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:09:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:09:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:09:16 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:09:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:09:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:12:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:12:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:12:28 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:12:28 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:12:28 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:12:28 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:12:28 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86ef32467aa8b10a9eb06972ad257f3280da2e1b800eb8c63b9e44afd2728b8`  
		Last Modified: Tue, 24 Feb 2026 19:12:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02fb82b439647f377a1702f28798eb112604a6e1e39fdf83d2115b95eef828e`  
		Last Modified: Tue, 24 Feb 2026 19:12:50 GMT  
		Size: 98.2 MB (98167982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da26482dcf9e31346e12647c8a4785ad0d5018ce0bf8befa6b4ba862b74a3a6`  
		Last Modified: Tue, 24 Feb 2026 19:12:41 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7237d441bc09475d95f038781478bd14061078240c6f89e4433bd6db7c134a36`  
		Last Modified: Tue, 24 Feb 2026 19:12:49 GMT  
		Size: 20.2 MB (20163649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7182e844d4cdb9b000ea10bfef2d91532d521d4dbfc13d165be367a6adcf2514`  
		Last Modified: Tue, 24 Feb 2026 19:12:48 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0d63f2bd7b7ce6f73e6a1bf22efd8223e04d9f5257d3453ebdee9d4db4a441`  
		Last Modified: Tue, 24 Feb 2026 19:12:48 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20c20a36c789c754dcf454138341a05bee2a39ad9a235dba4db2ada78f5d28b`  
		Last Modified: Tue, 24 Feb 2026 19:12:50 GMT  
		Size: 14.5 MB (14462154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585a4cde49e3bd253e7da58e560aca9d44ffcbe7dc339f4d511dd05fb381afd`  
		Last Modified: Tue, 24 Feb 2026 19:12:49 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd13260a7f68c0d2e654f2cdcaa6367d71fcb926918774d3cad06cdef3be00c`  
		Last Modified: Tue, 24 Feb 2026 19:12:51 GMT  
		Size: 14.5 MB (14511281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4bfb2a16faf0ceeaafd81a3cca92a772d3836ae5d24e7f4702ff71fcb440aef`  
		Last Modified: Tue, 24 Feb 2026 19:12:51 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3b721e767dc71c45e7c246336ea559ab255bdaa95c6f13376ddb3e45cad7ae`  
		Last Modified: Tue, 24 Feb 2026 19:12:51 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a420aa78a50e49c8caba057f8e6c3b865cb979ffd04bd7c084dc84d4dd957326`  
		Last Modified: Tue, 24 Feb 2026 19:12:52 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:e3b4e03197707dcf8efe399267c6e6eda46b79045eb71d1be22d8fdeb9effda0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7018894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97aaadf85620af0d764224cea8e224eb4f0bf4c8caa151330200cbff0371026d`

```dockerfile
```

-	Layers:
	-	`sha256:2d91dc1234c6b21729f7669868e0f9a4b7872e07d736e92343795cd7e44338c5`  
		Last Modified: Tue, 24 Feb 2026 19:12:48 GMT  
		Size: 7.0 MB (6960048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6f465930071734adce57c5310afac0332e36652f9cb8fa4f5534240b0cd881d`  
		Last Modified: Tue, 24 Feb 2026 19:12:48 GMT  
		Size: 58.8 KB (58846 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; 386

```console
$ docker pull php@sha256:d69f04c6a9102db992f773ace58f7b506a5781262f1f502341dcd7864dfaeef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.2 MB (181178414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f715f5fb40a416519b60954646f92e447c9e9a42f441a3f26840c8d9cf6fd2c1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:01:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:01:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:01:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:01:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:01:25 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:01:25 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:01:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:01:32 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:01:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:01:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:01:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:01:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:01:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:01:33 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:01:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:01:33 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:01:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:01:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:04:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:04:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:04:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:04:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:04:52 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:04:52 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:04:52 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:04:52 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:04:52 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bab6f574391274ab5dcfab8bda32d58ff3363c5f6d8b329979ceac5bd4afee6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 29.2 MB (29221705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1bada0816798a481d5694551065743798710a54795b5077bf911c43668de6f`  
		Last Modified: Tue, 24 Feb 2026 19:05:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:729aa62bcfdba517f3577f64c720c12e133726cec6a6a0164821de7dd86c765d`  
		Last Modified: Tue, 24 Feb 2026 19:05:18 GMT  
		Size: 101.5 MB (101526922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f318ec1fe3c296306ee9a5d7bf4364177c3fe97a1c8b15af6256088d2f5170`  
		Last Modified: Tue, 24 Feb 2026 19:05:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9237375df36015d3993b8fa6e25de83c8cb2a75baf09eac6d278d6e97b44c390`  
		Last Modified: Tue, 24 Feb 2026 19:05:14 GMT  
		Size: 20.7 MB (20665553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94ae9958bbb7cd96005185dbb442ef0256311e7508540c8f002b5721bca2d7c9`  
		Last Modified: Tue, 24 Feb 2026 19:05:14 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8eace960c355197ea02b7f08c06712f58e280bdcaf074ba3b91ae1a0947007`  
		Last Modified: Tue, 24 Feb 2026 19:05:14 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbca58c110eddab8da78faebe59b8581ddf633bf1ffd787752f8621051f899e4`  
		Last Modified: Tue, 24 Feb 2026 19:05:16 GMT  
		Size: 14.5 MB (14461470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65815ba873e10088a83b0a83c2e010d55dc22165c389e50ce5ac17a669d47b1`  
		Last Modified: Tue, 24 Feb 2026 19:05:15 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29557568187fdf614ef193fa8b049e2b6d536ce84e1a8f8eeef9955f21067508`  
		Last Modified: Tue, 24 Feb 2026 19:05:16 GMT  
		Size: 15.3 MB (15297278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d3a2532a7b95ce7aedb3bd1d7fbf698b79a04d6c75990d825feda790bbe7f7`  
		Last Modified: Tue, 24 Feb 2026 19:05:17 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a659d50c80d127b77d7a679d9dfe52d60c3430d266584f6761d46c6121ea83d6`  
		Last Modified: Tue, 24 Feb 2026 19:05:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49a3d97096d81b89ec7b3cb03e98f5b5427446a513353e83302df1a695bf54b`  
		Last Modified: Tue, 24 Feb 2026 19:05:17 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:83f60a3499f9565d840f679345903ccc7a33522f2103bf174936d178515a6af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:170c9a389998ca8d4eda4f1f64e190e81875f7643054f2a908300af3d6d71526`

```dockerfile
```

-	Layers:
	-	`sha256:4d67431cb6502442f94ed002dbfe86309488adb0e2d0f505fa6298964b53807d`  
		Last Modified: Tue, 24 Feb 2026 19:05:13 GMT  
		Size: 6.9 MB (6911401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bdd3e5c1c0a3250cf03da59746ce9fcefbb185bca0786f3b618a110453d1ae0`  
		Last Modified: Tue, 24 Feb 2026 19:05:13 GMT  
		Size: 58.6 KB (58586 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; mips64le

```console
$ docker pull php@sha256:4f1326731c7e656bd3d58794d3e208728eee423ab0375997880ba82c0333e32e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.1 MB (157063584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7108c54c95f35be3fc5eae49a2eba6bc4d2826e367398af97e6621f9fe528a9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 18:54:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 18:56:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 18:56:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 18:56:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 18:56:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 18:56:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 18:56:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:17:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:17:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:17:28 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:17:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:17:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:17:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:17:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:17:28 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:17:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:17:28 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:18:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:18:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:36:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:36:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:36:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:36:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:36:10 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:36:11 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:36:12 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:36:12 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:36:12 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:00b501106805d55ebe605ff077d09c8c22aa2ccf0dd9ceffb2a21c5319633322`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 28.5 MB (28526197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:506553368192ed02c2e77ece7b4fed5754d238a3247e9404b085275c8f85db43`  
		Last Modified: Tue, 24 Feb 2026 19:15:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768e8a03a9c01cacd6821f506a55e79ca491f3ae8a3dd89e497eb0c27ff23167`  
		Last Modified: Tue, 24 Feb 2026 19:16:03 GMT  
		Size: 80.7 MB (80674376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf85cab495030131ec6138239e94ba561aeaf115d5d9a16c18e0753bfd7e18ea`  
		Last Modified: Tue, 24 Feb 2026 19:15:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9e3bc8e6e451d6e0f5ab9427327bb1db7deb67e756fd939a325b922eb817de`  
		Last Modified: Tue, 24 Feb 2026 19:37:07 GMT  
		Size: 20.1 MB (20078946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254583b4e6c7d19fbde3e0e5bb83b404180f754080089df970b739c730387eb8`  
		Last Modified: Tue, 24 Feb 2026 19:37:03 GMT  
		Size: 438.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33d80030b9713bf097878cdc4bc43ddd85905a046edf7e148f6fb9a611ccecb8`  
		Last Modified: Tue, 24 Feb 2026 19:37:03 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49b9f1877ba994a817a7328e62d2e6edf1011aef5b1518b27b510f8363b5403`  
		Last Modified: Tue, 24 Feb 2026 19:37:06 GMT  
		Size: 14.5 MB (14460051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd454d974f036db4f3276f4fe3aab78b72b61301b196400ae3fe7fa0dfbabdd5`  
		Last Modified: Tue, 24 Feb 2026 19:37:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e555d0f2954a8a5ab7495dbb3b01ebc10d25213aba8203c978b8293938accf`  
		Last Modified: Tue, 24 Feb 2026 19:37:08 GMT  
		Size: 13.3 MB (13318504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:411cde392d7c55460ecd29f45a696b89ddde4cb4e2d13710387e64c9156944ff`  
		Last Modified: Tue, 24 Feb 2026 19:37:06 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2bd7da20ab5e2ef9c1687f0d5c3177d5a78253608c7d9868aef67112c734b68`  
		Last Modified: Tue, 24 Feb 2026 19:37:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd51e30180fc9ce4c13593b44bee2fe74cf957e274adb0e0b1cc4bd48d3da6ca`  
		Last Modified: Tue, 24 Feb 2026 19:37:08 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:986861eaa083da01930f702c016a885bc73ceea3439d94956de79b7ffffa6f7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 KB (58497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9395122aed6d185b7c8540544515c092c1fb8e1bb3273825b101d82a5b66e8c2`

```dockerfile
```

-	Layers:
	-	`sha256:8438e0e75086cbd55f7c834609602ea5b5295cb99c6215bf98243bd853ddb339`  
		Last Modified: Tue, 24 Feb 2026 19:37:02 GMT  
		Size: 58.5 KB (58497 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; ppc64le

```console
$ docker pull php@sha256:44453430f75689bd7d6bb3e59c69230fa67b9f941a6a4e70b0f0657f534d9a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.2 MB (186169269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1278b14fe8c6f0118397dd525fa36f982186f93c94b279e35d58a75c4627df5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:45:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:45:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:45:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:45:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:45:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:45:53 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:45:53 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:47:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:47:03 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:47:04 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:47:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:47:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:47:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:47:04 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:47:04 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:47:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:47:04 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:47:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:47:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:52:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:52:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:52:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:52:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:52:15 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:52:15 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:52:16 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:52:16 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:52:16 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3def25e912c223ee8b3899e5ca048b2439f856f438ac690293817fbc0291fb36`  
		Last Modified: Tue, 24 Feb 2026 18:41:49 GMT  
		Size: 32.1 MB (32078334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8909961eea48ef1b6874fc78e0a2a67be659ef1f501c141db727def77188f`  
		Last Modified: Tue, 24 Feb 2026 19:51:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ee44b9ad8e875a3f516f25b3e3c40a3cd26acc45cc0e89783e3044adfc8d3f`  
		Last Modified: Tue, 24 Feb 2026 19:51:33 GMT  
		Size: 103.3 MB (103330209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1044ec1105edb234be52095b7e7657e4bc5695912aac59d3a42b6d4609d990`  
		Last Modified: Tue, 24 Feb 2026 19:51:29 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c028bf874b5c30f73241cfb2f6871fc75b09cb312e452d430fdfa56bfcec3db`  
		Last Modified: Tue, 24 Feb 2026 19:52:49 GMT  
		Size: 21.3 MB (21332466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0702448893b5ade5883b68b8cd1235da79117ebdd7f4f6c29de6e57ca17b680e`  
		Last Modified: Tue, 24 Feb 2026 19:52:48 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac90603a6aa9fb56eba677ab1d2384d71ea434e594e4b239aee8160b8cb2a68`  
		Last Modified: Tue, 24 Feb 2026 19:52:48 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba9d37167f00c31c9a8d84f02ac0301e400218933390d034658cdb9fdb9b67a`  
		Last Modified: Tue, 24 Feb 2026 19:52:49 GMT  
		Size: 14.5 MB (14462034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfad41c2a3da2ecd4ad8cbfc031db2d6baea316d2f2c7e2334cbaa8659dd83fb`  
		Last Modified: Tue, 24 Feb 2026 19:52:49 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0743e0f5927c42ce1887929400635eda5a8dfd6b0913b3ed3f0636d5b8e3868`  
		Last Modified: Tue, 24 Feb 2026 19:52:50 GMT  
		Size: 15.0 MB (14960719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6743298c324751daa656fdb7f385a6e97959b1f61a6c04f435508b93ea42cd2b`  
		Last Modified: Tue, 24 Feb 2026 19:52:50 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae867c03f101ff18e788bdea0c967637b38fc3d17ad4a3690d1ed38ad1e55c62`  
		Last Modified: Tue, 24 Feb 2026 19:52:50 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79445c9135810b9bb4e348d4511b8b3581d6888b49a3cc72bcee700e66c5c97d`  
		Last Modified: Tue, 24 Feb 2026 19:52:51 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:58f4e2e7e2edeb6a537e774e459ed0e9baa5dc5ca475adda8f92fc93e70b71bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6967117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6495aa3af30416d6d85fe091c07ecab7da4f7ba0fff50ea87bf5f722ef34ae`

```dockerfile
```

-	Layers:
	-	`sha256:515f538fb69c3f4748188e254b9060f255bb00858ba6dfb672f53e829458ed8e`  
		Last Modified: Tue, 24 Feb 2026 19:52:49 GMT  
		Size: 6.9 MB (6908423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8490dc42e959c4e67ce786df8d345f03e270285be075c571719604baf59b7f63`  
		Last Modified: Tue, 24 Feb 2026 19:52:48 GMT  
		Size: 58.7 KB (58694 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bookworm` - linux; s390x

```console
$ docker pull php@sha256:ba53fc589439c940d025669346cd760864636f00f8d97f90644b9027ff9880cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155614905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cb5f79bb99735faac09e7f024d28e3aac6c06589ca884c649df9efcc3de267`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:19:26 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:20:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:20:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:20:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:20:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:20:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 24 Feb 2026 19:20:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 24 Feb 2026 19:20:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 24 Feb 2026 19:20:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 24 Feb 2026 19:20:34 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 24 Feb 2026 19:20:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:20:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:20:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:20:34 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 24 Feb 2026 19:20:34 GMT
ENV PHP_VERSION=8.5.3
# Tue, 24 Feb 2026 19:20:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 24 Feb 2026 19:20:34 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Tue, 24 Feb 2026 19:21:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:21:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 19:27:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 19:27:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 19:27:03 GMT
STOPSIGNAL SIGWINCH
# Tue, 24 Feb 2026 19:27:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 19:27:04 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 19:27:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:27:04 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0454182b759ca8367a521776a323cf567d04897caf35e4917b8c18696f0abb22`  
		Last Modified: Tue, 24 Feb 2026 19:26:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2c4b9916cf53a37e714a9d11da7d100b53b12008dd63b0c9c69e5343628e4c`  
		Last Modified: Tue, 24 Feb 2026 19:26:41 GMT  
		Size: 80.8 MB (80828336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf2779b25d90ffba89b1a396b71a9bc01a3518169905e9071645f37e7dfa2c1`  
		Last Modified: Tue, 24 Feb 2026 19:26:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d5aac47c7df8f9de88e6f43980528639285693eb2aa4b4523e348d07af6feb`  
		Last Modified: Tue, 24 Feb 2026 19:27:26 GMT  
		Size: 19.9 MB (19919106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f8a09496a69ec710ca1962e77d5f3f63d5912a94ff8cc02e9558f3cea4ffb5`  
		Last Modified: Tue, 24 Feb 2026 19:27:25 GMT  
		Size: 440.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf014498df6dcb5dff6568275a6b0677cba2a82c09530290b8d03076741384a`  
		Last Modified: Tue, 24 Feb 2026 19:27:25 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c60128fbdbedc0c26a2ea3e2939de0d07d2c70495619dacc2e9d9aeb2e20b9`  
		Last Modified: Tue, 24 Feb 2026 19:27:26 GMT  
		Size: 14.5 MB (14461084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ea2e5194a9498d13469c3ef3fe75fad25c31e790918a7d9072216f16ec5f10`  
		Last Modified: Tue, 24 Feb 2026 19:27:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a11c6c77c878ebeaf4aafd4f158ef1ae98f7dacd0fe28dcc9414200633a2a82`  
		Last Modified: Tue, 24 Feb 2026 19:27:27 GMT  
		Size: 13.5 MB (13509356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f029c18a521cbbf92159d2162e1e7a60d1f25bbe2dc56bf22472b0b372fc5683`  
		Last Modified: Tue, 24 Feb 2026 19:27:27 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02c5975335d3c0fe65e6111d89faffda6ac59be7d4f61deb71462d6ef1deb33`  
		Last Modified: Tue, 24 Feb 2026 19:27:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8da781d94707d543147d4b3a939e5d8aa3ff63add912cc2bc777535e174f61`  
		Last Modified: Tue, 24 Feb 2026 19:27:27 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:820d53b5ba5b0a3455b0d43708f5d129d37cc380e58ae94b3c15aeba27242166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6827471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86eeaee646a31e04b7500bc2768031ccceffe83259dabe04ffb2c52fd4f790cf`

```dockerfile
```

-	Layers:
	-	`sha256:8563a820925cd82ea4506cd8b66e7d1efa0929c7b314af9fb75602049e4fc4f1`  
		Last Modified: Tue, 24 Feb 2026 19:27:25 GMT  
		Size: 6.8 MB (6768849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0efe6a69bd730c7ed1bb3e83c18028d311c9a169509f55188740ff7bd15766bf`  
		Last Modified: Tue, 24 Feb 2026 19:27:25 GMT  
		Size: 58.6 KB (58622 bytes)  
		MIME: application/vnd.in-toto+json
