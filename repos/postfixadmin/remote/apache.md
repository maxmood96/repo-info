## `postfixadmin:apache`

```console
$ docker pull postfixadmin@sha256:d793f55e3bffcbad1f7d308ceb80cc7c037d935ec74a71ce1a45b93386f8e320
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
$ docker pull postfixadmin@sha256:bab288144a34d8eed39b51355b02b897db7dacfa6c1dd4ca0d1b5475be78610e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145267693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb83c57f70c4e5444cf7ae000770f32eda18215dbcdd4058841dce78df367ad`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 22 Nov 2024 13:33:57 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
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
	-	`sha256:0a10c3dc90f3767d3a56c300190a46410061a5e1b99b5139b2186f224838ae61`  
		Last Modified: Fri, 20 Dec 2024 22:47:47 GMT  
		Size: 12.7 MB (12651230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dc3eb524a3e7f4f08956a3446e4de08974f6e3f385c4db824ec91418b1bb46`  
		Last Modified: Fri, 20 Dec 2024 22:47:46 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a19136f0353b9168e79b275c908434ca123945fe7826fbee0a2c82ca7ad206`  
		Last Modified: Fri, 20 Dec 2024 22:47:47 GMT  
		Size: 10.0 MB (10040982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b86c216fce11952606c23ff6d34974efa92a474e79a4fecbbfbd25640d054c`  
		Last Modified: Fri, 20 Dec 2024 22:47:46 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43297479fbf2182e793b9726a1262e6e89750d5b9534155726e4f48fd5084393`  
		Last Modified: Fri, 20 Dec 2024 22:47:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3498a92def282a61e5bd1b8e4d6ceaa1ab22835094e2dbfb11be7bf5b3432b84`  
		Last Modified: Fri, 20 Dec 2024 22:47:47 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b5041f91c3bb54d1ce2e221ba1eea886d8359933489900836568e66d68c0eb`  
		Last Modified: Sat, 21 Dec 2024 00:35:19 GMT  
		Size: 1.1 MB (1058377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ddc7a2c0b63150dfcc3174a88f69fca97649464d8b322e0ce3785f8b11d5f5`  
		Last Modified: Sat, 21 Dec 2024 00:35:19 GMT  
		Size: 881.7 KB (881651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1c70685a6a1a620faa088262389ada4df39a42bd66c74b5b1ad55786441805`  
		Last Modified: Sat, 21 Dec 2024 00:35:19 GMT  
		Size: 8.0 KB (8045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc481ef050af5b802b0f3561db7570d9232d35cb4dafb98614800ec2a0b82cea`  
		Last Modified: Sat, 21 Dec 2024 00:35:19 GMT  
		Size: 1.9 MB (1860209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:547d9be2b9adbdbe1c69cec3460ce174be324fd043a2f918e55d03a116d67d45`  
		Last Modified: Sat, 21 Dec 2024 00:35:20 GMT  
		Size: 1.7 KB (1657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:05f98701321bcde70b63b81560212deda7380ee47ecfb54d12b1f6e0e52d4dd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ededeab50bc4371eb48a05e128d5fdd0302e6cae3cbfa26844c17e993066fcd`

```dockerfile
```

-	Layers:
	-	`sha256:3940b9672c66656290978882cc06171a9214ea5a81fcedcd4dc830d984ba3ef7`  
		Last Modified: Sat, 21 Dec 2024 00:35:18 GMT  
		Size: 35.6 KB (35645 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:43d790fead21182e92cad108b987b7d07a82e21107892ce62b562de045dacce5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.3 MB (174296794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc99b76086beb6521f20c7217585c97cbb292cf3ca0c740f51a5910e0ff2b8f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 22 Nov 2024 13:33:57 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:2c9244721bd3d7431eb0e28a4765d6a5585c0013c4a61a9ec6e5307abdbf6215`  
		Last Modified: Fri, 20 Dec 2024 22:28:33 GMT  
		Size: 12.7 MB (12652979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97b1eeb0d6a7a99b7d7d39ea96e9837990a764e816640d92740b7731a02c1fa`  
		Last Modified: Fri, 20 Dec 2024 22:28:32 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c647faa7e38699e19383a442c920dc09411e7842c85e7d3f4c21bc7971b498d`  
		Last Modified: Fri, 20 Dec 2024 22:28:33 GMT  
		Size: 11.6 MB (11645110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a5ca9209478d6440afab0c74fe8491a0741f34ed1e53ed9c5795b08dacb9b8e`  
		Last Modified: Fri, 20 Dec 2024 22:28:32 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0783ad255850e728d9522cb6b8ed362ee58122adbe010fb035c9538c5ffac83`  
		Last Modified: Fri, 20 Dec 2024 22:28:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d4fd06adf5aa986a77d3107a0647bbed53ee4fb87d537d374203b56ec9f6dd`  
		Last Modified: Fri, 20 Dec 2024 22:28:33 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88debe4a6f9aee152dae0c83a57f2ca452342419f6d9978f3d316e66c0b392f6`  
		Last Modified: Sat, 21 Dec 2024 01:15:38 GMT  
		Size: 1.0 MB (1022299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0d0eb02cbcba6d06f634a2acf996e3838477b9cef35fc2271a4636ae6b57b4`  
		Last Modified: Sat, 21 Dec 2024 01:15:38 GMT  
		Size: 984.9 KB (984922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3d5d0ecbfe12262801b562aaad49bccc2d0e9a650634023bae59e764d33604`  
		Last Modified: Sat, 21 Dec 2024 01:15:38 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4285c1f49c477c7b07a0c19915e30d46075e4a2cd2939e5e636527b092a41b62`  
		Last Modified: Sat, 21 Dec 2024 01:15:38 GMT  
		Size: 1.9 MB (1860213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406e9e55cead873d45cb5226ff61ceb2b54d1f1ced936ef344ed5f44d3b5a235`  
		Last Modified: Sat, 21 Dec 2024 01:15:39 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:e923adeeb432d4d8f51a928bd0ea00c248b389cc1a2af33da14051cd9bcf50a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 KB (35695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8153c22b143a0aa676415f9425319824500727c30c7950d81e8a91c0c3e585a0`

```dockerfile
```

-	Layers:
	-	`sha256:aac846c24a679e300433551fc9f2f640387a8f9dfa230dae0f0cf8d728ba1533`  
		Last Modified: Sat, 21 Dec 2024 01:15:37 GMT  
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
$ docker pull postfixadmin@sha256:a5575ddccf3f69df624bd9a6e0b66b1387765af16517795b7bfa3256661e59e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156230443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41b3eb5d04b39785bd62e48c0678808c670de697bc7840f59a89850c6f44fe7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 22 Nov 2024 13:33:57 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
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
	-	`sha256:3a00b2761eb2ee61a0f5e9de74aeb55b45c5e9253e74a1a94de50c5173a0d82b`  
		Last Modified: Fri, 20 Dec 2024 23:17:33 GMT  
		Size: 12.7 MB (12650944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc345af87c730c7fbc0752a0d7784f3056f853ba59fba6f578d9b60dfc8a4b8`  
		Last Modified: Fri, 20 Dec 2024 23:17:32 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bde5ccee86eb80e194010bf594ae1561fa2780fef3f5ea822807964efc3a341`  
		Last Modified: Fri, 20 Dec 2024 23:17:33 GMT  
		Size: 10.7 MB (10722042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1845c637d84299e1c92fc8c217f2620bd30376779434944581ff4f21ab464a9f`  
		Last Modified: Fri, 20 Dec 2024 23:17:32 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6211016ecab13315a6debc9874bcdb246ec36502324ac104bb2e0e5cf06943`  
		Last Modified: Fri, 20 Dec 2024 23:17:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973b2058a9c01f40645217e120b89ee95462c0fa4c546b2185f8cc3ffe7d712c`  
		Last Modified: Fri, 20 Dec 2024 23:17:33 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb221910674c6809ccee5316f97c9d132959e10257e1b047a6e7d16655271c9`  
		Last Modified: Sat, 21 Dec 2024 01:00:35 GMT  
		Size: 973.8 KB (973762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d9e5191487302b9e96c4eaca0e2445458e296d190dadf42bfd55d9c226ac8a`  
		Last Modified: Sat, 21 Dec 2024 01:00:34 GMT  
		Size: 958.2 KB (958151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c085b90f2084f324537a6692b8e0851acc81727038ff0ab264d868084a542cc5`  
		Last Modified: Sat, 21 Dec 2024 01:00:34 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5204ede4afc0892270a5667075264443efa5ddb011a4c7d797115885e12e4e40`  
		Last Modified: Sat, 21 Dec 2024 01:00:34 GMT  
		Size: 1.9 MB (1860211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecf584617c9becaf43e0d0e129774a630254a5f84e5b8f04cad82f29a7b7dae`  
		Last Modified: Sat, 21 Dec 2024 01:00:35 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:2b4285f9a45963081f8e146367225b248c1e77b2ccd5c5cc7ff233148825fcc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f877baecf53fee6cfc646f27ade94e848e7ebd87ad2c373d6ac41d7a5200af`

```dockerfile
```

-	Layers:
	-	`sha256:5fac17d2205bd9482633bd438cc1beef428a2ea07a491c4bb282affd52e81cb9`  
		Last Modified: Sat, 21 Dec 2024 01:00:33 GMT  
		Size: 35.6 KB (35604 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:683d02782545a66c5e4cd7f03271d21fd64866607a12b70d59c815b6b5832f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.2 MB (185231715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceacada9fa1c9ba4f3be5967751835cdef5bd7f4937bfe68c9ca2732f0257731`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 22 Nov 2024 13:33:57 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
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
	-	`sha256:2bf0913f25d18b26ad26f4ac8d7bd629b06c51b40b26818a6d00e5b659a2783d`  
		Last Modified: Fri, 20 Dec 2024 22:13:45 GMT  
		Size: 12.7 MB (12652633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1969658d0fcbe74e6caabbacfd229c70812ac865e87f3faacc452cc50138470b`  
		Last Modified: Fri, 20 Dec 2024 22:13:44 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b9a1d2272e74544b53318db92c4af48be06739469248efad4a608f9179415a`  
		Last Modified: Fri, 20 Dec 2024 22:13:45 GMT  
		Size: 12.1 MB (12066994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4de032c6529e54afbf2d8baff3a815e8af2bd4d38582eadf6acab0ba20489b`  
		Last Modified: Fri, 20 Dec 2024 22:13:44 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7a2b16b371551862e8768422ab4f0187150782d3c09f210dd98feda35a751d`  
		Last Modified: Fri, 20 Dec 2024 22:13:45 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05677d66e1a42a43edd50ef79f03f499b6a2f24968dd39868df813177da71d0`  
		Last Modified: Fri, 20 Dec 2024 22:13:45 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d373813ef0c0cc75a5fb95925d7f6698b2de89543d9d5befbe6dd83abac788b3`  
		Last Modified: Sat, 21 Dec 2024 00:15:02 GMT  
		Size: 1.0 MB (1009264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0936e4187215a39e56146c360e3fa9519c79af936fcb013cd87905217cf6ba`  
		Last Modified: Sat, 21 Dec 2024 00:15:02 GMT  
		Size: 1.1 MB (1127297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7df19c9aa1c13c419f7a6fb3fc8f5ff4c3ac8688f4ac4eb6f4ff38ec937e42`  
		Last Modified: Sat, 21 Dec 2024 00:15:02 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:775631c7bc392bd12856e958fdb923a26891f53aa0eaf0fb8044150d4ea80cec`  
		Last Modified: Sat, 21 Dec 2024 00:15:02 GMT  
		Size: 1.9 MB (1860214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402450f911bc790706c45679c60881998a09bb5471b7f0483ed5200a826f781a`  
		Last Modified: Sat, 21 Dec 2024 00:15:03 GMT  
		Size: 1.7 KB (1657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:1fc40da99346f2cb6d1589b29484328e304ed898b5f207be1500bd90ba3dfbb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61715d8cba7704f96738947a8e1d46b0ef4ad0a53c6ac79f8a817e7392bcb52`

```dockerfile
```

-	Layers:
	-	`sha256:ee03a332733882fdc6615e58e48ebb5e49c64a0f4ef646a30dacbc70a2248b03`  
		Last Modified: Sat, 21 Dec 2024 00:15:01 GMT  
		Size: 35.6 KB (35582 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; s390x

```console
$ docker pull postfixadmin@sha256:7cb5c64e6c94c8aaf805e041395ff0d93e752eecd5997933c2e297009a6f5670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154839380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07536e1e364ddb8e1f911be5112daa829b3e0a3d9c7d15f71bc27ef4ac4d42e6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Fri, 22 Nov 2024 13:33:57 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
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
	-	`sha256:46f52b7e6884c1b774e8a37167d61e6685bfb7d77ccc425abec49e126e4e4846`  
		Last Modified: Fri, 20 Dec 2024 22:27:31 GMT  
		Size: 12.7 MB (12651643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6f9945bf2f022783dda71bfb41503662f267072d1210dc40d5e047b767ca2da`  
		Last Modified: Fri, 20 Dec 2024 22:27:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e117719991b46346cc1da954175d888e8ce6f63a6d261e1d65e9978409a36ca`  
		Last Modified: Fri, 20 Dec 2024 22:27:31 GMT  
		Size: 10.9 MB (10871199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cde513f896dcdc52826df0efc8cbd408ee4e9e14ce35a5d38371e8b29b85e1a`  
		Last Modified: Fri, 20 Dec 2024 22:27:30 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b050ecd71c013d0f3002c795226fd459042d995281cbca80d781b070ad1e4b37`  
		Last Modified: Fri, 20 Dec 2024 22:27:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c14a268257348641a0e305233a89f401b15b833a7f65962bbd3fca99056d2c0`  
		Last Modified: Fri, 20 Dec 2024 22:27:31 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdaa382ebde9e92130b9dff0b206d5647c42b5a3045326a4924215700abc657`  
		Last Modified: Fri, 20 Dec 2024 23:50:12 GMT  
		Size: 1.1 MB (1057617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0313e73bbe4a3d1e019643914cafde52405c55c2881217462f771cd3323636`  
		Last Modified: Fri, 20 Dec 2024 23:50:11 GMT  
		Size: 985.0 KB (984960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385dfe77e80cfd526d7cc6cbecafba985d8c4deb1f456e3abb8564568aa74ffc`  
		Last Modified: Fri, 20 Dec 2024 23:50:12 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe4ce1a4264be0e682ad0e85b910073bae454d0d517c68015dd138b238ac65a`  
		Last Modified: Fri, 20 Dec 2024 23:50:12 GMT  
		Size: 1.9 MB (1860211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7884d72285b4cbe627bd928cd0a375f90981ee8dd526fbb6a6bdbea9f38f5758`  
		Last Modified: Fri, 20 Dec 2024 23:50:12 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:cb627226fa1f765a73bbc6c86645667afbbbe47c6529a7ecb2fb450d36144c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1e24a223d13ec845603ff9d935051311df04a651dc94cd7d7de33bd5888554`

```dockerfile
```

-	Layers:
	-	`sha256:c96caccc6cab007004e6badcf315bb4740b7df71db9c913d01d9a5a1282fe873`  
		Last Modified: Fri, 20 Dec 2024 23:50:11 GMT  
		Size: 35.5 KB (35498 bytes)  
		MIME: application/vnd.in-toto+json
