## `php:8-apache-trixie`

```console
$ docker pull php@sha256:29e2adeb12afa8f76bdb79c580380d4f87511ef33116d5966503393853659dcb
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

### `php:8-apache-trixie` - linux; amd64

```console
$ docker pull php@sha256:42851490fc4015f97b135ab9250c8caf4d78d87f1ad705c9c897d950977b8694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.3 MB (181343532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14f864620611e621357a2fe76ba195c5b65718e5f5b1f3b874abc9ac55da9efd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 18:28:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 13 Feb 2026 18:28:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 13 Feb 2026 18:28:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 18:28:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:28:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:28:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 13 Feb 2026 18:28:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 13 Feb 2026 18:28:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 13 Feb 2026 18:28:49 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 13 Feb 2026 18:28:49 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 13 Feb 2026 18:28:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:28:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:28:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:28:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 13 Feb 2026 18:28:49 GMT
ENV PHP_VERSION=8.5.3
# Fri, 13 Feb 2026 18:28:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Fri, 13 Feb 2026 18:28:49 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:28:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:28:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:31:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:31:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:31:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:31:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:31:54 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:31:54 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:31:54 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:31:54 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:31:54 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:0c8d55a45c0dc58de60579b9cc5b708de9e7957f4591fc7de941b67c7e245da0`  
		Last Modified: Tue, 03 Feb 2026 01:15:17 GMT  
		Size: 29.8 MB (29778596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534db4ee1a14bcf59d6c6369624886833b1ca59c73b18b1d2be4d750e056a904`  
		Last Modified: Fri, 13 Feb 2026 18:32:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28bcd246e78ff644dab9ee9db5a1ded9ecba8694c61fbe6da136d2d42a39619`  
		Last Modified: Fri, 13 Feb 2026 18:32:18 GMT  
		Size: 117.8 MB (117839521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea437830ee509c510b34f9ce86d5657c08d3cfce9a86e1a3f76331d3313d634`  
		Last Modified: Fri, 13 Feb 2026 18:32:15 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:062e8a687151da37c39c145b047de9655e1625aefe04367ca19230313f3ddc46`  
		Last Modified: Fri, 13 Feb 2026 18:32:16 GMT  
		Size: 4.2 MB (4226889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6884d67fe6e42f748e6322a3e5673a8b39cb63720d417ce04422d7cb6d4d9fc`  
		Last Modified: Fri, 13 Feb 2026 18:32:16 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4062cec7618c70cc90563dd8a5b4cc84fc2f0750123309fa4e2b896f780e1c68`  
		Last Modified: Fri, 13 Feb 2026 18:32:17 GMT  
		Size: 479.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c9c13c7604505e377e89967df3927640b5eb0301ea35d92151c794643b24e5`  
		Last Modified: Fri, 13 Feb 2026 18:32:18 GMT  
		Size: 14.5 MB (14499816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95367a6866e3b7a8c22c9564ef8324cccdcd363b5a134477fd3d55e55064fb82`  
		Last Modified: Fri, 13 Feb 2026 18:32:18 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da0762def83025882bab8acae1e72bd1a1a6ce8310cd6ee7ec4704967a3b4f7`  
		Last Modified: Fri, 13 Feb 2026 18:32:18 GMT  
		Size: 15.0 MB (14993230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb7686b39275805eb9e6fd8a04d35275168c317cff027fda49c0119ca7d18c4`  
		Last Modified: Fri, 13 Feb 2026 18:32:19 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1adfae2d487c52cf2d63d82fb60d24cc3c7b25f9ca724fe38753fb7bf23515c`  
		Last Modified: Fri, 13 Feb 2026 18:32:19 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c17746b88d67aa0a10036d349c18c96cb8c239f66db37d202ef2cdbe52ba22e`  
		Last Modified: Fri, 13 Feb 2026 18:32:19 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-trixie` - unknown; unknown

```console
$ docker pull php@sha256:373eeb9c772419c3f32c3e08ba5da2899b5394a1cf79d1a9947d0f4409ef6e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7272829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4259b2331649c3ab5ab24aa2e858ef3cb4bcfc62399ff45bedce0a558eafc3`

```dockerfile
```

-	Layers:
	-	`sha256:305e920ddd774e49a0601383a31af32b318a535101a56240d4570a1b8cab8912`  
		Last Modified: Fri, 13 Feb 2026 18:32:16 GMT  
		Size: 7.2 MB (7213125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a09216f06a1b8054255404ccca5aa4d9391c90214854726df9c4c72f4b8232d`  
		Last Modified: Fri, 13 Feb 2026 18:32:15 GMT  
		Size: 59.7 KB (59704 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-trixie` - linux; arm variant v5

```console
$ docker pull php@sha256:0f401e9b4b9e7ad7e50624eca7bc7d71af94ded5190f4d8bcb8f65f2a94a749f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154527200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b635d969f04d4f7112612f641eac7bbb54f535326ad0a9792c594b69ab08c797`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 18:42:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 13 Feb 2026 18:42:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 13 Feb 2026 18:42:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 18:42:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:42:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:42:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 13 Feb 2026 18:42:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 13 Feb 2026 18:42:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 13 Feb 2026 18:42:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 13 Feb 2026 18:42:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 13 Feb 2026 18:42:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:42:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:42:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:42:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 13 Feb 2026 18:42:43 GMT
ENV PHP_VERSION=8.5.3
# Fri, 13 Feb 2026 18:42:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Fri, 13 Feb 2026 18:42:43 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:42:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:42:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:46:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:46:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:46:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:46:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:46:19 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:46:19 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:46:19 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:46:19 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:46:19 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:2a2986ba48ae233640829460f6772db2ffbc330d97d2b29a533694dfdc7dc893`  
		Last Modified: Tue, 03 Feb 2026 01:14:07 GMT  
		Size: 27.9 MB (27947555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f1179856b0842b075da7ec39221145247ed0f73e21cc35de6c0c84235d7889`  
		Last Modified: Fri, 13 Feb 2026 18:46:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d4c089a5b570fd623b9aadddec50e5b409ce5606973a088a04863e2b10baf2`  
		Last Modified: Fri, 13 Feb 2026 18:46:40 GMT  
		Size: 94.9 MB (94876512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0bb4d6a239f93efb8a298b47a96ce660ed32ba42ef39444cccb13a50b17c89`  
		Last Modified: Fri, 13 Feb 2026 18:46:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07c3a44c4d9cef75ce1c3e26806fc349c02f3d1bd395c702ce6b79121fb55c6`  
		Last Modified: Fri, 13 Feb 2026 18:46:38 GMT  
		Size: 4.1 MB (4088772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a763211cc917caf85be68d49639414865392b8f3655dbfd98989a0454c12d607`  
		Last Modified: Fri, 13 Feb 2026 18:46:39 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31a8ae88e59efc7b1dc6f37375fb25d2bdcc369b847be9097ebad3929c61ba3`  
		Last Modified: Fri, 13 Feb 2026 18:46:39 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e99f110cba9c17dd0fa6127aa532fd848895ca9402e702e2d60a09b66016e24`  
		Last Modified: Fri, 13 Feb 2026 18:46:40 GMT  
		Size: 14.5 MB (14497078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82c3cdc7684692380c9d478b641a8dff2b8ff89dbc4951d06deba75833c07a4`  
		Last Modified: Fri, 13 Feb 2026 18:46:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0808baffdec0a9112f38e3e1ee950c84813ab294b566c3de2a740ea8792a63`  
		Last Modified: Fri, 13 Feb 2026 18:46:41 GMT  
		Size: 13.1 MB (13111791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea9f288d66b095430eaee561ce65348ab270f90a5ec1ef0aeaf5cdbb044e703`  
		Last Modified: Fri, 13 Feb 2026 18:46:41 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688a8e9b2b29c885b9d09b9365b46f436070661438387a6c859be9a9c3f39e97`  
		Last Modified: Fri, 13 Feb 2026 18:46:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab71728678324a820e6dad0187946329c5c0e38625dd6a20761ad869645d2e9c`  
		Last Modified: Fri, 13 Feb 2026 18:46:42 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-trixie` - unknown; unknown

```console
$ docker pull php@sha256:7ffc280861772eea84fd521e3c97a5ecb1aaf3fb9421afbf6fc9cf4c413e644d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7072895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e34145ed0db47a36977baff0576b6aac31a770a4b18c2fa1acc72d2695d22434`

```dockerfile
```

-	Layers:
	-	`sha256:a4621ce9dd96ae2ed6cd20ee8d7f3231bc660f66b8e86bc334befa3379c2acbb`  
		Last Modified: Fri, 13 Feb 2026 18:46:39 GMT  
		Size: 7.0 MB (7012987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dcb3de6b69bcc7b597c48f884d085ee68dc86c54eb65bb496d4d3dcfda694a5`  
		Last Modified: Fri, 13 Feb 2026 18:46:38 GMT  
		Size: 59.9 KB (59908 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-trixie` - linux; arm variant v7

```console
$ docker pull php@sha256:121d2e7e8a3806688187ed6079028500667a477875a2cdf44c916b1466e8f943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143216821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65b1711477bf76308497bf36ee9b3e40b67e0c38d150688e028d7f80371acee`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 18:28:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 13 Feb 2026 18:28:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 13 Feb 2026 18:28:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 18:28:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:28:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:28:18 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 13 Feb 2026 18:28:18 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 13 Feb 2026 18:28:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 13 Feb 2026 18:28:26 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 13 Feb 2026 18:28:26 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 13 Feb 2026 18:28:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:28:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:28:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:28:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 13 Feb 2026 18:28:26 GMT
ENV PHP_VERSION=8.5.3
# Fri, 13 Feb 2026 18:28:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Fri, 13 Feb 2026 18:28:26 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:28:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:28:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:31:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:31:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:31:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:31:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:31:34 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:31:34 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:31:34 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:31:34 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:31:34 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:abdd0f3062e6238c89a40b3e40277debcba2796d6736373219a089086718b8b4`  
		Last Modified: Tue, 03 Feb 2026 01:14:48 GMT  
		Size: 26.2 MB (26213748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25dc7395d2a6b8f04a68406616ae0a0d4020ef7cfee43f0c460b4ba3056edbfa`  
		Last Modified: Fri, 13 Feb 2026 18:31:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5990638f8eadc06aedf16f6f4f596394190ec95cf946125a1b4c2d3aa7e7b4a`  
		Last Modified: Fri, 13 Feb 2026 18:31:53 GMT  
		Size: 86.2 MB (86244741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132706703a6deb6b16806d6605640b129322481f1385677d0e751e8537eb7319`  
		Last Modified: Fri, 13 Feb 2026 18:31:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48be50cf90db9451fc94c5967c67fb0c3ce0dbedcac4a0a225256a17f5ac359e`  
		Last Modified: Fri, 13 Feb 2026 18:31:51 GMT  
		Size: 3.8 MB (3757596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fd3510cdbfca392c9010991e39ded864b4497aa9c8e33fcf1017336212f316`  
		Last Modified: Fri, 13 Feb 2026 18:31:52 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac93361d4b6556306d068e3d93f75d1d1a01bc0195bd96f997ae37061b7e1fe2`  
		Last Modified: Fri, 13 Feb 2026 18:31:52 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a671f134239555dbedc6a6bb608250dcd68bf16887d117627c43676bfd6ffe1f`  
		Last Modified: Fri, 13 Feb 2026 18:31:53 GMT  
		Size: 14.5 MB (14497213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e098582b8b440dd69120d36236c67637dbe6446f8dc4871ea45583cd192d2d`  
		Last Modified: Fri, 13 Feb 2026 18:31:53 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb74642e6268111f1c75de4326dea10cdc5e8a7d3189a6076d9e37ee2ae7ab8`  
		Last Modified: Fri, 13 Feb 2026 18:31:54 GMT  
		Size: 12.5 MB (12498029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c67abe9b766226d0968240327a2b90773bf6ed94c3b328ae6c4cca34d37445`  
		Last Modified: Fri, 13 Feb 2026 18:31:55 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab2d6d297b867f1bce05d99388d51a7fac7f4e7774e55868cdea6e2b4cccae6`  
		Last Modified: Fri, 13 Feb 2026 18:31:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947378874dc5b4c7becedf718c4c0df7c408560af4867e331940d3b919faa220`  
		Last Modified: Fri, 13 Feb 2026 18:31:55 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-trixie` - unknown; unknown

```console
$ docker pull php@sha256:45245c4ff156cdabc44262e58caf72b1bdfd732376c9a9bfe84f736393f8c000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7076892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c291e120364e7f607d9431fde94b7bf9201c8bf4fd057b82d4e1b9ace20cfcc8`

```dockerfile
```

-	Layers:
	-	`sha256:f812baacd3503a6506e71c368d244a1dbf6f576c8cb65c1eaf6a6ea5953a6b5d`  
		Last Modified: Fri, 13 Feb 2026 18:31:51 GMT  
		Size: 7.0 MB (7016985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa77f707acc69506925f80cd176c6cb7c2c92df8c4646082544a42c793709913`  
		Last Modified: Fri, 13 Feb 2026 18:31:51 GMT  
		Size: 59.9 KB (59907 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-trixie` - linux; arm64 variant v8

```console
$ docker pull php@sha256:ba33b072175ab4fd03677738832f682ada4a9e338b1626a3de9ebd29bc65afeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.7 MB (173677015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcb796868fbbd55b22c3c999de1f022db72af70b6a8b0504b15a14b66c1ddb97`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 18:29:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 13 Feb 2026 18:29:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 13 Feb 2026 18:29:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 18:29:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:29:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:29:31 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 13 Feb 2026 18:29:31 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 13 Feb 2026 18:29:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 13 Feb 2026 18:29:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 13 Feb 2026 18:29:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 13 Feb 2026 18:29:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:29:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:29:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:29:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 13 Feb 2026 18:29:38 GMT
ENV PHP_VERSION=8.5.3
# Fri, 13 Feb 2026 18:29:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Fri, 13 Feb 2026 18:29:38 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:29:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:29:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:33:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:33:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:33:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:33:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:33:03 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:33:03 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:33:03 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:33:03 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:33:03 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595f9fa5c523f2ba65cf31ecf978c49dbea57883392f3e9ef2f37112b7c961be`  
		Last Modified: Fri, 13 Feb 2026 18:33:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef1d7c0255a41e5c76f38d9c0e7b09b421519a0b8147b3ca6d258296dba53a6`  
		Last Modified: Fri, 13 Feb 2026 18:33:27 GMT  
		Size: 110.2 MB (110165016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdeb9f9c963f004dcfd7f3a1b0348f4602463b5b98fdb29cbc4fbe479fa6c99`  
		Last Modified: Fri, 13 Feb 2026 18:33:10 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:280cf079dc752fff2045adc7327e4ca9e143b754c0d6e94d8d21a8652b390502`  
		Last Modified: Fri, 13 Feb 2026 18:33:25 GMT  
		Size: 4.3 MB (4304876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025d8a69347e3b9cf1564651d7a40df1eb6b0e427c9efd65ba93340eb39aeda0`  
		Last Modified: Fri, 13 Feb 2026 18:33:24 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb8f8581a79e2798b88d5fc072de06160ffaba77292fe5d163c096b46f67b42`  
		Last Modified: Fri, 13 Feb 2026 18:33:25 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc096120762dac131f50ba08f94258d74179cf1cf5b3126968f9707eb5c4bd01`  
		Last Modified: Fri, 13 Feb 2026 18:33:26 GMT  
		Size: 14.5 MB (14499129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a71e6f1cd063e0a10322e1508bb1a990590a5bc14833b0dcf40547851e54dc`  
		Last Modified: Fri, 13 Feb 2026 18:33:26 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b03e80ecaf9e894db34c5e88c1db586543da6e7f6014bdd3d9a7136aa539b9`  
		Last Modified: Fri, 13 Feb 2026 18:33:27 GMT  
		Size: 14.6 MB (14562436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0c35da39ac3662bc9fc028d02b893493585fc58c119c2d8025ed19ab7f96475`  
		Last Modified: Fri, 13 Feb 2026 18:33:27 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03a27eaf6038717f80388f24e50f4d98a4a7ac779d5ac2d2ae9f2a3bdc7dc075`  
		Last Modified: Fri, 13 Feb 2026 18:33:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5335ae8078d14015ae5926741ef931ebcf191b91182e0c3e5ed7d1387b652f80`  
		Last Modified: Fri, 13 Feb 2026 18:33:28 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-trixie` - unknown; unknown

```console
$ docker pull php@sha256:b4f5b7b042884874de30bf9339052cdbb6aa7c7523204fcf7267bb3b3e47c048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7370444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a57990209e56413714c73ec7f99462ce962abf1461329f7bdd4e42df099a3f2`

```dockerfile
```

-	Layers:
	-	`sha256:6621a20afa99bba259fb5fadf0aba3869d7c42acdced31bb85ec5775ac1b995d`  
		Last Modified: Fri, 13 Feb 2026 18:33:25 GMT  
		Size: 7.3 MB (7310468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c157b5468d973b66bea0bac23dd4a69a61841d258b16c8b081b0e3da56a4bf30`  
		Last Modified: Fri, 13 Feb 2026 18:33:24 GMT  
		Size: 60.0 KB (59976 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-trixie` - linux; 386

```console
$ docker pull php@sha256:1e8cc273d717704c52dfc32b798aee168515f9b5b7473c3a08a1f12f75f9b65e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.7 MB (181737960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228322aa7d6f5cd7dcfaf2b4403010f7f8205a922a263b85557e94a13a5ce6de`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Fri, 13 Feb 2026 18:29:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 13 Feb 2026 18:29:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 13 Feb 2026 18:29:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 13 Feb 2026 18:29:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 13 Feb 2026 18:29:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 13 Feb 2026 18:29:34 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 13 Feb 2026 18:29:34 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 13 Feb 2026 18:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 13 Feb 2026 18:29:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 13 Feb 2026 18:29:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 13 Feb 2026 18:29:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:29:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:29:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:29:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 13 Feb 2026 18:29:40 GMT
ENV PHP_VERSION=8.5.3
# Fri, 13 Feb 2026 18:29:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Fri, 13 Feb 2026 18:29:40 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:29:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:29:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:32:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:32:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:32:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:32:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:32:48 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:32:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:32:48 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:32:48 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:32:48 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5038e7975f5dbd258f0c4de30f7649fb57c0948a38c3d5768b4da61a77af0032`  
		Last Modified: Fri, 13 Feb 2026 18:33:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0920a0260ebc76eb96fbdf27e1e4d695f0f71625d785e10f22dab971aba062`  
		Last Modified: Fri, 13 Feb 2026 18:33:15 GMT  
		Size: 116.1 MB (116139504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e9fd8262543582402ce1c3d48447c34fd6ce8da5863bd84ba700bd886ec9a4d`  
		Last Modified: Fri, 13 Feb 2026 18:33:07 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa62827d031d195b1be2ba3b1521ba53e1be7c69c3e26ae9a524a929bfa8628`  
		Last Modified: Fri, 13 Feb 2026 18:33:07 GMT  
		Size: 4.5 MB (4458293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920708bbc6ce11e175d2a9047517233967398bc0419d953592319267d11ecc82`  
		Last Modified: Fri, 13 Feb 2026 18:33:08 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b16eeac3b68e220733b2234afa1ae611120ceb47b44877009813c0978bb576f`  
		Last Modified: Fri, 13 Feb 2026 18:33:08 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3084abb5b08185aa6bcb7d8ed150c455caf4b807871629826372ecc25a1786f8`  
		Last Modified: Fri, 13 Feb 2026 18:33:09 GMT  
		Size: 14.5 MB (14498598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef74dd681415588047a801a082ca2952f693df66bf6da870b3ff5ad04f593b42`  
		Last Modified: Fri, 13 Feb 2026 18:33:09 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54ad46fb5d0c318d74df88cacc3f53853c9042fd24cbfec7f8030f51a773469`  
		Last Modified: Fri, 13 Feb 2026 18:33:10 GMT  
		Size: 15.3 MB (15342221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9ab7f9641e2fe554774294db71cc7f5ce46481bc5d0538e81bd1c27ddc514d`  
		Last Modified: Fri, 13 Feb 2026 18:33:10 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05305537ad631b92996f53afa2ab1026a6b1626efbf7deb66de147f65b4b76de`  
		Last Modified: Fri, 13 Feb 2026 18:33:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916c4a693112233b4c1d2ecc603a1a18f6ebf7c42a031311230ae0128daf8f5a`  
		Last Modified: Fri, 13 Feb 2026 18:33:12 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-trixie` - unknown; unknown

```console
$ docker pull php@sha256:1e4249dde72c104177026e444cfbdd9396cd967785313269704fbd2219a5b321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7246607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4757c8809644f3cd8be771213ea7e9370eaa96435a2b5b054bf4e9edaf924952`

```dockerfile
```

-	Layers:
	-	`sha256:7540255bd4b222f706f92cdb3c33d351f2e745e0ceeac25755e7ea96a9be5251`  
		Last Modified: Fri, 13 Feb 2026 18:33:07 GMT  
		Size: 7.2 MB (7186971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efd92b3c34596d7fb19183d1340300deceb3a8c58eff7db4c806a7bfc3571be5`  
		Last Modified: Fri, 13 Feb 2026 18:33:07 GMT  
		Size: 59.6 KB (59636 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-trixie` - linux; ppc64le

```console
$ docker pull php@sha256:f60029bdd170f219fa6160d0c05fd8e019987e06243298d1c56b0877ae881fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177583420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b457a957db7f3b8b627dd5a482ae11b37f444537e2ec0f9476983532d3705cb`
-	Entrypoint: `["docker-php-entrypoint"]`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_VERSION=8.5.3
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 03 Feb 2026 02:48:44 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:52:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:52:26 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:58:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:58:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:58:26 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:58:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:58:26 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:58:27 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:58:27 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:58:27 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:58:27 GMT
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
	-	`sha256:dbc574d3b8ba422c4d5f96b41738d0e06931790cfb9bd195dfa6db0663a47b88`  
		Last Modified: Fri, 13 Feb 2026 18:58:58 GMT  
		Size: 14.5 MB (14514461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344fe9bbecbda240ba480c8a42053c671ddf1e0682432933aa1abfb620959ca0`  
		Last Modified: Fri, 13 Feb 2026 18:58:20 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59d1601451b89978be52a445035cb0a54adf429c794cbf69004f364884fce47`  
		Last Modified: Fri, 13 Feb 2026 18:58:58 GMT  
		Size: 15.0 MB (14984656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa482acd178d2f9e5576faa5a27c544ea9ed0e8862c62dd869d41b359422b0d2`  
		Last Modified: Fri, 13 Feb 2026 18:58:57 GMT  
		Size: 2.5 KB (2463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686e9c0037ff1f57e1a847ab36648eb318b266b0f5177abf6cd25115e5beaa73`  
		Last Modified: Fri, 13 Feb 2026 18:58:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a0e5208af9c82d162891798b50196b53dcb7570c3a81a8f56797a08430fda8`  
		Last Modified: Fri, 13 Feb 2026 18:58:58 GMT  
		Size: 895.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-trixie` - unknown; unknown

```console
$ docker pull php@sha256:a92a742eaefd71be71e20f4eba2f3368e7056ac9906e447a98073a9d2cfd07ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7272699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b741d60081d1144609850423170b198b1cb3ba587b1df9068d5a13ed0564cc9`

```dockerfile
```

-	Layers:
	-	`sha256:e2fb3e437766646c991914941fd54494b03219cf1a1a319c8fd99d7ccee78ab2`  
		Last Modified: Fri, 13 Feb 2026 18:58:57 GMT  
		Size: 7.2 MB (7212911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26da3147e4db654c78abdc0e78aab3ebcf5434ef1206b50d4fa7b5a2f11e3bce`  
		Last Modified: Fri, 13 Feb 2026 18:58:57 GMT  
		Size: 59.8 KB (59788 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-trixie` - linux; riscv64

```console
$ docker pull php@sha256:72e00484b87a5b53033c88098421bb90c8ba4f14ac65581c64d4b754fd08fdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.3 MB (207333478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5822d5fb53e401df729ac7d862e10a5866e32f7727242f267b4c1e68a4d923c1`
-	Entrypoint: `["docker-php-entrypoint"]`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_VERSION=8.5.3
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Tue, 03 Feb 2026 18:15:48 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 19:08:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 19:08:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:04:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 20:04:47 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:04:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 20:04:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 20:04:47 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 20:04:48 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 20:04:48 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 20:04:48 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 20:04:48 GMT
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
	-	`sha256:f7cc8252a1cf4c391cf93ab67c8e431bd9d79ff17a96bb6ced189d81d614d390`  
		Last Modified: Fri, 13 Feb 2026 20:08:02 GMT  
		Size: 14.5 MB (14514413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66ada2524556038faf30c8a0471d30898e12ab3807bad5e4cd04156c6069f22`  
		Last Modified: Fri, 13 Feb 2026 20:07:58 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df3b66ba9bcda7ede006592fcdcb3fd319cb34b6f5a35654e417c0806c29e51`  
		Last Modified: Fri, 13 Feb 2026 20:08:03 GMT  
		Size: 13.9 MB (13927433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd80899af7730f880612f365e645027a2615cace1f1ed4c194198d19eac5e2f6`  
		Last Modified: Fri, 13 Feb 2026 20:07:58 GMT  
		Size: 2.5 KB (2465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21962b00b28715762f9d0a6d7846ca3db2db11df512c9ace7857af39560c8911`  
		Last Modified: Fri, 13 Feb 2026 20:08:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560d346c227ecca3acf5499e9552bd8d2483197b687cd849380571937495ee57`  
		Last Modified: Fri, 13 Feb 2026 20:08:00 GMT  
		Size: 897.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-trixie` - unknown; unknown

```console
$ docker pull php@sha256:52fb07f016a6cff32cf961eadef49030fc6a53e4322fa0b0c92a17d0e7134a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7344721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea15aa59d498cb415f50626311c9d59d270427edc11b7fb3db2bddab252637e`

```dockerfile
```

-	Layers:
	-	`sha256:7e035935016b3518795a237c4aec9a6fa929d8abd1e5aaef23cd75559a9c4587`  
		Last Modified: Fri, 13 Feb 2026 20:08:00 GMT  
		Size: 7.3 MB (7284936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4982405de699e3f1a2f1b60c53c9f39e2b791be7a569c6e95637fbade93b5397`  
		Last Modified: Fri, 13 Feb 2026 20:07:58 GMT  
		Size: 59.8 KB (59785 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-apache-trixie` - linux; s390x

```console
$ docker pull php@sha256:c9fd390388fe7297aadd1278aea5a298eeaac6e4288868e28c236b720860fbc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155537387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe17c55d6457f008910c661d84fb02c4218a540945abd2039344110917ded73`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:21:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 03 Feb 2026 02:21:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 03 Feb 2026 02:21:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 03 Feb 2026 02:21:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 03 Feb 2026 02:21:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 03 Feb 2026 02:21:58 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Tue, 03 Feb 2026 02:21:58 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 13 Feb 2026 18:31:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	apt-get dist-clean; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 13 Feb 2026 18:31:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 13 Feb 2026 18:31:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 13 Feb 2026 18:31:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:31:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 13 Feb 2026 18:31:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 13 Feb 2026 18:31:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 13 Feb 2026 18:31:40 GMT
ENV PHP_VERSION=8.5.3
# Fri, 13 Feb 2026 18:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.3.tar.xz.asc
# Fri, 13 Feb 2026 18:31:40 GMT
ENV PHP_SHA256=ce65725b8af07356b69a6046d21487040b11f2acfde786de38b2bfb712c36eb9
# Fri, 13 Feb 2026 18:31:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 13 Feb 2026 18:31:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:37:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Feb 2026 18:37:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:37:08 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Feb 2026 18:37:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Feb 2026 18:37:08 GMT
STOPSIGNAL SIGWINCH
# Fri, 13 Feb 2026 18:37:08 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 13 Feb 2026 18:37:08 GMT
WORKDIR /var/www/html
# Fri, 13 Feb 2026 18:37:08 GMT
EXPOSE map[80/tcp:{}]
# Fri, 13 Feb 2026 18:37:08 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:809310277795fa02ff585c83bc37c8fb5e06066ee7e053bab5d08bf186beeae9`  
		Last Modified: Tue, 03 Feb 2026 01:14:11 GMT  
		Size: 29.8 MB (29838149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7e198ceab28d440d37bc9b2389ec84e5069402425c16e365d75cd20da313ea`  
		Last Modified: Tue, 03 Feb 2026 02:25:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfce049a7f31ebe3bbbea4249b3c047493e29ee727178adf1abbcf363d500955`  
		Last Modified: Tue, 03 Feb 2026 02:25:36 GMT  
		Size: 92.6 MB (92567679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e74625cb46a02aab18b786df1acf328a052bc24afe5610ef71d2e912d1f36a`  
		Last Modified: Tue, 03 Feb 2026 02:25:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6c634113997c920116b668b0a325ab33a614ba603f3da0a7d24167e0295bba`  
		Last Modified: Fri, 13 Feb 2026 18:37:28 GMT  
		Size: 4.3 MB (4344215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4f47a37b46899e07e3275585925c37bfa61c253000b31c7d280d5c560890ce`  
		Last Modified: Fri, 13 Feb 2026 18:37:27 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94696e159f89c229bb3ebe5b3401a23e0354515a54d90a73bf2c71ee77b60d98`  
		Last Modified: Fri, 13 Feb 2026 18:37:27 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485543fa3476607bf4c376fa9158ed4816adbaad4ae80ac61ae70e7534a99e2f`  
		Last Modified: Fri, 13 Feb 2026 18:37:28 GMT  
		Size: 14.5 MB (14498071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127df3760d839c53942e6fb0a8872c56ffb953bb41382df04611d0df641e979f`  
		Last Modified: Fri, 13 Feb 2026 18:37:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f74405e085ac12b2682e2921d7f066641b38b2af1d7b899888ffde67a26842e`  
		Last Modified: Fri, 13 Feb 2026 18:37:29 GMT  
		Size: 14.3 MB (14283776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab799490b175d7618bf85c454a42afc16c272be3eb4893cb35fa09d355675e2`  
		Last Modified: Fri, 13 Feb 2026 18:37:29 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68cb4627762668827a54f1f2e8d5e1fe105e53d904ea794835f6da9f5d5ee123`  
		Last Modified: Fri, 13 Feb 2026 18:37:29 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eeaac5bf1c875a86959430faf65e2021e024998127911054e6af3443b3313744`  
		Last Modified: Fri, 13 Feb 2026 18:37:29 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-apache-trixie` - unknown; unknown

```console
$ docker pull php@sha256:1fcb944294023ef62017e7ead0279f243285d907ba5953e1429439861db26515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7090074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:345dc7e6f1a173529f7f2497a366a3e6aadd3a29f07428f7349d023d89dd623c`

```dockerfile
```

-	Layers:
	-	`sha256:85b213a37ed29bcf60800a3b25fb2a1d23708becbfa3e6a3271a09d9d07fb3a8`  
		Last Modified: Fri, 13 Feb 2026 18:37:27 GMT  
		Size: 7.0 MB (7030382 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62a96fb22ff6e51bee96ec1e2c0dd681129eb22e9571775bb0fa5b22ea522f6c`  
		Last Modified: Fri, 13 Feb 2026 18:37:27 GMT  
		Size: 59.7 KB (59692 bytes)  
		MIME: application/vnd.in-toto+json
