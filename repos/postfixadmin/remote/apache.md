## `postfixadmin:apache`

```console
$ docker pull postfixadmin@sha256:af066246bca43fbd63b31b654e7cc86a1ef2637e90976c2edacc8648b19176a7
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

### `postfixadmin:apache` - linux; amd64

```console
$ docker pull postfixadmin@sha256:06d4036d3e28366234b7d331edd7061e28fce2d4a2ae7c2c0a30cfb2a1cab21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.8 MB (180775563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76fdb71fb798622380ec00205f7286fd824d4b91e43710c8f2f1f6f3edd71bf5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 22 Nov 2024 13:33:57 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 22 Nov 2024 13:33:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_VERSION=8.3.15
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Nov 2024 13:33:57 GMT
STOPSIGNAL SIGWINCH
# Fri, 22 Nov 2024 13:33:57 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
WORKDIR /var/www/html
# Fri, 22 Nov 2024 13:33:57 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 Nov 2024 13:33:57 GMT
CMD ["apache2-foreground"]
# Fri, 22 Nov 2024 13:33:57 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 13:33:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee76793b1dc27d2be891bcae43ebacbb8afda83987fc906ce6c29215b4e76045`  
		Last Modified: Fri, 20 Dec 2024 21:33:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be874e774f8b0057d5eac486bb6e3125122cf551d23f1959dbf36fb004f4effd`  
		Last Modified: Fri, 20 Dec 2024 21:34:14 GMT  
		Size: 104.2 MB (104150632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aaf01a6bae4eaf5b3f24bc3f599863b148b85a15a405367143fb591fe8c42c6`  
		Last Modified: Fri, 20 Dec 2024 21:34:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3255a282480dc63c4d7815fabe4e2f6951126483b20b78529849a8a38e3ffe72`  
		Last Modified: Fri, 20 Dec 2024 21:34:13 GMT  
		Size: 20.1 MB (20123860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f950b3b482eb5c6ea4d53e33cb35bf3ca0c48fb5f07f558cac4467cb580a76`  
		Last Modified: Fri, 20 Dec 2024 21:34:13 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db00025dce0bf3a570eec1b015d6ba37538d7d7499234fcb3a8753c79e1b0f37`  
		Last Modified: Fri, 20 Dec 2024 21:34:13 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87844378dac54758acbc418e711b8ca7aa9ed7c5727c2eb6edead646e42c7d29`  
		Last Modified: Fri, 20 Dec 2024 21:34:14 GMT  
		Size: 12.7 MB (12653155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab92348d597f7a0732179260489735af567251e0adef51ef77c17138e961f19`  
		Last Modified: Fri, 20 Dec 2024 21:34:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f1eafd839bd2e3b82b8d3500bcdb25caa952ac37756d73f001f505305128e47`  
		Last Modified: Fri, 20 Dec 2024 21:34:15 GMT  
		Size: 11.7 MB (11652473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa1f1ec9914d51fc5c35d1dbe956d6086a936d015ae61f26b7da85275362c3e`  
		Last Modified: Fri, 20 Dec 2024 21:34:14 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb577448e6d3c0ccdcf2a537c413c8adf1a8d50336c02d6414f842acc2090b32`  
		Last Modified: Fri, 20 Dec 2024 21:34:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c74faa8e00c73f2f53222c3dfab3ee80909daf1bba93f2ce7a72e1fa0223c7`  
		Last Modified: Fri, 20 Dec 2024 21:34:15 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0bf96313b87d9ace2ca85a994d3227fe6e0868b86e2704a6bbc029990ebc71`  
		Last Modified: Fri, 20 Dec 2024 22:30:23 GMT  
		Size: 1.1 MB (1092508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b49ace922b42e6b7de35773ba43f095986f3f9a4528b60fa2ba39e0ab01d3cb`  
		Last Modified: Fri, 20 Dec 2024 22:30:23 GMT  
		Size: 996.0 KB (995953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9488332408af61aa2e7a61135828a26e7ff7f717fa70bde8d909b70b04af1e`  
		Last Modified: Fri, 20 Dec 2024 22:30:23 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657a8bfc38b764a7212f11506dd4d9e10889f79313ec41cf604b64985d8ae7e6`  
		Last Modified: Fri, 20 Dec 2024 22:30:23 GMT  
		Size: 1.9 MB (1860217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefb3b4b72f96eb1cc41bc90f9511326598a1821a9d7e3c0f9f3e726cad2fc63`  
		Last Modified: Fri, 20 Dec 2024 22:30:24 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:5c2e8a146500a1d312038f0aef562996839ca864de4d54b0ccb446525bc979f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23bb9fe9bcedf6eac023939f0f1596ad9416a2b368d54147c275b5279e746fd`

```dockerfile
```

-	Layers:
	-	`sha256:31ee527e1bdec24e2dc3c2a0b38b771eef40b93a6f2cc254bafc3ae6f6b42c54`  
		Last Modified: Fri, 20 Dec 2024 22:30:23 GMT  
		Size: 35.5 KB (35503 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; arm variant v5

```console
$ docker pull postfixadmin@sha256:09add6ff39cee9288c169921bb332e4ddfff96addd826503968cfc6fd0cc3847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154120994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7cae3373de5067e4b23e17090037aa2f968646b6fd7f5d944d3da6d03d68e43`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 22 Nov 2024 13:33:57 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 22 Nov 2024 13:33:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_VERSION=8.3.15
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Nov 2024 13:33:57 GMT
STOPSIGNAL SIGWINCH
# Fri, 22 Nov 2024 13:33:57 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
WORKDIR /var/www/html
# Fri, 22 Nov 2024 13:33:57 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 Nov 2024 13:33:57 GMT
CMD ["apache2-foreground"]
# Fri, 22 Nov 2024 13:33:57 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 13:33:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f38f689bfc81a80b77922476ec5fa4c66c3c95c18a88e0d5c163e4f88a3fa2`  
		Last Modified: Tue, 03 Dec 2024 02:47:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1391778530ecd6fb67099da1af9389d8c5e85a5bf4eda9154dc075982c5d03aa`  
		Last Modified: Tue, 03 Dec 2024 02:47:27 GMT  
		Size: 81.8 MB (81799353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1730374a8da7a42b29a8cb7308121c86932f17cf03f72bcbc1157654eab662c6`  
		Last Modified: Tue, 03 Dec 2024 02:47:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d43114e6dacb9dea8dc21a7254e5e88b1cc12a6d007a1431166907121528d6`  
		Last Modified: Tue, 03 Dec 2024 02:51:31 GMT  
		Size: 19.4 MB (19418860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fab695d67cbdff447c2ab807f8900e1d2a4dce642475708bed149bbdd54dab`  
		Last Modified: Tue, 03 Dec 2024 02:51:30 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e205d192900e0b63fd0542c47e1a455fa0a703afa9932fd48ab46e05557439`  
		Last Modified: Tue, 03 Dec 2024 02:51:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee69b59c25d9ef7160325ada4814f43f750ef00d5508783fab3c795a53d0fd57`  
		Last Modified: Fri, 20 Dec 2024 22:05:27 GMT  
		Size: 12.7 MB (12651271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7767fbd56dd24df4ccaa1e48a9c5c0137100fe729e877184aaf4533c438f31ec`  
		Last Modified: Fri, 20 Dec 2024 22:05:26 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba568b5c12606915df49b23d06c1665e3ce4aaf7124a032f9deab725112a7dc`  
		Last Modified: Fri, 20 Dec 2024 22:05:27 GMT  
		Size: 10.6 MB (10622545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae36a267958e17a9f4fa59bc3c359192d77bfa8a5c7cb7696c88bbee738cd26`  
		Last Modified: Fri, 20 Dec 2024 22:05:26 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c18711fd5aa09b7a507242330c5164ae3deb0aef9a1453e2e46b79c0064cf50c`  
		Last Modified: Fri, 20 Dec 2024 22:05:27 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8043e02ca03422d26cb58b890861be8cff1ee0b97caa2f0dd58a88a8427edd91`  
		Last Modified: Fri, 20 Dec 2024 22:05:27 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616fc961d4250224e189f288fb39492fe873da928dd0e46adc4a759d587238d5`  
		Last Modified: Fri, 20 Dec 2024 22:41:44 GMT  
		Size: 1.1 MB (1065454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2802a0f8df98436189d7e725439ece30c9ae86497692368c700953bb1f86e3a9`  
		Last Modified: Fri, 20 Dec 2024 22:41:44 GMT  
		Size: 933.2 KB (933193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07bb600d876efc47930b6b496636d24110254a8974fb5e9fe8993c3fe862d327`  
		Last Modified: Fri, 20 Dec 2024 22:41:44 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b905cd90e8de0c675b44467fa8313b364d46621ecd435e12ad046ffdf823ca00`  
		Last Modified: Fri, 20 Dec 2024 22:41:45 GMT  
		Size: 1.9 MB (1860209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e670a2bfbd8fff14bebe1378deac73c1225615bc6a7644b49603b6d837ab78`  
		Last Modified: Fri, 20 Dec 2024 22:41:45 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:9a31e450cedab35ddf3afc273270435aa4bb97582d1cb5ac4adcbe4c32fb1ab0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47a63cf50b9b4c44193252e96e9ed054f1fe4471607521a2b4cd6696dd2b9185`

```dockerfile
```

-	Layers:
	-	`sha256:ab009de48ed59603a2ca9a83b351c7e082037861eebf765e58d5e9f4cb729d95`  
		Last Modified: Fri, 20 Dec 2024 22:41:43 GMT  
		Size: 35.6 KB (35645 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:f21cec95e23cd35c25754ee1e4112b30c970154196087f4b25dced2e247d894a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145261497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e1be6fef3f85ab719796412936a0625687b89a4c3abfcf07ed10dc4275cb62`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Fri, 22 Nov 2024 13:33:57 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 13:33:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc399a814abef0b215a25083103b4fcd6382c3040364b6565271bfaad3edcda`  
		Last Modified: Tue, 03 Dec 2024 02:45:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c111bef206c9990ed304a2c9e0dbc3e87552d4023cb73e5796908ce98c5a16`  
		Last Modified: Tue, 03 Dec 2024 02:45:47 GMT  
		Size: 76.0 MB (75969214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c345ebeb8ac614dcc4ff559e2cf2d693ff887d5cb958080625dc4d803abd018`  
		Last Modified: Tue, 03 Dec 2024 02:45:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64247e8882ecb48484c43614c1bd400c9f3fa7ff601a3e74f81606279623eca2`  
		Last Modified: Tue, 03 Dec 2024 02:49:32 GMT  
		Size: 18.9 MB (18857266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:489174183fa221f132d5b3d11e3bf9b32527d04508f03839c9a1555913aeb51b`  
		Last Modified: Tue, 03 Dec 2024 02:49:31 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be5de890f1f55562915effb16f54430acf049d0013e862b5942f473118fe5ed`  
		Last Modified: Tue, 03 Dec 2024 02:49:31 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1dae98941703900f5d67eb628e8c739584759a62febbfde2b5732e0e9937a85`  
		Last Modified: Tue, 03 Dec 2024 03:17:38 GMT  
		Size: 12.6 MB (12646708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575b1547dd67fbc79b2894a9acdbb35c5602751fe946730baeed886d98d317f1`  
		Last Modified: Tue, 03 Dec 2024 03:17:38 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d03b0e112f9bf2399a8653a7f0f7f44f1574d3d30f59e2bbc680bbb1e7efb7`  
		Last Modified: Tue, 03 Dec 2024 03:17:38 GMT  
		Size: 10.0 MB (10039384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac32bf7a783595bf28fad56375a219029164e32c1730bb1f4d451bb468cbf43`  
		Last Modified: Tue, 03 Dec 2024 03:17:38 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce01050756d5b9d200fc8b4a234e85c9655ff0b61d5b74cdef42a54ac82e663a`  
		Last Modified: Tue, 03 Dec 2024 03:17:39 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b99e8de489c2a7c70479fad34915d0f0f085f2c471cd07cd3aa94ee6df3a13`  
		Last Modified: Tue, 03 Dec 2024 03:17:39 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67386b980da7d0d8e194421b9c43c51eab043e65cdf344d5a20c8131ef2ee9d`  
		Last Modified: Tue, 03 Dec 2024 17:00:12 GMT  
		Size: 1.1 MB (1058334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d31874d8a7af37d6ef5dbd91e77c2fefc043f117d4282d25dc73a87816a1c9f`  
		Last Modified: Tue, 03 Dec 2024 17:00:12 GMT  
		Size: 881.6 KB (881617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0f6ce156e366a147f6dcf7078f65148ad3aa11085721a7e2f14f5cc5576858`  
		Last Modified: Tue, 03 Dec 2024 17:00:12 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478077751904af41fac05119e17a9817936b5ca75550d6de2f6bdf17626347d4`  
		Last Modified: Tue, 03 Dec 2024 17:00:12 GMT  
		Size: 1.9 MB (1860213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530b794071fc311e0c500f62ff36ff9e5ab8cfd8a51a8f9c062326c7dde010db`  
		Last Modified: Tue, 03 Dec 2024 17:00:13 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:f25458d3904f746510d4f236b6c45a3cd835a0fef4315075c6e4fb091e424051
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9da35253a5b02c95e995c53d3207fa5edd077d4796cd49484214d2d291bfe50e`

```dockerfile
```

-	Layers:
	-	`sha256:8a09582bb3e917b4348cc64025d982fa9c0344c66b859656395c28eb4dbb8a5e`  
		Last Modified: Tue, 03 Dec 2024 17:00:11 GMT  
		Size: 35.6 KB (35645 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:1fabb40f582e5bdc19c5bff6e24717a349827464ff02a80614434ac57afcac47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174287171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de5c567a3a62fc7d5190604adbf1c21ea1600a737c02428522998855e1b7735`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Fri, 22 Nov 2024 13:33:57 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 13:33:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593b3b5e04c8b4e6110fb0e212055b9c7eb2aaa1cf8779fd681a2462f67111a8`  
		Last Modified: Tue, 03 Dec 2024 03:01:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc980920c054a940b9793a107341acd51b059aed873177ef237579d941f23ef`  
		Last Modified: Tue, 03 Dec 2024 03:01:11 GMT  
		Size: 97.9 MB (97936346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7130ec09764042703bb02f30348dab7ba0380d619963d04ab8ccc9678ca27470`  
		Last Modified: Tue, 03 Dec 2024 03:01:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0487dfea6acc671d5a73050d1cb6d9894d55ab6f79fe82e0916fd83c0ee4c37`  
		Last Modified: Tue, 03 Dec 2024 03:04:46 GMT  
		Size: 20.1 MB (20120928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9970f3d36c66c0d81d84d5b43bd8a643ca7669c83b51b9efe950944e0ae9d6b4`  
		Last Modified: Tue, 03 Dec 2024 03:04:45 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fe821f4633e8a7a268f1b2ee321ff810e3810688d047ab340d79ad5a71f116`  
		Last Modified: Tue, 03 Dec 2024 03:04:45 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361a4309642952cdc346487a3effacb91f3c25526ca46e1fa1ed8a857bff88f5`  
		Last Modified: Tue, 03 Dec 2024 03:32:15 GMT  
		Size: 12.6 MB (12648135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e067713d3bb8bf10e1ccac2aa889ee97dfbbc6ba74efd51b0298d124d23adaf`  
		Last Modified: Tue, 03 Dec 2024 03:32:15 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b8267a65e16f1c67b113b843bd38e16497f2f6db35526a777034c9c2a355b9f`  
		Last Modified: Tue, 03 Dec 2024 03:32:16 GMT  
		Size: 11.6 MB (11640338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80095e87fe8006a1cbe24ff0496d434679a34711f121a035a0f444f555a745cc`  
		Last Modified: Tue, 03 Dec 2024 03:32:15 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39498ca233b715054ed8825ef432138a3cd6ee787078c5a8f4cda9470065b468`  
		Last Modified: Tue, 03 Dec 2024 03:32:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558cf9388e9b575510d5b4af096bb10ebf7daf6c978dd526f8ef0c3f75ebe823`  
		Last Modified: Tue, 03 Dec 2024 03:32:16 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84c1d7ce711aa92f3ff970c033ad05bfebbf9294dd7d2ba555cc724b8ad646b`  
		Last Modified: Tue, 03 Dec 2024 11:33:05 GMT  
		Size: 1.0 MB (1022286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1050332b8db325e6b4c673f5c89389d82792a794f6ae624d9f8d024d1af713fb`  
		Last Modified: Tue, 03 Dec 2024 11:33:05 GMT  
		Size: 984.9 KB (984931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5e03e8af1c073abf47d477d8f4007e19fa896e8a486c14f349181ce7efeed98`  
		Last Modified: Tue, 03 Dec 2024 11:33:05 GMT  
		Size: 8.1 KB (8052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15796526db4816b6d8d8bab2d7dfc95f7ca7146b3f4f71829153f15ad31d6046`  
		Last Modified: Tue, 03 Dec 2024 11:33:05 GMT  
		Size: 1.9 MB (1860213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119dab9fe1bc0b0723d65b05a89acf66a41f4960a29e5006b2fd7be330e81d67`  
		Last Modified: Tue, 03 Dec 2024 11:33:06 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:5787ecc60ea5932b25de2108154e0383e9a9f4107cf7b76bb0d9ac98a989981d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 KB (35695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:702030bdf01891d42878ee02d42aaab8a835840a1ab03121504ee05ab43f4d06`

```dockerfile
```

-	Layers:
	-	`sha256:7a41788434348cfa21738b52449bee4be29e237b330281394ec71dc776022516`  
		Last Modified: Tue, 03 Dec 2024 11:33:04 GMT  
		Size: 35.7 KB (35695 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; 386

```console
$ docker pull postfixadmin@sha256:58906025a347be51400234372130b47d7d02b7b14fc089911de10157b334f756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.7 MB (179651553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a17ee9bb3579df8ccab27d3b3a46a65646fa81d65aaf3be5bc7abf647148197`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 22 Nov 2024 13:33:57 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 22 Nov 2024 13:33:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_VERSION=8.3.15
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Fri, 22 Nov 2024 13:33:57 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 22 Nov 2024 13:33:57 GMT
STOPSIGNAL SIGWINCH
# Fri, 22 Nov 2024 13:33:57 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
WORKDIR /var/www/html
# Fri, 22 Nov 2024 13:33:57 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 Nov 2024 13:33:57 GMT
CMD ["apache2-foreground"]
# Fri, 22 Nov 2024 13:33:57 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 13:33:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d82e9ea3fa65bf8333714b3d9c338b367699c802196732ef90d4b64e367ccd`  
		Last Modified: Fri, 20 Dec 2024 21:35:20 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f933ca6170dab526f92787b71b4cc43a28e8d5c3c311d20f4e4d684bbca19eeb`  
		Last Modified: Fri, 20 Dec 2024 21:35:23 GMT  
		Size: 101.3 MB (101320480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17692ccafa790be39d41cbc7135bc3a12b7671591daae236723e6a09ef3fd653`  
		Last Modified: Fri, 20 Dec 2024 21:34:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f100f1e2887b097466868797db13955baac0d02e598190d74331d22e37283a`  
		Last Modified: Fri, 20 Dec 2024 21:35:20 GMT  
		Size: 20.6 MB (20638499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0495f17ccfc59f1d154dd1c3b597b9a9ac7635b9a7ec6542c443a3b1afb0772`  
		Last Modified: Fri, 20 Dec 2024 21:35:20 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df46ff5a1d55ca593381da11c45faba4564ec005c038a08577943720d8e81c25`  
		Last Modified: Fri, 20 Dec 2024 21:35:20 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6828a771d5d34b23d22124744bfb7be424fa90b4661985fccfcaa432d644fb98`  
		Last Modified: Fri, 20 Dec 2024 21:35:21 GMT  
		Size: 12.7 MB (12652223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d986177f32841f6258ae750064b7cd61549b7864d9f7eb9a191d431dab097a5`  
		Last Modified: Fri, 20 Dec 2024 21:35:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d813f5cee583f5bcdc04c8fa096b928927d232d0c790a7288925b2146330bf`  
		Last Modified: Fri, 20 Dec 2024 21:35:22 GMT  
		Size: 11.9 MB (11868857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6709d5f84b506fdf80cbfc0fcb4ca9bdfb0eb531a7607d788be039facf6b3df`  
		Last Modified: Fri, 20 Dec 2024 21:35:22 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf164e001273c28776d5c4a28151bd616e7d8fab75e3faed7cf28103057ad4d9`  
		Last Modified: Fri, 20 Dec 2024 21:35:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948e948ad837c72ab523d810a161d6f4d9caad65038ac92524b844226a9ff54b`  
		Last Modified: Fri, 20 Dec 2024 21:35:22 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7019502a63475a41c9d6da90c0042d9b142e5320893bb292c2e14accb72c754`  
		Last Modified: Fri, 20 Dec 2024 22:30:18 GMT  
		Size: 1.1 MB (1077068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70ad0e68338bfe794429d39c3be141bd78be5066582d94867324ddcea969a86`  
		Last Modified: Fri, 20 Dec 2024 22:30:18 GMT  
		Size: 1.0 MB (1013550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35d0ed8c2d2e4d009e1d17dcffa1df6ecc6944799694acb81545b58b6034ee1`  
		Last Modified: Fri, 20 Dec 2024 22:30:18 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029ef1a699314633e11a632e7dd5021481eabba5b2c9acd90350a13f408c47de`  
		Last Modified: Fri, 20 Dec 2024 22:30:18 GMT  
		Size: 1.9 MB (1860213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e822ee74bbc85c3f82046df517040c12f8d95d967ca179c0417582ad27af3343`  
		Last Modified: Fri, 20 Dec 2024 22:30:19 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:cc71c52f87fe47819c911fd204c981366acf367f29ce0d37ca2109e6baeed79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9322a692c12867483a109ff06422aa03efb461d078793e129fbd1dbfba5784d5`

```dockerfile
```

-	Layers:
	-	`sha256:d39e2da5f469585e3576d3ccb71a373aa96cb08bd5365862061a2744bb637638`  
		Last Modified: Fri, 20 Dec 2024 22:30:18 GMT  
		Size: 35.5 KB (35450 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; mips64le

```console
$ docker pull postfixadmin@sha256:99da8582b402298ab2e952bc8ced5e7dc473f81106207243611c61fddb58a76d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156226906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f326dce1bf42e77c29f3fde3744572e3716fdcede877e7c9a02d136d87f344cd`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Fri, 22 Nov 2024 13:33:57 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 13:33:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697b6f869e689f1f7935effcea7aef7505ad04025b0311ff3937b9103eef46fd`  
		Last Modified: Tue, 03 Dec 2024 04:22:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b7f48524d255d2a114c61e2dea94f3576d2144432398eb626ed6bbb8da968d`  
		Last Modified: Tue, 03 Dec 2024 04:22:41 GMT  
		Size: 80.5 MB (80475126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7c3c34315ea9a93e65cc52bfdaf45d8f691045833035294baddeaa21df2439`  
		Last Modified: Tue, 03 Dec 2024 04:22:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df91c5aff622eeb49d30bc53aeda928e25ca30d9809e0caf1fc0dbcf6aec00dd`  
		Last Modified: Tue, 03 Dec 2024 04:42:14 GMT  
		Size: 20.1 MB (20069109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1873dc58b3bfe6549f8fd226713fa111f41803622dcaa71518533d1ab7f287`  
		Last Modified: Tue, 03 Dec 2024 04:42:11 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1faa97de501943d58384491dc09430289a7e70957ada9f084524d32187e90f64`  
		Last Modified: Tue, 03 Dec 2024 04:42:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086bec4646d1fe7c30afdda8bba2ace7b4ad4cae1e29698e857ad093548b3787`  
		Last Modified: Tue, 03 Dec 2024 05:53:47 GMT  
		Size: 12.6 MB (12646486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c39f01ec4e8beb6ec481c66348428c0978f4c4e3fe488cea9118707fbfef2d`  
		Last Modified: Tue, 03 Dec 2024 05:53:27 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6151c1d5e70b934c7ad2a723bad2a5fa99ad2a9bd62dc351695764aeec6b3754`  
		Last Modified: Tue, 03 Dec 2024 05:54:30 GMT  
		Size: 10.7 MB (10723164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6e59901856c4567a5f6d3c01b56ff9fb0d7b1891f56f82882c4cd178026a9`  
		Last Modified: Tue, 03 Dec 2024 05:53:27 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31d22511c5559be8defa32ac1e4157850ab5e2f9ed0eea6560edc80675fbde`  
		Last Modified: Tue, 03 Dec 2024 05:53:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b7880ee2a01ba14309b9bef4e9138157568c241edf02934b3a7e9d2b2d6dfc`  
		Last Modified: Tue, 03 Dec 2024 05:53:28 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528341be8716bb31b5f7607bbfac108acfffbe91bbbf0e4ae9ce69297e424767`  
		Last Modified: Tue, 03 Dec 2024 22:12:09 GMT  
		Size: 973.6 KB (973649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c9bc9337afb16bc330cbae34d0a9bcad365f6c9b982b7186013bc80ec338d`  
		Last Modified: Tue, 03 Dec 2024 22:12:09 GMT  
		Size: 958.1 KB (958062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60596008dcf042a9ae9a511302a86d6b95924d4f8ac0ed5a27ca4dfc68aec81`  
		Last Modified: Tue, 03 Dec 2024 22:12:09 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415de2caf3b7b98bb2efc1bbc9c5223c895b7f03f3a1ee678c4d1e4d04383b61`  
		Last Modified: Tue, 03 Dec 2024 22:12:09 GMT  
		Size: 1.9 MB (1860213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856c7156a829caa7910a45699e2b54633d694af6ff536366aeeeb1c8ff8a021b`  
		Last Modified: Tue, 03 Dec 2024 22:12:10 GMT  
		Size: 1.7 KB (1657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:9675be18d926a4982decb74114b61d19b9bd1af42ca8f1956858a1b9865767f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaef6eefe16448c325e9157d0797afdee7945f1490e680ffce98874ce7604b0`

```dockerfile
```

-	Layers:
	-	`sha256:9b92ef5f02705c0a9531fc18a410e6db9fe1c6ed1421ebbb7016a6c9bb9e7f2c`  
		Last Modified: Tue, 03 Dec 2024 22:12:08 GMT  
		Size: 35.6 KB (35604 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:c3d75bbbf7e81cf3ee357ce5d8c8bea1161b765f61c1bcbf688b5434b2fb895d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185224523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981890f0162153f1d5345e4302ebbf9ce54e3e2005e5a7d9b2b1ce81dc8e50f0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Fri, 22 Nov 2024 13:33:57 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 13:33:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfd0832c6742842354605a68e1c37e01805dbd8dcb42bed521f3b5ffc9d6782`  
		Last Modified: Tue, 03 Dec 2024 03:01:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8241edc102752205916990cef5c543934549ef471e4363e3f37b4d609359e`  
		Last Modified: Tue, 03 Dec 2024 03:01:42 GMT  
		Size: 103.1 MB (103128469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe6a6422bc6eb2d0ecc0d78cfc1ccb6571b1ef03bf7b17f2384e77abef0c849`  
		Last Modified: Tue, 03 Dec 2024 03:01:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be563cd21515e56438eeee24e165c5e6eb1efe06f45df830dbb193247c929683`  
		Last Modified: Tue, 03 Dec 2024 03:06:23 GMT  
		Size: 21.3 MB (21308386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34863b54186af36b092695264d86f35c3119978d70427455e85f6fd279681048`  
		Last Modified: Tue, 03 Dec 2024 03:06:23 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7b95b58340fb918a89b18f660a1045c0f902984f4cae1590b337184e865c1a`  
		Last Modified: Tue, 03 Dec 2024 03:06:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36b12ea7855a4f5cc02ab5a21fed90aa6fdeb8e172e9f5ddb12207361aadb10`  
		Last Modified: Tue, 03 Dec 2024 03:22:58 GMT  
		Size: 12.6 MB (12648026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d9cf2577947f916a49bf8b682cd00ae9273a794be7c758adb0aca2d8f5ae709`  
		Last Modified: Tue, 03 Dec 2024 03:22:56 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e3a15fca22dbd0f787bc2c706234ffa6cbefbd219aba99588302ab2f085e8e`  
		Last Modified: Tue, 03 Dec 2024 03:22:57 GMT  
		Size: 12.1 MB (12064217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4dcd2cf193dc764293a488a6b7948c1e45c21572293bd9ccc9d627ff87fa8e6`  
		Last Modified: Tue, 03 Dec 2024 03:22:56 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf630f64cdf4c64eb83d88b5b604f18f9f3502cda5357559624fe6df4cc677e5`  
		Last Modified: Tue, 03 Dec 2024 03:22:57 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2711004d906b8d821b04608d575be9905c6e99c496f5fb22e0e8f2b6ce6cd1`  
		Last Modified: Tue, 03 Dec 2024 03:22:57 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b263d82e230e4bf5d3f8066c8a8a5287d13ddb7070888f87f10109fbbe5e7e5b`  
		Last Modified: Tue, 03 Dec 2024 09:14:21 GMT  
		Size: 1.0 MB (1009346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21100b0dc3cb59a25aff672c79e370394fa76df20b5243c315ea9ab0bd12ba98`  
		Last Modified: Tue, 03 Dec 2024 09:14:21 GMT  
		Size: 1.1 MB (1127420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8cbbe8c579f1aff5baf9783bfef57cd845f57ac25ddc826555a6a7a2c7dcc6`  
		Last Modified: Tue, 03 Dec 2024 09:14:20 GMT  
		Size: 8.0 KB (8046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6f6f01235ceba844c0e3b6af31744e052cdc8e1508890afd76d75aab6d6e0a`  
		Last Modified: Tue, 03 Dec 2024 09:14:21 GMT  
		Size: 1.9 MB (1860215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659eadaeb07e625f236fe6e7ec06da580831f2cfb3be9fa96d6df25349357de0`  
		Last Modified: Tue, 03 Dec 2024 09:14:21 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:0f0e54ec203387831a0c1d1444fccb2504957891b904852d00c30376144a922c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b32cb1aa1ef7fc1d50e8099f0ad412938cc1d0b5173dcd345ed62ae942a8146`

```dockerfile
```

-	Layers:
	-	`sha256:68157b1f50497bdb3f24931e7d929113e1b92b061bf9e9c622b32954ef7bad32`  
		Last Modified: Tue, 03 Dec 2024 09:14:20 GMT  
		Size: 35.6 KB (35582 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; s390x

```console
$ docker pull postfixadmin@sha256:4b3961cb879fb849a6189efe3961ce817f74625911a82334bebc8294eafd6e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154830771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1762aa6a0520c6b9fda7111422c3db159a1bea66e232774efa969d1a05d8de2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Thu, 21 Nov 2024 06:31:33 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Thu, 21 Nov 2024 06:31:33 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 21 Nov 2024 06:31:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 21 Nov 2024 06:31:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 21 Nov 2024 06:31:33 GMT
STOPSIGNAL SIGWINCH
# Thu, 21 Nov 2024 06:31:33 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Thu, 21 Nov 2024 06:31:33 GMT
WORKDIR /var/www/html
# Thu, 21 Nov 2024 06:31:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 21 Nov 2024 06:31:33 GMT
CMD ["apache2-foreground"]
# Fri, 22 Nov 2024 13:33:57 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ARG POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_VERSION=3.3.14
# Fri, 22 Nov 2024 13:33:57 GMT
ENV POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
# Fri, 22 Nov 2024 13:33:57 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.14 POSTFIXADMIN_SHA512=18837c112e08f3a7d41d829d2f26f5e791d5a0b9b8d0ac458d9a266f5b1aac2f0d9e6b7ebec0c5324ac54d944ba81cba210b2cf82075bcf7ab588c7d96eb49fb
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 22 Nov 2024 13:33:57 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 22 Nov 2024 13:33:57 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff6d88ca75be60fd842318e38796161d90dc699ddefddb72e584661cafccbb5`  
		Last Modified: Tue, 03 Dec 2024 02:45:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1972b1cde205ce78e000379a6f103cc814e05cf048628db71370f4268b574`  
		Last Modified: Tue, 03 Dec 2024 02:45:10 GMT  
		Size: 80.6 MB (80624347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0df81e218837c9a0821f00169675df65b6dc92a07a5e60fb03eb1b30c73673`  
		Last Modified: Tue, 03 Dec 2024 02:45:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81785c5e81e41257e9343844a3bb03f7c6b683f55e2dd07969f24adcc528917d`  
		Last Modified: Tue, 03 Dec 2024 02:49:17 GMT  
		Size: 19.9 MB (19895239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b912aab84041841b2de0edb1264346e4f5aa519009fc0ab560ea1b76d041e127`  
		Last Modified: Tue, 03 Dec 2024 02:49:17 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ddea8579f46dc94efa149af85f249d1131297e7dcfce941798a62873eb5745`  
		Last Modified: Tue, 03 Dec 2024 02:49:17 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7a019423bbf4924612bacdb4fb32961bae808beb1a6bbbb0a2b2351d70f4632`  
		Last Modified: Tue, 03 Dec 2024 03:03:57 GMT  
		Size: 12.6 MB (12647106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b58be623527e52c6268e1bc48178a69489a19d8ca7947e04e7225ac949ce9ed`  
		Last Modified: Tue, 03 Dec 2024 03:03:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944f5ab62e81231588ee6d2e4bfe7f5e8ccaf646e6382c8c0a6c4447c67bf5ce`  
		Last Modified: Tue, 03 Dec 2024 03:03:58 GMT  
		Size: 10.9 MB (10867061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c246e2709d2d338dc489dae54e12bb063c07ebe0647d6178ff5ba45c4c9897`  
		Last Modified: Tue, 03 Dec 2024 03:03:57 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c394ca57b6cc143ad4697bc1bf77b7409d239a324c0ee8f61a501d0073411e`  
		Last Modified: Tue, 03 Dec 2024 03:03:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0841cee2fbbd72ff56980fef3c1e955bf863b1a442877d8eecad48198b1c029f`  
		Last Modified: Tue, 03 Dec 2024 03:03:58 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbde73c3344831b8e05c639d827da6c067f2333ebfbc6715c415b5855411af12`  
		Last Modified: Tue, 03 Dec 2024 07:39:18 GMT  
		Size: 1.1 MB (1057655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4e968a276042e7763d8cd596c7ba642471a1e819caca40ab5381de1804992f`  
		Last Modified: Tue, 03 Dec 2024 07:39:18 GMT  
		Size: 985.0 KB (985001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72e248c878301c7ff9c1804193f16bfe94e33fb92719a7485db04fddc9128ac`  
		Last Modified: Tue, 03 Dec 2024 07:39:18 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9a12a937662862ee4c5d5ec51d5419266fe6a04a9b6d00fde0439143344a6c`  
		Last Modified: Tue, 03 Dec 2024 07:39:18 GMT  
		Size: 1.9 MB (1860211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0213a5fe46f310cb5007f1167e06a28e20fea8c9dd0a7baebba9680c8b6f5267`  
		Last Modified: Tue, 03 Dec 2024 07:39:19 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:858a66158e3eefb829ac6eaaab3b469b085c2b9bac656afce17fdbd3708a3688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b689b8d42ea471640a97a18516edd58810d650c9235703a823f8959f9b033cf3`

```dockerfile
```

-	Layers:
	-	`sha256:53a33874f5af36eff1ab1bf2b37e020dd00420bef45d396f8eae0b2939918446`  
		Last Modified: Tue, 03 Dec 2024 07:39:17 GMT  
		Size: 35.5 KB (35498 bytes)  
		MIME: application/vnd.in-toto+json
