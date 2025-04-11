## `yourls:latest`

```console
$ docker pull yourls@sha256:298827a5ba299ccb5c9baceb5aa4ba679409a2e978c78881e8d900842196c37a
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

### `yourls:latest` - linux; amd64

```console
$ docker pull yourls@sha256:a8bf12c3dc2fa0ac3e935bfe4f9f57f27e75ecefaae1b58193b0c6d36c71838e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.0 MB (186965445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b35227cea1f126bd8b6bf683119c7cb266c4564680d094924f9144cd56b03199`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 03 Apr 2025 16:33:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 03 Apr 2025 16:33:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 16:33:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_VERSION=8.4.6
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 16:33:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Apr 2025 16:33:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 16:33:43 GMT
EXPOSE map[80/tcp:{}]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["apache2-foreground"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fa59a7a5495717f68946c1a6402a6a5b0169fbebf8061fe0e0a47eb0d822a8`  
		Last Modified: Fri, 11 Apr 2025 17:02:16 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d50c230598ebcc6d231c565381cbad453d8b063b0cee7774d17de9fd797498`  
		Last Modified: Fri, 11 Apr 2025 17:03:22 GMT  
		Size: 104.3 MB (104328933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc0729a0babad8ddbb2bf0ec6dd59135537c6b2a3316f9e562f534f4dfbcde3`  
		Last Modified: Fri, 11 Apr 2025 17:02:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ce48bee8a5bb56b914728aa2dcf0ae5b6927ed55223e79c0d6ec219cd43637`  
		Last Modified: Fri, 11 Apr 2025 17:03:20 GMT  
		Size: 20.1 MB (20123746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4eb234cfc99ad9edf3ef3230ca5c03d902d4f839274b74cb6b671635360d79`  
		Last Modified: Fri, 11 Apr 2025 17:03:19 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a63fa5236d8cc3e9e25f8281cde485cdf37d1e15e46355c9ce3080d4468a750`  
		Last Modified: Fri, 11 Apr 2025 17:03:20 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27c2a2460a341725bf64f6daeb1c1a55563b8dbb86cdb79e781f573aeffae5d5`  
		Last Modified: Fri, 11 Apr 2025 17:03:21 GMT  
		Size: 13.7 MB (13741335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752494fa16684cc394b165d3a81969ece119bd215b09ded782ef03c4bedaedf2`  
		Last Modified: Fri, 11 Apr 2025 17:03:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eca2159292da5982868039b04d34b7bdb0bcb00defa1638cd199c7e1209cda0`  
		Last Modified: Fri, 11 Apr 2025 17:03:22 GMT  
		Size: 14.2 MB (14166497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54785a43cf5ab94a29ce8286d2004bb9362e0b7d4ead29612db5a3c11259abb1`  
		Last Modified: Fri, 11 Apr 2025 17:03:22 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f90828d610345b4104daa1065e9b2ef2dc6b50410fe53bcc44d71fdca020d3f`  
		Last Modified: Fri, 11 Apr 2025 17:03:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ac9e1e3e3e6008eee7574ec914b397553254c63372e07664c69be0203ee496`  
		Last Modified: Fri, 11 Apr 2025 17:03:23 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255aab271b00df0a150de34b1e1efdf81ec7031c16526b10492099872f86f22a`  
		Last Modified: Fri, 11 Apr 2025 17:09:41 GMT  
		Size: 662.3 KB (662265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00e541f511a0fc2378418a12d1000d1b746375f7c74000ccd55c63a0dc577ae3`  
		Last Modified: Fri, 11 Apr 2025 17:09:41 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc80d8b89fa09f387bfbf3a42e42e92436444a8c023b39d30ca5bfc65d3ac5cd`  
		Last Modified: Fri, 11 Apr 2025 17:09:41 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e11320d441e88462c8dbb774ca53f023ba35a1aaf7bc7c1f93cc3687bb7b18a`  
		Last Modified: Fri, 11 Apr 2025 17:09:41 GMT  
		Size: 5.7 MB (5705148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03679c946fd34f283979799b9bdf73e62fb157336130e7850fcfd6a1f273bad2`  
		Last Modified: Fri, 11 Apr 2025 17:09:42 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab77add3f71c552ed4094319ae3c5d4eb19f464dbdbc8b71b5602bb2e8e112bf`  
		Last Modified: Fri, 11 Apr 2025 17:09:42 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6b67cf1ec7c57f9c286f3dbf6ff41550df04702b100b737116697866227a61`  
		Last Modified: Fri, 11 Apr 2025 17:09:42 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:62e6864405f8297990d427f9c3e83600643593493317340de0c2efe9f01df09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 KB (39008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e2ea2641cb48ca0f3c607c43d2a4fa87304dc562a17d134acc42627e7b9df9b`

```dockerfile
```

-	Layers:
	-	`sha256:975534b72d9b52add8e50df4c973a5dbc9490110d01962a2230d53a32e8b2b28`  
		Last Modified: Fri, 11 Apr 2025 17:09:41 GMT  
		Size: 39.0 KB (39008 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm variant v5

```console
$ docker pull yourls@sha256:1a75d55c331ee73d344045c1c5891ad343348beb9f725c1816dfaab34a8b75c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159717157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae126e97cfc77f637beb6e1369ade4063f3673e39065dcbada3f4f08547a00a9`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 03 Apr 2025 16:33:43 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 03 Apr 2025 16:33:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 16:33:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_VERSION=8.4.6
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 16:33:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Apr 2025 16:33:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 16:33:43 GMT
EXPOSE map[80/tcp:{}]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["apache2-foreground"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ede7f8a7a1736b2e1b1ffe73c183b355dc5ee08397a7422bb32c05c5d814665b`  
		Last Modified: Tue, 08 Apr 2025 02:08:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b061af77698181b6bb0dd67d0bb746c766d8bd85efe5f88c650b068d46e81b14`  
		Last Modified: Tue, 08 Apr 2025 02:08:21 GMT  
		Size: 82.0 MB (81993897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f8695a0bd1bfac037b09588f9a6fc30e41235265df32436850260ead851069`  
		Last Modified: Tue, 08 Apr 2025 02:08:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03c130c61813856b232b40bc695445765a169983299bdfa9039772b3faadf57`  
		Last Modified: Tue, 08 Apr 2025 02:12:37 GMT  
		Size: 19.4 MB (19418866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f85bfe26e31b06742b9d342330fa8e0ee545b24a441e7a5aeb67856706abeaf`  
		Last Modified: Tue, 08 Apr 2025 02:12:36 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3febb68d833ecf2a9d208931eda2bc74eb7d0413ca27c65776b8e9d25bdd1709`  
		Last Modified: Tue, 08 Apr 2025 02:12:36 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278fa2295bf934edc8ddb5ab56c29848c3eef402b272719ba88397d936049d6f`  
		Last Modified: Fri, 11 Apr 2025 17:10:13 GMT  
		Size: 13.7 MB (13739518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc18aeffd4ff90316fae9b51c08e5f5b65bbda21b281889e79e845b5b8c95ac`  
		Last Modified: Fri, 11 Apr 2025 17:10:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c3911ebf4467470e2c9444e4c0ddfe5acee9eb16f9fe2feca1f2d729880190`  
		Last Modified: Fri, 11 Apr 2025 17:10:13 GMT  
		Size: 12.9 MB (12918517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2716845003db68ae8ed96832ca89944221b0f50cf1c2e328d1b849a59c10ee3a`  
		Last Modified: Fri, 11 Apr 2025 17:10:12 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c96aad646ff0449201a5e668cdb52cfdddace2e539e1068d4cc9bd7ba02b309`  
		Last Modified: Fri, 11 Apr 2025 17:10:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ffd02cfd64ff5279db60348354283c581d40a2cb0e21cbad13c843523f2a89`  
		Last Modified: Fri, 11 Apr 2025 17:10:13 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53988b014998fe4a25a5458f11fe8393230ef6fc17c2eb6b5b852c75246e580d`  
		Last Modified: Fri, 11 Apr 2025 18:26:54 GMT  
		Size: 173.1 KB (173111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77000f4090d8a47adb53ec04530b49e702f054b13708f97c9c12fa61f0bb9985`  
		Last Modified: Fri, 11 Apr 2025 18:26:54 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d523656e02a257d5db69c7a54da30d3fffd8a0e505cda5f925ad630c798ac9`  
		Last Modified: Fri, 11 Apr 2025 18:26:54 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c5c7944d8e8424584ab230cc94583091e8a5f44b6d2a82f9b59ea5e08671b7`  
		Last Modified: Fri, 11 Apr 2025 18:26:55 GMT  
		Size: 5.7 MB (5705149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af1afbc9f8a3a740c714d10b6624c7b49d9e623a40a2dc429659127fd0d3e10`  
		Last Modified: Fri, 11 Apr 2025 18:26:55 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af9f9672dd9358585d8716f9ccd28054b13748250a30f5f43c2a80008f64b71`  
		Last Modified: Fri, 11 Apr 2025 18:26:55 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93d4b0ef1734326073d9de9d9074e14813136c8ff57731cc68e50f362c3743`  
		Last Modified: Fri, 11 Apr 2025 18:26:55 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:8bd67b90661b22189ad92416dac22b70f328d3b246c66e7fa2e88ae7acf30b11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ba9961a88b059dc39284a33979ea5840290621def763d823fc275ab074e14a`

```dockerfile
```

-	Layers:
	-	`sha256:3420da9293e15606de993774db648d32767d50fb982f0ffa338d1c0ab4c12fb5`  
		Last Modified: Fri, 11 Apr 2025 18:26:54 GMT  
		Size: 39.1 KB (39148 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm variant v7

```console
$ docker pull yourls@sha256:b6ea8ddd77b81e9566843edd264f3de54c0ee278146823d3df53df6f4c8bf281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150838613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c06bd7ea99cad4f1caf11830049d07b9888c01b0d999aaaefd8d0d513278d7`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 17:27:40 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 17:27:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 17:27:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["apache2-foreground"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7d4b097a6bd1e1c6005148baf6fe5c3fc8f71c3806b0533176b9e71d30fae09`  
		Last Modified: Tue, 08 Apr 2025 02:06:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b59a7abdeed6ca1e9edaa9c4d716d1e51f3acd76ac9b8a9593379251477a15`  
		Last Modified: Tue, 08 Apr 2025 02:06:14 GMT  
		Size: 76.2 MB (76162685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911e77faae9141f2a82370cde20bb002409354ce3554b28663322cebbfd4d775`  
		Last Modified: Tue, 08 Apr 2025 02:06:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e979a46700c4cc8c523fd97c1920eda2a65475e59e5b50da04ec094381646cc4`  
		Last Modified: Tue, 08 Apr 2025 02:10:09 GMT  
		Size: 18.9 MB (18857333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b785355f97ba083df35cb14c0fd6f4ca577253c72f4946c98e2965daf3ec4b6`  
		Last Modified: Tue, 08 Apr 2025 02:10:08 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6315b72a13f74b37348b5dc00938e06103a423aa74a44181c5cfb4d60cd94140`  
		Last Modified: Tue, 08 Apr 2025 02:10:08 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31edbe1ca6d24ec16bb2f9a388169e53062cee1fe59f23313c0f43c4c39d03d0`  
		Last Modified: Tue, 08 Apr 2025 02:40:08 GMT  
		Size: 13.7 MB (13731541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091d2f101b0011f3f7b33f96b4b943358160b25813c8879768eed36d701efe70`  
		Last Modified: Tue, 08 Apr 2025 02:40:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596e397ac7f538ac20658312135fd366ab0f2ca7220573086018dbb7cef0243b`  
		Last Modified: Tue, 08 Apr 2025 02:40:09 GMT  
		Size: 12.3 MB (12274782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c51be084a110daabe9d3668e60db69b37ab6627cb9cfcf6f95140c947510f8`  
		Last Modified: Tue, 08 Apr 2025 02:40:07 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4439b496fe2a444a2487a5ca1f94a1e40cf5b69770f29eb186e554baf8456135`  
		Last Modified: Tue, 08 Apr 2025 02:40:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e5243914888bbf22d158829646d224f4512e438af2da2c533bdb19a687cb63`  
		Last Modified: Tue, 08 Apr 2025 02:40:09 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950b0fcd4966671f9a7d45e7443103401dbe71eb4581a34f812083974c5a7426`  
		Last Modified: Tue, 08 Apr 2025 17:27:58 GMT  
		Size: 159.0 KB (158990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5569b55a15bc25905e646575ff02385baa2640caff09f996094206753d10d21c`  
		Last Modified: Tue, 08 Apr 2025 17:27:58 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112c63208befeca749f2cdb174d769e0c84de91aa79885779eaf43085b4f2ae1`  
		Last Modified: Tue, 08 Apr 2025 17:27:58 GMT  
		Size: 347.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff44f0d4a21a496bf0d85c0b4fa64b16d2c0c2f893670ea70a33d9a160c2529`  
		Last Modified: Tue, 08 Apr 2025 17:27:59 GMT  
		Size: 5.7 MB (5705139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af42473bc2ea2e8df3b22b2a70eae497137bced971884c50d049d19277160e19`  
		Last Modified: Tue, 08 Apr 2025 17:27:59 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44428bdea5533c24c884cd89b5ea0e020d0f47f90ddaf9819ca7d238b931f217`  
		Last Modified: Tue, 08 Apr 2025 17:27:59 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df514884a9bcb80fe5d9287747bb91ddae3b0beb7812790abb1a15f78ed5fc4`  
		Last Modified: Tue, 08 Apr 2025 17:27:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:26457a9d8da684e7301221801f608b5b10e975481f97c059926b895248f14ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b4daed61a14d1d41ff51cdafad7bb259f4c48614b350b3d8548a28bf926585`

```dockerfile
```

-	Layers:
	-	`sha256:8dfa781ce06a18a990975f19bb653811dba6c262c7d36ead685756fd5d775de4`  
		Last Modified: Tue, 08 Apr 2025 17:27:58 GMT  
		Size: 39.1 KB (39148 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:569e0f520bc4b4819727de49d2fe48ffe23e3f157c4323a39fe3afee03195615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.1 MB (180104407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d3e4db6024c858891543657307274952d8f7ffc6775f2ec8acf53f78a4fdc8`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 17:27:40 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 17:27:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 17:27:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["apache2-foreground"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705c5f6dffca44b4205f0e945a57290bb8e3e1ae585f26eccc2c9828d7f9ccda`  
		Last Modified: Tue, 08 Apr 2025 02:20:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc8e5730fe526cc83387586aee6b7883edb46c1cbf4028dd372d5e9cc4aa7ec`  
		Last Modified: Tue, 08 Apr 2025 02:20:36 GMT  
		Size: 98.1 MB (98130393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d28e77e2da9013ba78046a81e9835f08797c66738b7838294afd4c12822ca8c`  
		Last Modified: Tue, 08 Apr 2025 02:20:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb08e5d87081c943aebec15603635f044e709767399fb9288a5d353191df808c`  
		Last Modified: Tue, 08 Apr 2025 02:24:16 GMT  
		Size: 20.1 MB (20120982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f63fc51568c1c2eac81ae1839660c84517f78b8a9f41fb196501391ccd75a90f`  
		Last Modified: Tue, 08 Apr 2025 02:24:15 GMT  
		Size: 436.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5eba2365fced3eefbecb722f27c4db6bc90624cbba0b3bac5a572af06d125f7`  
		Last Modified: Tue, 08 Apr 2025 02:24:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab562b2866ae1872105c38ea32cead32e9da35632e121f8eec63601a6c5685b`  
		Last Modified: Tue, 08 Apr 2025 02:52:30 GMT  
		Size: 13.7 MB (13732990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e64d78ad1d48c286cd49af34d67ca98e8d1b55b8abb3431dea7f4f488d0a4f6`  
		Last Modified: Tue, 08 Apr 2025 02:52:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10e7850e2b8417df601193d588bdc162d9867b500038b754653e8d587203db6`  
		Last Modified: Tue, 08 Apr 2025 02:52:30 GMT  
		Size: 13.8 MB (13768678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b917ccdd67db8ddcde2c315615b0fa17d2cd8afafea08f429f9ae21dac8f52`  
		Last Modified: Tue, 08 Apr 2025 02:52:30 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ec394bda2121342bd4fa0ecfd8bf1e0c3327c052d1a4e796b5e3209dca5a2c`  
		Last Modified: Tue, 08 Apr 2025 02:52:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785080df917c11ea75d0c6d354369f30342066814e8ef7a3890f72b2c9addd36`  
		Last Modified: Tue, 08 Apr 2025 02:52:31 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248a3de5387ecb47ee5fbfa9381817f3143494cd6ffea713954a32fb50e4340a`  
		Last Modified: Tue, 08 Apr 2025 12:13:35 GMT  
		Size: 569.6 KB (569638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ab52415034fd7efbaac02d932966c7132581cf07efd252dd8c909e522e7fd8`  
		Last Modified: Tue, 08 Apr 2025 12:13:35 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d08429b573ac84348e148b7bfdc930b8c71167a6a2cb709118a900d7b7ec90`  
		Last Modified: Tue, 08 Apr 2025 12:13:35 GMT  
		Size: 348.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769cdb4e938d74fd2b9e11ee0e9b42eee4afb360c9ca4f60350bf6f395f918fc`  
		Last Modified: Tue, 08 Apr 2025 12:13:35 GMT  
		Size: 5.7 MB (5705130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c923584efa9f62dfbff6875c7990281af5f5ececfeb90520a91dadd8b23e05`  
		Last Modified: Tue, 08 Apr 2025 12:13:36 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9a06460d3a1e23df40cb90acaaf9c6e7d8a30d805b5da3c84619842ab05820f`  
		Last Modified: Tue, 08 Apr 2025 12:13:36 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833ed093ffd5a949b85f7075879cd36d30e5ca39f62d35041d87c80fdd8a2f45`  
		Last Modified: Tue, 08 Apr 2025 12:13:36 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:aea36bb3f6786569779ae5534ea9c52f98a322845bb14be6887c908457b92118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 KB (39198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f9473d6e16ac41a44291eda787e06bc0121b6b907cde97417c72172d1be8077`

```dockerfile
```

-	Layers:
	-	`sha256:9a0f494747d51892a04cfb247e6ea8ab3e28f206ffe0ab9179b52c5066add10c`  
		Last Modified: Tue, 08 Apr 2025 12:13:35 GMT  
		Size: 39.2 KB (39198 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; 386

```console
$ docker pull yourls@sha256:f428aaa606b8eb6f50213e94d62f1db781accf072f71ddd91f6f03f873e22eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.0 MB (185963211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3a5da9d1d9ee51b4a8aa24a750e7ef6c99de13c3549041ac1795a97682b946f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 03 Apr 2025 16:33:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 03 Apr 2025 16:33:43 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Apr 2025 16:33:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_VERSION=8.4.6
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.6.tar.xz.asc
# Thu, 03 Apr 2025 16:33:43 GMT
ENV PHP_SHA256=089b08a5efef02313483325f3bacd8c4fe311cf1e1e56749d5cc7d059e225631
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Apr 2025 16:33:43 GMT
STOPSIGNAL SIGWINCH
# Thu, 03 Apr 2025 16:33:43 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
WORKDIR /var/www/html
# Thu, 03 Apr 2025 16:33:43 GMT
EXPOSE map[80/tcp:{}]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["apache2-foreground"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecbc29f49eb69138afadaddf562bf8cbcf87694293fe5604449b0329a526928`  
		Last Modified: Fri, 11 Apr 2025 17:03:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49abf993ef5ef9e6fe55214eb1657a1a2d247052d26bb0562cbd86080adbd32e`  
		Last Modified: Fri, 11 Apr 2025 17:03:41 GMT  
		Size: 101.5 MB (101512786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d99fa445a490e3a33beaffbd9ab257bba5a47c99e50b2572ccecba23cde8adf`  
		Last Modified: Fri, 11 Apr 2025 17:03:38 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1833e0f6f35e78533eb0c9a8278e942b0cdf65badecfd268beb0b2a085c240c`  
		Last Modified: Fri, 11 Apr 2025 17:03:39 GMT  
		Size: 20.6 MB (20638410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaeb848e2613d809f08762814893b123625f0c398c810996c780c5ee4a1c893`  
		Last Modified: Fri, 11 Apr 2025 17:03:39 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc59ce326b39ce34fd040afa99bfa7beedd63a860672a8195bd73595f72759f9`  
		Last Modified: Fri, 11 Apr 2025 17:03:39 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d66f8e561cea0298a252fbe00371d3ff4e26b9a4234921e96f13315a815d7d`  
		Last Modified: Fri, 11 Apr 2025 17:03:41 GMT  
		Size: 13.7 MB (13740327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25030eaa7fdfdf5d6b7da8f08f3c5cc5265a1c329350687940e213a9688a14ed`  
		Last Modified: Fri, 11 Apr 2025 17:03:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78122d6b6593ebf941e6934812f721576d96493693645d3c2ed6c75ecc8193e`  
		Last Modified: Fri, 11 Apr 2025 17:03:41 GMT  
		Size: 14.5 MB (14460751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e499763c0271f90e3e20c7cc4d6c74c487f4cfa9176b2eeee200ad840aab33b`  
		Last Modified: Fri, 11 Apr 2025 17:03:41 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2b5dbd06092cfaff5286e582a65b3ed0a8286d2c1981b0821fd25411cb3eda`  
		Last Modified: Fri, 11 Apr 2025 17:03:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2850d7585245fb79804d4e90c6b57bc7f8a064c3ad4578d502e7e71a2efc7300`  
		Last Modified: Fri, 11 Apr 2025 17:03:42 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acfc2e05b2537a88fef94a0a3dc1f5bfc34bda33d6360301e8458ff45e2aaa35`  
		Last Modified: Fri, 11 Apr 2025 17:09:45 GMT  
		Size: 684.8 KB (684813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18003b8490b5de94d9c6bb540a103a27c04a5623560d40d44b0e61e1e6c2954`  
		Last Modified: Fri, 11 Apr 2025 17:09:45 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894cb6139952e67a34b2f2521d4c754503cf51d6e76d750ab668a6b5f3a8de19`  
		Last Modified: Fri, 11 Apr 2025 17:09:45 GMT  
		Size: 339.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986d68255d22f29ab908e3ee8b6c9565caf8940d7f64a07fcbf7bc076aec8f08`  
		Last Modified: Fri, 11 Apr 2025 17:09:45 GMT  
		Size: 5.7 MB (5705130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3092ccc1e27fab5e28e8bb0f6185e59ec7335fe9c200de5a04b72673a7fef27`  
		Last Modified: Fri, 11 Apr 2025 17:09:46 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7035ed8e89c9c87812ec84065517ef88e9a95a3714481e832f625d345d36ccb1`  
		Last Modified: Fri, 11 Apr 2025 17:09:46 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1433ad9887f5688a0e5a28b61ff408acf79ffc7cd638c8652b3176c12f492a21`  
		Last Modified: Fri, 11 Apr 2025 17:09:46 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:cd93c41a41a7d2afcd4e37020cca319b8e59de6865bb259d79ce081e92bbf904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 KB (38951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d05348cf6a0835efc2d4b21dddf722f4681be6891f67e649ee336c5ff5953345`

```dockerfile
```

-	Layers:
	-	`sha256:109a5825cf1991157cf6789e7770d8c6e87c141e49dab92efe020cb17a75c757`  
		Last Modified: Fri, 11 Apr 2025 17:09:45 GMT  
		Size: 39.0 KB (38951 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; mips64le

```console
$ docker pull yourls@sha256:fbabb51e976404aa1b31e2db8be9e54b6941e44b807901da2141e580240f7c65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.9 MB (161932733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadfa591565f09918b5a3f6edd96f83264d1f8d52d5c6514021b354638c02e0c`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 17:27:40 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 17:27:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 17:27:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["apache2-foreground"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ba0a04c9b2bb07ebbbf1ff9838da10bb162c6ac637a662105936e8b0cfe6c4`  
		Last Modified: Tue, 08 Apr 2025 03:33:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fb1f9e949a7943e3a44c47922361d3e69b1969a2cea4dec89ae36496be4b8b2`  
		Last Modified: Tue, 08 Apr 2025 03:33:53 GMT  
		Size: 80.7 MB (80670501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ea48728e7911587bf93013dabc6b5148fd156c8e821390a2fcc1d7e3112bc8`  
		Last Modified: Tue, 08 Apr 2025 03:33:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d45220d5b314961f76fcc9f51363853b5745dd7637549d29b537ad9e85005c5`  
		Last Modified: Tue, 08 Apr 2025 03:54:20 GMT  
		Size: 20.1 MB (20069188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2eab7faa10af817dd8310e47c802c4655fd298bafdc29fc210a73083dcdfaaf`  
		Last Modified: Tue, 08 Apr 2025 03:54:18 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87183d1ae13ad1c89771a8a8cf86d85be4ddaa72bc4b284c6d28fbf11b85d408`  
		Last Modified: Tue, 08 Apr 2025 03:54:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bbf4aa6106ffcd92a2dacc8c4fe1d26aa0e9185e3b7dbdcceea079c09159cb5`  
		Last Modified: Tue, 08 Apr 2025 05:07:42 GMT  
		Size: 13.7 MB (13731342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bd186a1ab945911528bbe911747e8c7617dfeb5af403faea6dab13e4449767`  
		Last Modified: Tue, 08 Apr 2025 05:07:40 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b3b10993aba888d0f5647ee50c39cbf9b4168b38e7aff2f9d0eb0985537bca`  
		Last Modified: Tue, 08 Apr 2025 05:07:42 GMT  
		Size: 13.1 MB (13062518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a464547def0fd9dcd8507ca588f66fbae403f5a95985d80da77d4091e98c03`  
		Last Modified: Tue, 08 Apr 2025 05:07:40 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce0d8c347fb87856a246256419201d93d7da6b100b8c02cb132708ae9239cdbe`  
		Last Modified: Tue, 08 Apr 2025 05:07:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a7fe90af0f656398a5b49d99388a0130b107bb57a0cffbbed51102306c7ab9`  
		Last Modified: Tue, 08 Apr 2025 05:07:41 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fbd34b0e5cbd893ae570477577811e3164517539104281be8dc7ce9ab234a87`  
		Last Modified: Wed, 09 Apr 2025 00:32:51 GMT  
		Size: 169.8 KB (169792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1c2864657ce2938107edacc0056985bd578e7aba724e8b90c1f265651e52b0`  
		Last Modified: Wed, 09 Apr 2025 00:32:51 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b239d934d928e5b1cc2950e759b516f31e0193e41c58b5f982bced40bd6c73`  
		Last Modified: Wed, 09 Apr 2025 00:32:51 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a06142d70a351bf57039b9a4791d7bc4843e1ccc8f856d69e29357f7870aafc`  
		Last Modified: Wed, 09 Apr 2025 00:32:52 GMT  
		Size: 5.7 MB (5705141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a312273ca6fca7488c5005390b966c31f44abaa7180f1f1a82d9d3bc7dc6eca`  
		Last Modified: Wed, 09 Apr 2025 00:32:52 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03076bc12e492170d9946ab72552b0b96123cd491bb93b03533cfc8ca030bafb`  
		Last Modified: Wed, 09 Apr 2025 00:32:52 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f007cc8551c0800fb060ff8c09d7a8de66c5af6dc0006b141c80647fb95b09`  
		Last Modified: Wed, 09 Apr 2025 00:32:52 GMT  
		Size: 335.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:f6736a4be496a130edeec855f8a73b979fa87c0fc4ec248aeee6e7efb2222cc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be44c39f434be40b9b9ab170571d1de552393d31629641ae03ccbdc062f7749c`

```dockerfile
```

-	Layers:
	-	`sha256:d6560d312bfeb8fbb1cd76f832c3e1e9657987a754c92b43086c315df185e25a`  
		Last Modified: Wed, 09 Apr 2025 00:32:50 GMT  
		Size: 39.1 KB (39112 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; ppc64le

```console
$ docker pull yourls@sha256:9827f408fb5e19562a4d0b4d1058f21da448a27e26e9a26e04c17d023516fc51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 MB (190940382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054b5852f10d26bd8ca887dcb44a7d3c0c3fcc2d1b9f311aa12556ede8769c1f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 17:27:40 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 17:27:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 17:27:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["apache2-foreground"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9a46967066ae4671f168da66f36a8b5a2975183ce39c8dd4a2b10bf95a917f`  
		Last Modified: Tue, 08 Apr 2025 02:10:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c687d4e4921b0609438b51c7d318fa414c7011636641c6b89f5fd3f8f3fc315`  
		Last Modified: Tue, 08 Apr 2025 02:10:43 GMT  
		Size: 103.3 MB (103324796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e3514f5d628c2a9213004449181d4a82ac680ebdb792bc18d335a66bc84e0a`  
		Last Modified: Tue, 08 Apr 2025 02:10:40 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f67434e8832967db0f0dce87d8c6f20e4cbaf6e006924b3f9536048a5ac7cc09`  
		Last Modified: Tue, 08 Apr 2025 02:15:46 GMT  
		Size: 21.3 MB (21308407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4adc38f5ae243525673101edcd5d2e2929fd04cd4d3310723abd07c4f041abe`  
		Last Modified: Tue, 08 Apr 2025 02:15:44 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a195fcdfa3af6fc1f6b42885b72bdb556c77252e12ba66006e705fff9e25f7`  
		Last Modified: Tue, 08 Apr 2025 02:15:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:165034220792c10bb926bcc969640223f7b3ec5dee0e55ccf0b3891aa822e686`  
		Last Modified: Tue, 08 Apr 2025 02:33:27 GMT  
		Size: 13.7 MB (13732779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b908c848a87e4b170e228f73a830fb49d9c114d0745a849f3bd5becf9b9b5221`  
		Last Modified: Tue, 08 Apr 2025 02:33:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdec30a25fcf03aa319539070be9011787137335ebffc5ee6ed15d51cee492b1`  
		Last Modified: Tue, 08 Apr 2025 02:33:27 GMT  
		Size: 14.6 MB (14580526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495b612c484fa36f627e822c6b54daf012403de3687e5b80985659796ae90b7b`  
		Last Modified: Tue, 08 Apr 2025 02:33:26 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e6bf6f8161245ed75f6c2ee719682ebe34036ba5436b3b993e6645536d60f4`  
		Last Modified: Tue, 08 Apr 2025 02:33:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23050a7ca559e176b4dbc6f926bca77fe79e8d36bffeb19a22a50d37a5101ac`  
		Last Modified: Tue, 08 Apr 2025 02:33:27 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0663bd274fe551923fb057a5480a02a8ab5263735f5c82061713f0ce27e704a2`  
		Last Modified: Tue, 08 Apr 2025 08:35:18 GMT  
		Size: 210.2 KB (210244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9923f85106f0a321c91c911c771a68bcaed7b0bc4558e8447615e68eebff6f`  
		Last Modified: Tue, 08 Apr 2025 08:35:17 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e4f2ad83ed2f5883dd4c964a781f08b478f8233eb13b9831bd7b51b819bcb7b`  
		Last Modified: Tue, 08 Apr 2025 08:35:17 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29554a259ce27b0f37a1d6f5967ccf32820bd3e7f484b75fdfe01bb8fa429a51`  
		Last Modified: Tue, 08 Apr 2025 08:35:18 GMT  
		Size: 5.7 MB (5705130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94798a34e2818c10fb0ecb574897ce9d7c3d18a1181b7797a77d0927f9b42b24`  
		Last Modified: Tue, 08 Apr 2025 08:35:18 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295c008e847cebda7aa52af616803c561a2ceb12955f030e16aa9980a658fd30`  
		Last Modified: Tue, 08 Apr 2025 08:35:18 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8935f9bc525244af299fd579e7eefb720a1f180d379843814cdcee64a98c5eea`  
		Last Modified: Tue, 08 Apr 2025 08:35:19 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:598b5d6ec27f338f4c6788feec62b4a2be001a3889304bf69b90526055ca9207
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.1 KB (39083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c6451f33e7d3b0e83e7b8e749167c3f7674013d17594fa4d59c352c753e235`

```dockerfile
```

-	Layers:
	-	`sha256:8da0db3ee347bbf64784d9a126c53b7751c8fb07b8f57f817b7cc9eaf0574049`  
		Last Modified: Tue, 08 Apr 2025 08:35:17 GMT  
		Size: 39.1 KB (39083 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:latest` - linux; s390x

```console
$ docker pull yourls@sha256:bb7ed04621698ec812bd8ecfaa856737fef4043f59c5201c71defc1262002b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160761640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1018e5649056adb10f55dbb374f5a1d83f3bed214d6e7f1ddf13343e582907`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 13 Mar 2025 17:27:40 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 13 Mar 2025 17:27:40 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 13 Mar 2025 17:27:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_VERSION=8.4.5
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.5.tar.xz.asc
# Thu, 13 Mar 2025 17:27:40 GMT
ENV PHP_SHA256=0d3270bbce4d9ec617befce52458b763fd461d475f1fe2ed878bb8573faed327
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 13 Mar 2025 17:27:40 GMT
STOPSIGNAL SIGWINCH
# Thu, 13 Mar 2025 17:27:40 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 13 Mar 2025 17:27:40 GMT
WORKDIR /var/www/html
# Thu, 13 Mar 2025 17:27:40 GMT
EXPOSE map[80/tcp:{}]
# Thu, 13 Mar 2025 17:27:40 GMT
CMD ["apache2-foreground"]
# Thu, 03 Apr 2025 16:33:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
RUN a2enmod rewrite expires # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ARG YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_VERSION=1.10.0
# Thu, 03 Apr 2025 16:33:43 GMT
ENV YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
# Thu, 03 Apr 2025 16:33:43 GMT
# ARGS: YOURLS_VERSION=1.10.0 YOURLS_SHA256=2756e534ef8a92fc183af5000583b354c9f147beca4a35f68dbe1b0ed0e40bc5
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
COPY yourls.vhost /usr/src/yourls/.htaccess # buildkit
# Thu, 03 Apr 2025 16:33:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 03 Apr 2025 16:33:43 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0629663656342054d2f9f2b005107659a6c173bb5f0b7cb64dc8cb1ee42b441c`  
		Last Modified: Tue, 08 Apr 2025 02:00:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687a798e29fb2285c77a2ed089ffb98dd2ae622d769dfc8b8796f747270caa16`  
		Last Modified: Tue, 08 Apr 2025 02:00:49 GMT  
		Size: 80.8 MB (80816477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8881dcc114cdc5cc5dfd6ca5beca1e2ac5ae137a5266f40776b68c106d43cac9`  
		Last Modified: Tue, 08 Apr 2025 02:00:47 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c520e00ddd0867ba8e331d1186044f72208c47374173fad3059cf8cc4adc8c2`  
		Last Modified: Tue, 08 Apr 2025 02:04:35 GMT  
		Size: 19.9 MB (19895320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a2897dccb49d2367540f651842e2f2ec441a6dd6b8b949377032b31cb747cd`  
		Last Modified: Tue, 08 Apr 2025 02:04:34 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d5efa8de1c9bc5dc861d369497b6023969810db9946783b63ee84762d9cedf`  
		Last Modified: Tue, 08 Apr 2025 02:04:34 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32513b176e076bccce8df20c74343ab8f432de5af74c8ee7cee638b5514193f`  
		Last Modified: Tue, 08 Apr 2025 02:19:05 GMT  
		Size: 13.7 MB (13731902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f78fe6bae0bf337376c04cc8f8c54eedf78bda3d8ed149f7285f7f9a18b40eb`  
		Last Modified: Tue, 08 Apr 2025 02:19:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce34e85ea1fdcf7da9726d7a87b53a9e39fde74918be53c0e8c99e77c6dbc06`  
		Last Modified: Tue, 08 Apr 2025 02:19:05 GMT  
		Size: 13.5 MB (13538393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e22a2a2d8d08d890bba4310276c840ea9a6824ba9020db3ec1e82a61c874d7`  
		Last Modified: Tue, 08 Apr 2025 02:19:04 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93463ce992f1dc75ffa8f6f672d2c13531d9472653d6a24db04d7b04497483f9`  
		Last Modified: Tue, 08 Apr 2025 02:19:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2136d7ca5ef39b5eb8b19f58f0da8b9b7e64e0fac9159bd097aaf43b8443c32`  
		Last Modified: Tue, 08 Apr 2025 02:19:05 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278a2adc65a746edd588458727d814ec70492c766267219a98e9760cc6d7baa6`  
		Last Modified: Tue, 08 Apr 2025 06:50:22 GMT  
		Size: 179.5 KB (179530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab0fcb304f16f1d4ae3ccdaa6af317bfd1e1bd2bd60bdfd423886a6d03bfeb8`  
		Last Modified: Tue, 08 Apr 2025 06:50:22 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c62f93c036e473ba97987cde98c7f139e2ce5f79a8e287aab67fe9f623dd4e`  
		Last Modified: Tue, 08 Apr 2025 06:50:22 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996468313bcdf74e7d859a6222cec6d40a0e553af0cfbb5d3be8844373535fe3`  
		Last Modified: Tue, 08 Apr 2025 06:50:22 GMT  
		Size: 5.7 MB (5705141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc90ae6f69089b8ac209d9d1c10b92095dcf470c8552420b7506e100c23fe85c`  
		Last Modified: Tue, 08 Apr 2025 06:50:23 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2362a237199e0e3eb69dc3765e62d9b40d0da7dc994e014f90aa68037fd720b`  
		Last Modified: Tue, 08 Apr 2025 06:50:23 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f71f0ad323da7d8070d5a6e97313be6ec92f105a446d56ad705b39a9934e5b5a`  
		Last Modified: Tue, 08 Apr 2025 06:50:23 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:latest` - unknown; unknown

```console
$ docker pull yourls@sha256:f6edd48cb4e0d0171aba7af84f27797bf0091615d5e0561096563dca195f7361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 KB (39001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc1f2a3d81289db47a3c29113956973563b0dc6b60da1889b3a8d030768cc82c`

```dockerfile
```

-	Layers:
	-	`sha256:f98c48507f472f95c06d415fda09b9cac67b4eb9c01e69a23ce7bb2f2425bae3`  
		Last Modified: Tue, 08 Apr 2025 06:50:22 GMT  
		Size: 39.0 KB (39001 bytes)  
		MIME: application/vnd.in-toto+json
