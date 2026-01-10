## `php:8-apache-bookworm`

```console
$ docker pull php@sha256:81476b1d093592ca159d646c2b34e8180d0f377177926d994a42d16dd2364335
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

### `php:8-apache-bookworm` - linux; amd64

```console
$ docker pull php@sha256:7c3cfde2baa90b0c655551aed1568053f68e60ea2254df243e1e3c02972bb03c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182097156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:372c2adbd46a075a486765e0c44f648f226326c563982151b0d4fc4e1e3d1096`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:30:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:31:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:31:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:31:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:31:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:31:12 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:31:12 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:31:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:31:19 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:31:19 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:31:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:31:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:31:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:31:19 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 09 Jan 2026 22:31:19 GMT
ENV PHP_VERSION=8.5.1
# Fri, 09 Jan 2026 22:31:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Fri, 09 Jan 2026 22:31:19 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:31:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:31:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:34:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:34:39 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:34:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:34:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:34:39 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 22:34:39 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:34:39 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 22:34:39 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 22:34:39 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0347dcb76707f7d71a7c0b3a5f4a63b97cdd9923e637e67ad65b3b2d4ba05942`  
		Last Modified: Mon, 29 Dec 2025 22:27:06 GMT  
		Size: 28.2 MB (28228424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057aed7214bb804ec97ea715e215b53d9f8cbad3d7ce7a0b5077582fe9129727`  
		Last Modified: Fri, 09 Jan 2026 22:35:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c6ceb3e7a255991468d0e29c9a9000150f6ee4011b02848555e0c6c74a1354`  
		Last Modified: Fri, 09 Jan 2026 22:35:24 GMT  
		Size: 104.3 MB (104330707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d178c7d9c334f09d52607f514321847945c3ce396503cad75aa380d01e3196d6`  
		Last Modified: Fri, 09 Jan 2026 22:35:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae808c10d97e9a3784a1360a27980b900445f812a5987ccaaae9cd36916eedd0`  
		Last Modified: Fri, 09 Jan 2026 22:35:14 GMT  
		Size: 20.1 MB (20131826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b40079fef2f92d1c52600bb358a5c190d2c7f5b70698d868aba5e7132acf19`  
		Last Modified: Fri, 09 Jan 2026 22:35:11 GMT  
		Size: 426.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873bc334eead948b82fa67a6b2188f8aa7caf50d7d77e4ef2a4e314721831268`  
		Last Modified: Fri, 09 Jan 2026 22:35:11 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aec45927688bd726c54b8d124ec79cd895ffdc38ee7878fd6c65ef30ad4c188`  
		Last Modified: Fri, 09 Jan 2026 22:35:12 GMT  
		Size: 14.5 MB (14455608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f8b4ebdbad7f9ee316126d4d3082099fda2b22e1f8d36b48379cc238b8657f`  
		Last Modified: Fri, 09 Jan 2026 22:35:10 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a279701e0122bce0102f1034a6bf9b36d4c2ffce0bc6be109d2d48859c78bcf4`  
		Last Modified: Fri, 09 Jan 2026 22:35:12 GMT  
		Size: 14.9 MB (14945117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d524ae9fc3245b1153fa533730fd337b0629074d90b529a65cc7b70045985e2`  
		Last Modified: Sat, 10 Jan 2026 00:17:05 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2e296ad901c1f145cdadb851af69879bf5c58c16dc1522534d8d0b27504af2`  
		Last Modified: Fri, 09 Jan 2026 22:35:11 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f8ba36a209797e111e30c9d1ecc0d4de0fc97508c66839d19ee6362d234c2f`  
		Last Modified: Fri, 09 Jan 2026 22:35:11 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:656f63d63da20af3cfeea1ca6a4d69eca0aa026b1b5cc30a1bdafe1f9c73ff29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6990265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32dd2d26796bf46000350b509e3b9150c17e411ad2b0770a467ad9a549bade47`

```dockerfile
```

-	Layers:
	-	`sha256:6fd00c23c1d9139cdfb2d25ec0c4359d9358ef9354ce6e0ca7e87a8afb27a363`  
		Last Modified: Fri, 09 Jan 2026 23:57:14 GMT  
		Size: 6.9 MB (6931631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6220c3931ed612718118f22ac2a3d79c59273417fba34d1bd95b15b06ef98a4`  
		Last Modified: Fri, 09 Jan 2026 23:57:15 GMT  
		Size: 58.6 KB (58634 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-bookworm` - linux; arm variant v5

```console
$ docker pull php@sha256:ad8a630b264629c4510ad424fc11514dd688e651cbd0351c63fea32cbac86a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154763840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a4944f6d5736aaae25bf8bfae95adc4382c7005daf1d03b234dbe934c5732c6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:38:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:38:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:38:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:38:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:38:23 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:38:23 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:38:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:38:32 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:38:32 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:38:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:38:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:38:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:38:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 09 Jan 2026 22:38:32 GMT
ENV PHP_VERSION=8.5.1
# Fri, 09 Jan 2026 22:38:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Fri, 09 Jan 2026 22:38:32 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:38:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:38:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:41:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:41:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:41:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:41:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:41:50 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 22:41:50 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:41:50 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 22:41:50 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 22:41:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cdd01b66e4b6599d6f59fe75d883783e8ddfc67db8fda967c6ce250da575cc0b`  
		Last Modified: Mon, 29 Dec 2025 22:25:33 GMT  
		Size: 25.8 MB (25757576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f048d17806ce9da041a3db8d4261b4117f50504999176178475443093fc51fc5`  
		Last Modified: Fri, 09 Jan 2026 22:48:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41449d34d1ee68d70bfea6e1d1295127ef16172009cac49ed197b966a56d73c5`  
		Last Modified: Fri, 09 Jan 2026 22:42:21 GMT  
		Size: 82.0 MB (81981423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6181a0ae3f56b62cb891d88b20e3c313460fa1f0cf9f92d93ca45984270619a6`  
		Last Modified: Fri, 09 Jan 2026 22:42:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19aef6ee623190a73530e5e32d37e5397a9cc0b447dd4ccdc8244d79f1face0f`  
		Last Modified: Fri, 09 Jan 2026 22:42:18 GMT  
		Size: 19.4 MB (19422381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf1a659205e1856256057e27a58d2f3ae75221db23456b7d1cfd7e4d76ce8b4`  
		Last Modified: Fri, 09 Jan 2026 22:42:16 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477370955b2f5c7df8fb12611108e518f94e8046ebad4a049bff61e9608bd72a`  
		Last Modified: Fri, 09 Jan 2026 22:42:16 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2197cf31184aba61ad735adc755d15b5977dbf75cf6c07ef136060e9149c5fab`  
		Last Modified: Fri, 09 Jan 2026 22:42:17 GMT  
		Size: 14.5 MB (14453611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab6221bcf317986884d286291e5317bfd5a5199a392ab2f7c52f8902bc16059`  
		Last Modified: Fri, 09 Jan 2026 22:42:16 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7fbf25872f67914ebe59ac137df7e02c991b1d7e99645a2c5aef42caf82b1ee`  
		Last Modified: Fri, 09 Jan 2026 22:42:17 GMT  
		Size: 13.1 MB (13143357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08e3d49b8f4472c6f1a7d4dfc18757e24bbd702e42061e19fdcef45b5a00ccb`  
		Last Modified: Fri, 09 Jan 2026 22:42:16 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e02fef06e4bb8357455eb2d7795b922fe278e1dc580cf4b12befa61238132cc6`  
		Last Modified: Fri, 09 Jan 2026 22:42:17 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e99cba0dcfacfb22be72697f5a54aa50cdb0bc2d7a30745dba00a45afac0bc7`  
		Last Modified: Fri, 09 Jan 2026 22:42:16 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:3101e84bb22e1a5ede7895108dde8f446f039f4c1612cd48b3f29cb3f1242e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6799779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014e1bb73b806acedb9da0f01b1347dac42b08ae412dcc0af2efa8490bdbeca3`

```dockerfile
```

-	Layers:
	-	`sha256:2c8100126b3f3ef911b327c5828a3b2e70c48cd95950217af37c1b153de603a9`  
		Last Modified: Fri, 09 Jan 2026 23:57:20 GMT  
		Size: 6.7 MB (6740973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f4a3fefaa30924338eb694708752b8478dc1ee278faf6147fb4b15688acaa6f`  
		Last Modified: Fri, 09 Jan 2026 23:57:21 GMT  
		Size: 58.8 KB (58806 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-bookworm` - linux; arm variant v7

```console
$ docker pull php@sha256:f246a87d59bb12737b5e6e13beac7d605bc51f926e41299bb04f631310b65eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145874618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86faffe98c033781fd82767909d79f4e1c90318050e3cee86705e3356b9544d8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:43:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:44:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:44:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:44:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:44:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:44:08 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:44:08 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:44:15 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:44:15 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:44:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_VERSION=8.5.1
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Fri, 09 Jan 2026 22:44:15 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:44:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:44:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:47:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:47:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:47:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:47:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:47:25 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 22:47:25 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:47:25 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 22:47:25 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 22:47:25 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3733e79b87ec6af3c60809fa9882f5d220b1e1fc2459b7d6a5b3167dc8eb7155`  
		Last Modified: Mon, 29 Dec 2025 22:25:04 GMT  
		Size: 23.9 MB (23934053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcb090f1d21d6c9cf3d4937306130af775c6b8f77b7015bbc3aeec7831e00cd`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6bcf417f4c97734fc37095a7f4c9b4cfa7d5b09bfe0c3da212d45e63079a7b`  
		Last Modified: Fri, 09 Jan 2026 22:47:58 GMT  
		Size: 76.1 MB (76148731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b714c6e3ee2e505ebbf8085d3c232291b10a74563d8e2886cc4677b5c8b7fe`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba97861883a05a5fe227b13559b8b9477552ccbce71a196429fdd7ba71d8c4bf`  
		Last Modified: Fri, 09 Jan 2026 22:47:53 GMT  
		Size: 18.9 MB (18860044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f877b2e5c7edf9f5fd98f943e52013a9ee513903917ac0e6697d9b819d07350`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cb1bd16c15ea76aea5f1cd5ec4c5f28d6739045d25f1fdb092673752891b9`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee22ba4a3127146fe51e675e97911ab3db1c2f9ce2da6545ae98470bb183c76a`  
		Last Modified: Fri, 09 Jan 2026 22:47:51 GMT  
		Size: 14.5 MB (14453585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e49c4221658cc2592bbee79a2b53dc2697e3e114cc88bdcfcd06c72f9c6fbb0`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6ac276e2ca262d548dfd6549d0730a47910851e68bb79cb7beaba566820e0`  
		Last Modified: Fri, 09 Jan 2026 22:47:53 GMT  
		Size: 12.5 MB (12472717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b7e94d669f5aee76b72213950ef1ce0f34e78c436e4d3a731b9a24431920b5`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469b8bd6d4510c48d483e49a8c3c7b089b9165a1106bf24536744ad1d9380532`  
		Last Modified: Fri, 09 Jan 2026 22:47:50 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86c8e110868bfebd15da184e18501b18278fe6d70bc4f00e8418d57cd9f51222`  
		Last Modified: Fri, 09 Jan 2026 22:47:51 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:60e8e269880074aa8d874a01494547ad0c1f81fa7654e89f44234d024f17d739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6803755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345ab5d21691083931701df9a2dbc414ed81bf0a79cf7260aaf65232ff77d3cb`

```dockerfile
```

-	Layers:
	-	`sha256:c4c3361a2262198f361b75bf10907c6617d5039c34c3fb253a92134f148ecbfc`  
		Last Modified: Fri, 09 Jan 2026 23:57:27 GMT  
		Size: 6.7 MB (6744949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8138f7e3ee12bff2f44e3e539ba07da95cce6a63ac05771ad45f21117d231990`  
		Last Modified: Fri, 09 Jan 2026 23:57:27 GMT  
		Size: 58.8 KB (58806 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-bookworm` - linux; arm64 variant v8

```console
$ docker pull php@sha256:34cbabd90c1d0a8610a7220d264ec465769be71bf2c64142cad56c162f69c69a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175391443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3dc14e69466423ea0515ac21742832ece6caf73f2cde4ea0f1092e3e1fbe9f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:25:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:26:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:26:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:26:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:26:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:26:00 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:26:00 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:26:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:26:07 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:26:07 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:26:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:26:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:26:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:26:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 09 Jan 2026 22:26:07 GMT
ENV PHP_VERSION=8.5.1
# Fri, 09 Jan 2026 22:26:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Fri, 09 Jan 2026 22:26:07 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:26:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:26:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:29:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:29:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:29:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:29:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:29:27 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 22:29:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:29:27 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 22:29:27 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 22:29:27 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b1efea88fbf7c88bbbdeec2e84bd4f8d0b814c210ee65763f6d4cc91c28365e8`  
		Last Modified: Mon, 29 Dec 2025 22:26:16 GMT  
		Size: 28.1 MB (28102210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb2816a0319170e1c8783a27f0ce2556a5ac7420407d182d9cc375d4b1b68e1`  
		Last Modified: Fri, 09 Jan 2026 22:29:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db95465b3ad974414d3580e358c1aea4e574d4c69abfc08b548778e99b393347`  
		Last Modified: Fri, 09 Jan 2026 22:30:04 GMT  
		Size: 98.2 MB (98165325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79207bee0f7ef7078307cbce704903264cee9a9df76de93fcafb5f14daf0c281`  
		Last Modified: Fri, 09 Jan 2026 22:29:57 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4283a11be619956afdf6d6d6fa0d2986aa827a0dcfb8fdf6216b23d2caca1bb0`  
		Last Modified: Fri, 09 Jan 2026 22:29:58 GMT  
		Size: 20.2 MB (20159033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70ce0ad3e2c5ce8513af38c8130a51cfc7673a2ef2e4ea80f0f24abc355573b`  
		Last Modified: Fri, 09 Jan 2026 22:29:59 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f370b20a39ff922e4069efe4f45e949c3bd33a7d040706715dcb5bde3d5bc70`  
		Last Modified: Fri, 09 Jan 2026 22:29:57 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05196421f11344111a1c4b54ec50daa20a21b543d1eb7968d99f2ef04563ea8f`  
		Last Modified: Sat, 10 Jan 2026 00:16:20 GMT  
		Size: 14.5 MB (14455269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24639a119546030dd9b0afba48de29f4f65b6d339c62b843f06d127394c640c`  
		Last Modified: Fri, 09 Jan 2026 22:29:57 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b6a40ec79b6345bae1376ca6287fb1fdab94201a6b0817caabd231677118da`  
		Last Modified: Fri, 09 Jan 2026 22:29:58 GMT  
		Size: 14.5 MB (14504126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136fc99e94931336fb0b4caad2ae46466e0bef120fb8ed38647c179cb5822ceb`  
		Last Modified: Fri, 09 Jan 2026 22:29:57 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84089d9504d441e220bfd5d2f4c6ef95a0ae6b310f02c2b8b3c66ecebcf984d3`  
		Last Modified: Fri, 09 Jan 2026 22:29:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4cc9eb585245367a97fc5042a670507125b03f7b3ea24c43dfb7c15b4b29d4`  
		Last Modified: Fri, 09 Jan 2026 22:29:56 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:0532478eb4d4407e101af63ece404cb9b85f7a8f1c9c09f450a341255cd715cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7018882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836dd1d46efeeec7c0c03dfe55338eff4d6a288f9da5fc93b809fdb2032a23ab`

```dockerfile
```

-	Layers:
	-	`sha256:58c089b310bc0cc41630ba578fac03eb8dbe163fa11296761dbbdbffec12c856`  
		Last Modified: Fri, 09 Jan 2026 23:57:34 GMT  
		Size: 7.0 MB (6960038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77fdd3bd0bb80ed455af627e9f50dfa8ff8bef33f6d75887a182faf5cac2b720`  
		Last Modified: Fri, 09 Jan 2026 23:57:34 GMT  
		Size: 58.8 KB (58844 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-bookworm` - linux; 386

```console
$ docker pull php@sha256:d1c99f3922fc71844cb9caf766d1f76f659688d820f7a6a6baf38d85a36e1e19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.1 MB (181133543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52298e797268e66ccb455b71c533d15e2d9c900b1919148671aa04973ac20b3a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1766966400'
# Fri, 09 Jan 2026 22:30:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 09 Jan 2026 22:30:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 09 Jan 2026 22:30:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 09 Jan 2026 22:30:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 09 Jan 2026 22:30:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 09 Jan 2026 22:30:27 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 09 Jan 2026 22:30:27 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 09 Jan 2026 22:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 09 Jan 2026 22:30:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 09 Jan 2026 22:30:35 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 09 Jan 2026 22:30:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:30:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 09 Jan 2026 22:30:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 09 Jan 2026 22:30:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 09 Jan 2026 22:30:35 GMT
ENV PHP_VERSION=8.5.1
# Fri, 09 Jan 2026 22:30:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Fri, 09 Jan 2026 22:30:35 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:30:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:30:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:34:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:34:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:34:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:34:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:34:02 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 22:34:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:34:03 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 22:34:03 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 22:34:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f67520a70f469d560f84fd587586b5b9a9f46691d2f4b10c88544b5d21f5fe06`  
		Last Modified: Mon, 29 Dec 2025 22:24:46 GMT  
		Size: 29.2 MB (29209773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9597d7509177c6bd2de86881234312bf976a12800e8b06a43fd3db9d5eda3`  
		Last Modified: Fri, 09 Jan 2026 22:33:47 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4822d4be4b4812fff53b48d63c96ac06640bf0f70df7075002748cecc4366a4c`  
		Last Modified: Fri, 09 Jan 2026 22:34:44 GMT  
		Size: 101.5 MB (101518621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334fad0c6b8c32c1d0d453bc33c5c13aa956cdb67d1def67519aa5af3bd55568`  
		Last Modified: Fri, 09 Jan 2026 22:33:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4970376d6a643e3c6f67dfec5380746ec6e9ed32ebf3615d5cc10fed28f7a8d1`  
		Last Modified: Fri, 09 Jan 2026 22:34:35 GMT  
		Size: 20.7 MB (20658448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dec67b45741cfce82ab3ad35954fcbf1718f6341c6ad5d371fef2c33cd2ac70`  
		Last Modified: Fri, 09 Jan 2026 22:34:33 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1656302b7ee2f98de7a7d82fd98fe7e091e8008161a8dcfcf9ebb3675f443aa2`  
		Last Modified: Fri, 09 Jan 2026 22:34:33 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490beeb644a2ff87aa728574186f8f43c78819e83d8a861bac5bf4318bcf0422`  
		Last Modified: Fri, 09 Jan 2026 22:34:35 GMT  
		Size: 14.5 MB (14454566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5660fd0c46ac52f7108ee3ec89defcca505085da00147120942eb6b653239dbd`  
		Last Modified: Fri, 09 Jan 2026 22:34:33 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2304992183453420d4e90de9028b613a11a76200d126305bd28d57fd53791a97`  
		Last Modified: Fri, 09 Jan 2026 22:34:34 GMT  
		Size: 15.3 MB (15286645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9751b2b824d37620bf8654e4e48aefebd39eba18a0b8a5d77ab296afd91f48b`  
		Last Modified: Fri, 09 Jan 2026 22:34:33 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e077a0e24528225f56a78355523f56487320f9ffad90e13a1861ad645b9e42`  
		Last Modified: Fri, 09 Jan 2026 22:34:32 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8d590f2fa2e8196c8fa334be03021a841438c8d42b38d1c18cf0149de78d6f`  
		Last Modified: Fri, 09 Jan 2026 22:34:33 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:6aac909d67d642a0c9e9979741b9508c09b671786b1c6b52382ce0dab86d5dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64583280332f9e524f0114afb481cd5e0531830dee495edba592941a49836603`

```dockerfile
```

-	Layers:
	-	`sha256:c41030bd5ddaf763872417e6030b79df8ebdb3d257a98eb5d410316a998733c1`  
		Last Modified: Fri, 09 Jan 2026 23:57:40 GMT  
		Size: 6.9 MB (6911391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d064259f070842da076b1964d62ee583469cb8e68cb1527e8b98ccf5716c612f`  
		Last Modified: Fri, 09 Jan 2026 23:57:41 GMT  
		Size: 58.6 KB (58586 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-bookworm` - linux; mips64le

```console
$ docker pull php@sha256:41f26bb79caa8fa602e0fc780b2cee0535505d49fb9dbaf86b9257667dc29435
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157034175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:933f6074ab32e071156da0db393d4f15324ba577ac4d8bbb88ec6e4dda295d8f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:16:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:18:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:18:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:18:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:18:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:18:17 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:18:17 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:39:39 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:39:41 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:39:41 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_VERSION=8.5.1
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Mon, 29 Dec 2025 23:39:41 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Sat, 10 Jan 2026 00:03:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 10 Jan 2026 00:03:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:21:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 10 Jan 2026 00:21:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:21:10 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 10 Jan 2026 00:21:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 10 Jan 2026 00:21:10 GMT
STOPSIGNAL SIGWINCH
# Sat, 10 Jan 2026 00:21:12 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 10 Jan 2026 00:21:13 GMT
WORKDIR /var/www/html
# Sat, 10 Jan 2026 00:21:13 GMT
EXPOSE map[80/tcp:{}]
# Sat, 10 Jan 2026 00:21:13 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:f479f5e9b924c5f7ef1d8b31a2c87cbd2a63c9fdc99e9e0c0cea7eae009e308c`  
		Last Modified: Mon, 29 Dec 2025 22:38:39 GMT  
		Size: 28.5 MB (28513809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93d9cabd4aab99e194d4a41705774411b061e905a5607b5d68428e6c0fdfc3f`  
		Last Modified: Mon, 29 Dec 2025 23:38:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8fa90b950d6df8880366223e469aa2861d9bff3782a34bbbbd8c49d4d03a522`  
		Last Modified: Mon, 29 Dec 2025 23:38:16 GMT  
		Size: 80.7 MB (80670513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39959c61c1a601c13b85fe9f2c5c8646ffe26d790e73c6bfb044a1a8b6891d0e`  
		Last Modified: Mon, 29 Dec 2025 23:38:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd3e0ce24ae30c711e9419a264d4d93fce74a5c8942103ed45335be3ce91d5f`  
		Last Modified: Mon, 29 Dec 2025 23:59:39 GMT  
		Size: 20.1 MB (20077244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66299e8474ac8c18bf4447b629ee9d516ca68ec5591d0b782108643a83b38af`  
		Last Modified: Mon, 29 Dec 2025 23:59:37 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:252fef5e44ae8f0167582befd01c30b3a3ff36ecb05a852ed19c145bc6d5c389`  
		Last Modified: Mon, 29 Dec 2025 23:59:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7771a5d600fa94b56eba00848e322fb55ae10d45d23d7b95dde83f81648638`  
		Last Modified: Sat, 10 Jan 2026 00:22:09 GMT  
		Size: 14.5 MB (14453455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08649e0ba2fa94888c97f976b9434bdd5cb06effc6a04d83006cc75234836297`  
		Last Modified: Sat, 10 Jan 2026 00:22:08 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643892d100f81483aa7232b087ea501ce1e9fdf519cbdcc96c639d8c6533da64`  
		Last Modified: Sat, 10 Jan 2026 00:22:09 GMT  
		Size: 13.3 MB (13313645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8a47bd96e8addf42a64c8421a254b21f83ac341d6ed2f4334afe44012ad0f4`  
		Last Modified: Sat, 10 Jan 2026 00:26:16 GMT  
		Size: 2.5 KB (2464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1dee667373822b2b0fef95d94dc2c41c86fb9296b035bd1172050d12558f24`  
		Last Modified: Sat, 10 Jan 2026 00:22:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1723322a321c10e9f65be7fb984b82367088bf5a0cf2a1b4c6f155ad63d3ab21`  
		Last Modified: Sat, 10 Jan 2026 00:22:08 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:9a6d09e65421192070fa07006406f0c650bd16895c12c3e5961169d13ae10336
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.5 KB (58497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bab784016f2cadfb94270d75b8ca86665be4ce7a94e68a2b04d5428ee7cac7`

```dockerfile
```

-	Layers:
	-	`sha256:cd6f3a338947c8dfdc678e6a4aef435c767098d30d5e0389ff7ce3316938d81f`  
		Last Modified: Sat, 10 Jan 2026 02:55:06 GMT  
		Size: 58.5 KB (58497 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-bookworm` - linux; ppc64le

```console
$ docker pull php@sha256:4ef8aabd396248ed67a7ec49ad65bf6478b2ce53747c58f12cac3c0381f50dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.1 MB (186131185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2a49fbc49b6a8caeef96e297f3ba64a5d178c179302736c6d1ee971841eb37`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1766966400'
# Tue, 30 Dec 2025 02:15:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 30 Dec 2025 02:16:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Dec 2025 02:16:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Dec 2025 02:16:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 30 Dec 2025 02:16:51 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 30 Dec 2025 02:16:51 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Tue, 30 Dec 2025 02:18:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Tue, 30 Dec 2025 02:18:35 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Tue, 30 Dec 2025 02:18:36 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Tue, 30 Dec 2025 02:18:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 02:18:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 02:18:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Dec 2025 02:18:36 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 30 Dec 2025 02:18:36 GMT
ENV PHP_VERSION=8.5.1
# Tue, 30 Dec 2025 02:18:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Tue, 30 Dec 2025 02:18:36 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Tue, 30 Dec 2025 02:18:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 02:18:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:20:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 23:20:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:20:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 23:20:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 23:20:16 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 23:20:17 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 23:20:17 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 23:20:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 23:20:17 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:b7648f01f6858fc79caf032b4b9ed2f7e43e57f4621dc8cb36e84eb86399065b`  
		Last Modified: Tue, 30 Dec 2025 01:48:36 GMT  
		Size: 32.1 MB (32068844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee93a9966845dddb639588fdcde0ed0ecf405e81db5bf3e7b306c9cbebf976cb`  
		Last Modified: Tue, 30 Dec 2025 02:21:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1226cbc8a9cbea94e5a9e2e037754124cee088acdf931d11622ed35b2aabbfeb`  
		Last Modified: Tue, 30 Dec 2025 02:21:55 GMT  
		Size: 103.3 MB (103328995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20082871cd07652f43cb1378561dfdd8cfbf23782814ff423bbb205eeab4afae`  
		Last Modified: Tue, 30 Dec 2025 02:21:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf0e7e95c4bfe931089c745b9f0c9993308aae1138b73d194191d1bc3de333`  
		Last Modified: Tue, 30 Dec 2025 02:23:19 GMT  
		Size: 21.3 MB (21317935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ff296c8769fe763baf1673adc246dd1ece51620d816d35c54181fbae695758`  
		Last Modified: Tue, 30 Dec 2025 02:23:17 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8505b534f0278fb5de391ad84a9513e3f3121b9b564aca61a26e0f41dd1b54b`  
		Last Modified: Tue, 30 Dec 2025 02:23:17 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a66ec807fdb6c758fcd61ef8052a01c3a276492d86c767d42575ddae20dabd`  
		Last Modified: Tue, 30 Dec 2025 02:23:18 GMT  
		Size: 14.5 MB (14455055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfb02df7703d251e406e2e68d158e0aa8286878942b126d7fb06ee6e2526a8f`  
		Last Modified: Tue, 30 Dec 2025 02:23:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a890eb1fcc4121888b5f775a65f76a656f3c1b6bf1adfe2c357c20fa02305a`  
		Last Modified: Fri, 09 Jan 2026 23:20:52 GMT  
		Size: 15.0 MB (14954866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b02c8b0422e1109aeba1d6c365015fa1ace1bb37697bc4564ca24a2c7d7eec7`  
		Last Modified: Fri, 09 Jan 2026 23:20:51 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc2a7246520598fb34a9c8d7bc22fd634326457bf2a9108df352803129179e6`  
		Last Modified: Fri, 09 Jan 2026 23:20:50 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be250e34c0f400cdd91481ab5688a00f4c17d55e267fdd4ab2499ca94c47f8f9`  
		Last Modified: Fri, 09 Jan 2026 23:20:50 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:5962fc38414d463b861267ee2ef1ed51492810a840eb7a49cda582a6bca51411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6967107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5654e667b801815ecdd6f3d983dcb57bc008db3a226883eaa2c3729647b12e`

```dockerfile
```

-	Layers:
	-	`sha256:0c078667a08e38120b1348efa0e32ecd0f970be2823cb8f4e73e0da4cae6d0df`  
		Last Modified: Sat, 10 Jan 2026 00:39:45 GMT  
		Size: 6.9 MB (6908413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50d64ec68c35b9fa29f22219b9e1c81c8c09a4075b2872170dbae35e54505bcc`  
		Last Modified: Sat, 10 Jan 2026 00:39:46 GMT  
		Size: 58.7 KB (58694 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-bookworm` - linux; s390x

```console
$ docker pull php@sha256:b103f38747417ff328609dff4483369540b8eb0f40543806dda40e850e4e177b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.6 MB (155585218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91b7edf524f1b118b38b7599737e34614c8ef5bd531af1414f385c19eec76ec`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1766966400'
# Mon, 29 Dec 2025 23:24:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:24:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:24:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 29 Dec 2025 23:24:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:24:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:24:36 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Mon, 29 Dec 2025 23:24:36 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Mon, 29 Dec 2025 23:36:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Mon, 29 Dec 2025 23:36:23 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Mon, 29 Dec 2025 23:36:23 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:36:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_VERSION=8.5.1
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.1.tar.xz.asc
# Mon, 29 Dec 2025 23:36:23 GMT
ENV PHP_SHA256=3f5bf99ce81201f526d25e288eddb2cfa111d068950d1e9a869530054ff98815
# Fri, 09 Jan 2026 22:49:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 09 Jan 2026 22:49:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:53:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 09 Jan 2026 22:53:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:53:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 09 Jan 2026 22:53:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jan 2026 22:53:50 GMT
STOPSIGNAL SIGWINCH
# Fri, 09 Jan 2026 22:53:50 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 09 Jan 2026 22:53:50 GMT
WORKDIR /var/www/html
# Fri, 09 Jan 2026 22:53:50 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 22:53:50 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:908a8b9619550bcbaa302a1a1375bffd68fb4bab6330d7a965b0b9e3f3896a0a`  
		Last Modified: Mon, 29 Dec 2025 22:25:40 GMT  
		Size: 26.9 MB (26884397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03eb418c0e5abcefe16acbc6e83182df41a4844e89a661b7628f7b0852127c87`  
		Last Modified: Mon, 29 Dec 2025 23:28:40 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbed6618c1961e2a7b7cf2c87e46f37dd87a16548388c42e37807bf2ce70d12`  
		Last Modified: Mon, 29 Dec 2025 23:28:46 GMT  
		Size: 80.8 MB (80826406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bdd0c0b33812eb4b7f25ae54473174aebd54cf322e1c27b866650bf4f1c6dc`  
		Last Modified: Mon, 29 Dec 2025 23:28:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222bc849e1b19371c05dc68d739ed0f184d73bbb8532c19f810ba988bef7b2ab`  
		Last Modified: Mon, 29 Dec 2025 23:40:12 GMT  
		Size: 19.9 MB (19909960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89757ebcdcc864a57a0e2a372eb3540fbd9b10f5a4de7457f350eaeae6a38b35`  
		Last Modified: Mon, 29 Dec 2025 23:40:10 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd1a00aff1b003f8f4201db4bbce376688e04da2e77809b06123ea3d73eaf17`  
		Last Modified: Mon, 29 Dec 2025 23:40:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20ace7a556f1d6f26a1c0e4387c3091a4c25fbdcd0c340bd818293ae7f78f7af`  
		Last Modified: Fri, 09 Jan 2026 22:54:15 GMT  
		Size: 14.5 MB (14453974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3b1081830c1488d6c3fb4249f9c6a28c048c64ed2eecb2144e32e58ab3a21a`  
		Last Modified: Fri, 09 Jan 2026 22:54:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e88846d9a4bd6a95ed1dbe48b9f42b1cdb17163aa6baf97c88f26b72a1a14e7`  
		Last Modified: Fri, 09 Jan 2026 22:54:16 GMT  
		Size: 13.5 MB (13504988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8cde42fbd8f743863ea6604068399ed2a03bbe6e71ee08341259c0337ab4d9`  
		Last Modified: Fri, 09 Jan 2026 22:54:14 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a5f093bb0353200a7929536be55af68b0600b9b18070e83aef2bb2049f4d908`  
		Last Modified: Fri, 09 Jan 2026 22:54:14 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d4b0d5a52ffdbcfd11f8cb537fbb31aab0ef0b3f68bac24a858190f9e83101`  
		Last Modified: Fri, 09 Jan 2026 22:54:14 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-bookworm` - unknown; unknown

```console
$ docker pull php@sha256:d326057d9116b3c1e8b28f2bf762d9c0fb2ec508af4a4c53be839fa7810c2088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6827461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373711cc4b89a8342042eff7129e1cccc324e6126a79b6ee5044a4c30500bfd8`

```dockerfile
```

-	Layers:
	-	`sha256:407301af298b25c655d8d25f9e7de363391a0b82efe3d04c912303fd8a7dd327`  
		Last Modified: Fri, 09 Jan 2026 23:58:12 GMT  
		Size: 6.8 MB (6768839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7250cd974e97f43d68f25548c8f64e354f2d33369a62d26d764bb7d373bab62`  
		Last Modified: Fri, 09 Jan 2026 23:58:13 GMT  
		Size: 58.6 KB (58622 bytes)  
		MIME: application/vnd.in-toto+json
