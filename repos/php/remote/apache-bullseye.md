## `php:apache-bullseye`

```console
$ docker pull php@sha256:5047cc5245ab825d473cf5b63506b3adf169a1031ebee4946affb65643512a57
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `php:apache-bullseye` - linux; amd64

```console
$ docker pull php@sha256:f52df2ad1e3233d5615100ce0553d3b5f9d78c30e4ac0b54e8f685bbfcc129f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.6 MB (168562882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:026d708086adba4263e6f6d01ba43bfb9fe2b0ab1ae258b25d4e724365a8403b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Feb 2025 21:31:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Feb 2025 21:31:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
WORKDIR /var/www/html
# Thu, 13 Feb 2025 21:31:38 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9795d1a946c98a5a2d27d2e69e05938539fea24b15b933818b0172298ad692c4`  
		Last Modified: Fri, 14 Feb 2025 02:32:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d1dd15bb69194906223febf1afab4f742324bda0649b7c949437e730d7e6c8`  
		Last Modified: Fri, 14 Feb 2025 02:32:27 GMT  
		Size: 91.4 MB (91448540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb0be92f44968b433827ed6c0dbef0971647e1f1cc9aba464914074b34d3025`  
		Last Modified: Fri, 14 Feb 2025 02:32:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8200935932ed7e0e56f157da3f6017e427d0c0f0938dcf729329354dcee7387`  
		Last Modified: Fri, 14 Feb 2025 02:32:26 GMT  
		Size: 19.1 MB (19064356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad973efeab025209df5470bb2334743b7c57747435a96c1103af043879c9b44`  
		Last Modified: Fri, 14 Feb 2025 02:32:25 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8921cb9cbf79be8570de65e94e4f295c0c5b8b8b224d9aeb4e97a77fdf43af31`  
		Last Modified: Fri, 14 Feb 2025 02:32:26 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e1d272d8a51006e261a1f543ca7911bdc5abc6d74c85f898c8c1ede3b622ff`  
		Last Modified: Fri, 14 Feb 2025 02:32:27 GMT  
		Size: 13.7 MB (13714026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4c8d12ce931ad0f9f2504ca4cd1884cd776927c317c50a46bd210e72c2b806`  
		Last Modified: Fri, 14 Feb 2025 02:32:27 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78340113c4057cb8ea9ca2887f2c9a1b4624ccd64526b05f2e2d515bd024a34e`  
		Last Modified: Fri, 14 Feb 2025 02:32:28 GMT  
		Size: 14.1 MB (14077905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f5e2bc2a9447f764a7bfa280f9f4728ff2867336a56bcfa33a3340a781024b`  
		Last Modified: Fri, 14 Feb 2025 02:32:28 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3485b3ef6ce150ab7ee843f5bc145459a876e7456014a2c72dbfd2058e026488`  
		Last Modified: Fri, 14 Feb 2025 02:32:28 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754f792937986be4f6f2a52bd79cd3be6766583d2a1c3abb2a1a2426ea2365f8`  
		Last Modified: Fri, 14 Feb 2025 02:32:29 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:fb615c402fedf3e9000250f7831e62004c611346a82cb776c6174c1107ff5349
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6978758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e28a8c14b322d06144cdf4a4af637b14113bb5251803f4529134966829bd166`

```dockerfile
```

-	Layers:
	-	`sha256:d1a03b31d564fb108267e58fbea24f9e87161db9fda3234c5c256c41b08016e7`  
		Last Modified: Fri, 14 Feb 2025 02:32:25 GMT  
		Size: 6.9 MB (6920799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbb2f4ffc6a24f9ba703aa65eaaab6469555d55d7ad8087bccefba4797fa52cf`  
		Last Modified: Fri, 14 Feb 2025 02:32:25 GMT  
		Size: 58.0 KB (57959 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:a20c583fa708b85d0516fa4bd9632bc6b13ecaa6170cdbf568a92403d6a4698d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.4 MB (138445160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e86df0a764ba5a0e371f64a33543362dde74009780a29a821fc9fef99b0170e2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1738540800'
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Feb 2025 21:31:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Feb 2025 21:31:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
WORKDIR /var/www/html
# Thu, 13 Feb 2025 21:31:38 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:be8e62ac4d3904082a64376be6dbebabc925200adb880f791173ab7f6800b156`  
		Last Modified: Tue, 04 Feb 2025 01:38:07 GMT  
		Size: 25.5 MB (25533883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9f22afe418a45c031cf43983b6e05c8ed9b386411bd488f375251dc4089c49`  
		Last Modified: Tue, 04 Feb 2025 05:25:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20b645f918db98d26680f3077f4791bf599ff64dcf689b13a40c8243399e230`  
		Last Modified: Tue, 04 Feb 2025 05:25:06 GMT  
		Size: 69.1 MB (69119296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c03588c4764681ba1b285def08d8bf43afd148e8bc56a103b85f5ac8fd68cd75`  
		Last Modified: Tue, 04 Feb 2025 05:25:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011d0e07a08551756fc0d9251dd7d8adcb43b54b55f862230c27cb52281d3c0b`  
		Last Modified: Tue, 04 Feb 2025 05:28:49 GMT  
		Size: 17.8 MB (17816973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e5d87506fe5f9d0f2478db889ed9a97ded17fd651aa1775559280fe1356590`  
		Last Modified: Tue, 04 Feb 2025 05:28:49 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:723307e39c6c36865316265914b7178ea59e979eaa4e029b7a48851b408e44a7`  
		Last Modified: Tue, 04 Feb 2025 05:28:49 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3395dbc0fefb48d3c05c8a2175f3fb46b47e0a17e2a71e1ed9c8a87be2826b94`  
		Last Modified: Fri, 14 Feb 2025 04:49:10 GMT  
		Size: 13.7 MB (13712497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f545d60dc8dc75eba505bd30d36ae35e07ba6bf2d6d8cc5ed962fa72a1ec1e1`  
		Last Modified: Fri, 14 Feb 2025 04:49:10 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a1acfa3c00bbbfb689a3368f1b2b994533753c846707404755040136ab0674`  
		Last Modified: Fri, 14 Feb 2025 04:49:11 GMT  
		Size: 12.3 MB (12257027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332b502cf66bc7c02ea7b32e34809bdfe06307a7650e46b1b5688a325c3f16b4`  
		Last Modified: Fri, 14 Feb 2025 04:49:10 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b593c48990e51e73332cb989e5702ca3cb7a5f8fa4ed56e73863f9f1d156c56`  
		Last Modified: Fri, 14 Feb 2025 04:49:11 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05adbae3ce9f325f694f730a5e927f1a214d76615c4a2284410ec483e6f544a2`  
		Last Modified: Fri, 14 Feb 2025 04:49:11 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:24fcc4994abfd19ecee51ef182d912f1f6c6fa3b78e7ae44d4ba42760c5a2fc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6787814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea5d00015c771293c83009638d067c4d87bc17a737c679d50f88613011c833a8`

```dockerfile
```

-	Layers:
	-	`sha256:cb2e1c22e925f5124b450d1d9d906670bd348131ebc66daa62eec8482732e849`  
		Last Modified: Fri, 14 Feb 2025 04:49:10 GMT  
		Size: 6.7 MB (6729677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45a87878ac1c59c42e146e1152e7f317f53631b985a6601ad787d244585d76a5`  
		Last Modified: Fri, 14 Feb 2025 04:49:09 GMT  
		Size: 58.1 KB (58137 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:5ab9c80e422f0ff9db741181c13a783bb6c3165d169b66bac8870b24a167bb5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161948508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18985b333adf4470e17f38b9be0adab52c724c8f42214c31c616171ba753b5c3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Feb 2025 21:31:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Feb 2025 21:31:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
WORKDIR /var/www/html
# Thu, 13 Feb 2025 21:31:38 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f170b18fc37f37ecc87975e5944875fd3d007167024e0f8a586c70f59364c2`  
		Last Modified: Fri, 14 Feb 2025 02:45:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9877a67bcea947fd28896ce8ce4388d08d8eae5ea20fe294649dcd55f6253c`  
		Last Modified: Fri, 14 Feb 2025 02:45:49 GMT  
		Size: 86.7 MB (86734370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a4bff070cb9c3aa82cac65e78d2b37dc73ac5f5518d9eef698f9ef5c2dc618`  
		Last Modified: Fri, 14 Feb 2025 02:45:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07124adb1d9b97db6d688feed5df86faaa1d4e336db6f7eb6286181761eeb742`  
		Last Modified: Fri, 14 Feb 2025 02:49:13 GMT  
		Size: 19.0 MB (18981147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d92e0cfe925cb5172c8c47b5b8748909ce3ba205a61e1b822bc1098f0acd5d`  
		Last Modified: Fri, 14 Feb 2025 02:49:12 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe9521d4d77bd33c8dec7224d364cbac56032849b7ea68a92683a653b4aa551`  
		Last Modified: Fri, 14 Feb 2025 02:49:12 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdefbcb8dd218c3b46cbbe62cbe8e2e3aa10ad3f6e8c3e401ee1d8560ee560ad`  
		Last Modified: Fri, 14 Feb 2025 02:49:13 GMT  
		Size: 13.7 MB (13713317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5212bdd4efe8b7c11ca091b05b4301c1651531cd35aaa42a0d9c2df63d50055b`  
		Last Modified: Fri, 14 Feb 2025 02:49:13 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c67df255fed271b7b51c934ac86bbe914db6521dffbf5c1619341b31daf0f`  
		Last Modified: Fri, 14 Feb 2025 02:49:14 GMT  
		Size: 13.8 MB (13769384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c99bfb10d764b757cbee4666f121bc4357a10f6e9f2b63e07ee4b966b540ce5`  
		Last Modified: Fri, 14 Feb 2025 02:49:14 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05010897ce00616c6db4b16a8d8487c006d880a37505fdc25098279b117d784c`  
		Last Modified: Fri, 14 Feb 2025 02:49:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386beb28db324c23fb778178a78de05c925cbd9cc6457005d9b24f80408d08bb`  
		Last Modified: Fri, 14 Feb 2025 02:49:14 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:fbbc2d0095800f8f43775a533942cb899ac81c251d781d3f55363376f0ac69de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6981772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202df0f8598c98d135c63623f10d16647b447d8608614d28668f9aff362b7a88`

```dockerfile
```

-	Layers:
	-	`sha256:3aef688dfdf5256389a905db40f0a513d0016f2da512cb5252cf0d022b998f4f`  
		Last Modified: Fri, 14 Feb 2025 02:49:12 GMT  
		Size: 6.9 MB (6923589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b0b0946dcb2d08f1eab8628d985099baeef46574eb62f97dafee3304cd9e75d`  
		Last Modified: Fri, 14 Feb 2025 02:49:11 GMT  
		Size: 58.2 KB (58183 bytes)  
		MIME: application/vnd.in-toto+json

### `php:apache-bullseye` - linux; 386

```console
$ docker pull php@sha256:3d67ceed64183cc7f6b19de08c9ed34404d7d125fd349652d2110ec3919cf363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171337265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c489fa7287394bafa4d7957c6cceb16f23df9e18fb88ed794706fbbaa29b63`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Feb 2025 21:31:38 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Feb 2025 21:31:38 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_VERSION=8.4.4
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.4.tar.xz.asc
# Thu, 13 Feb 2025 21:31:38 GMT
ENV PHP_SHA256=05a6c9a2cc894dd8be719ecab221b311886d5e0c02cb6fac648dd9b3459681ac
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Feb 2025 21:31:38 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Feb 2025 21:31:38 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 21:31:38 GMT
WORKDIR /var/www/html
# Thu, 13 Feb 2025 21:31:38 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Feb 2025 21:31:38 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0820289d697a57b1ebe2d97bdaf578098ec852f81bfa869fab657593f27ac59`  
		Last Modified: Fri, 14 Feb 2025 02:32:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf9b2f34ec0ef6e19a6f58e192a54ccb42b9c94b1035f63c46c1b54d9a7f7be`  
		Last Modified: Fri, 14 Feb 2025 02:32:33 GMT  
		Size: 92.5 MB (92521777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13db3e89ed106597429699fa83a3e29b0676127142fc1d4ee4ffe137661f2680`  
		Last Modified: Fri, 14 Feb 2025 02:32:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86dd2f985f96643ad97789e184f1656295e1a679d44c2f5eaf45530e90d3d69`  
		Last Modified: Fri, 14 Feb 2025 02:32:31 GMT  
		Size: 19.6 MB (19552847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ea31bfa23b330f9fb07e27e6fd1928a76c641d36b524fd4def8ee4d437dae3`  
		Last Modified: Fri, 14 Feb 2025 02:32:31 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469eded895e11bbf4b8ace9b9818616dbf05933d12b355574615fcb0a4b40961`  
		Last Modified: Fri, 14 Feb 2025 02:32:31 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1acd200c92e1c8ec7b865ebae82bccd0c86f1528acadda9049252aaf657078`  
		Last Modified: Fri, 14 Feb 2025 02:32:33 GMT  
		Size: 13.7 MB (13713263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affd77b269ad72ca3b8dfdca9a223ef1bf691cd10b114da79dc82c5f5721f687`  
		Last Modified: Fri, 14 Feb 2025 02:32:32 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c3da6f970ee3e4846ba5a3a0c6b6ad2802eb06c50a3ca3f900b5453f74affd`  
		Last Modified: Fri, 14 Feb 2025 02:32:32 GMT  
		Size: 14.4 MB (14365026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22be509204143019d58875400793f43acf87581c97598fd4b88768da1d7d748a`  
		Last Modified: Fri, 14 Feb 2025 02:32:32 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28457a65fd2d91c4e6d7c7962b9c21c0224dfd09baa321f660016e667d93f28e`  
		Last Modified: Fri, 14 Feb 2025 02:32:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62efe632912e896c02e4aab36d1a631925d6145fc527d03055344be4f54cd5dd`  
		Last Modified: Fri, 14 Feb 2025 02:32:33 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:apache-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:0b73c24aed01c2a25c690421f1872f3f54eef3b8d610e8ad4d10acd3b5112857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6969329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f890e8a78c5e07c59234ece5b96f040d5a908769e2c84e40513874edc975eaf0`

```dockerfile
```

-	Layers:
	-	`sha256:499115315d78824d02d613f17ff2cafb08d53107175bf22669a4a6861837b96e`  
		Last Modified: Fri, 14 Feb 2025 02:32:30 GMT  
		Size: 6.9 MB (6911419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:754212240fb5b7a4382b82321b14841f6a43ace08f8e94dad8f6b070832ed6b1`  
		Last Modified: Fri, 14 Feb 2025 02:32:30 GMT  
		Size: 57.9 KB (57910 bytes)  
		MIME: application/vnd.in-toto+json
