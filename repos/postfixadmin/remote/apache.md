## `postfixadmin:apache`

```console
$ docker pull postfixadmin@sha256:27b9e3f6b734ee11abc8b6710098f397fbba37b8bb22b6de46db3bae6b0629f8
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
$ docker pull postfixadmin@sha256:c43e7a028b826ee529254d399646da54ec0a6f21457e78bec79b3797254f9487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181016637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ef627dc84b838d666dabe22c06fc2273925d9a1db3d4b1c8806b5b53f668e9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.23
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGWINCH
# Sat, 21 Dec 2024 02:12:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[80/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a26209085cd1cce5de1a7d664c618fbf4f5e5fb13a2a77aef150e8025d962ab`  
		Last Modified: Thu, 03 Jul 2025 23:11:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2654ecca65df76b9d9f0c366ba5da322050a5815dd5d7545664a00cfc8a3022c`  
		Last Modified: Thu, 03 Jul 2025 23:03:56 GMT  
		Size: 104.3 MB (104331328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56f7760a27b3d3d1f01930f338f6bac23746221c20e8040c085499ee34801d3`  
		Last Modified: Thu, 03 Jul 2025 23:03:33 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a211c9717574696dc7ebce1696c0109a46236a84da3fe6d8c46c6ee7f5648be9`  
		Last Modified: Thu, 03 Jul 2025 23:03:51 GMT  
		Size: 20.1 MB (20123815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393d07ddf4d99be3bebd5370efbebb6a38d0ae7aeed5776cff69ca7b134eb260`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6346f6b34eddbf80aad674100182224de5de0a7551ba38ddb9b57ec44c20d7ba`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77fdcc46ec0840b404cf5d3706ceaf26119499b6a0907845e1c3ec7d8c2779b`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 12.7 MB (12706476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86287894cf98f90492aa4259cff7e0413c108ba525e54bd5f0dcf21c13ce7340`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce089e67acb7160982b69bf54c730bc996696f6931dab8db5f9c72c4b37f583`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 11.7 MB (11658498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b1dc46c5e6191fe0a137399ce9c49be6ff0565f2d8099dbde3b81798bda997`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f2da87ea27ab8683f8de86a54843f44716f69e8d026a3937997a68507e48ed`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fbcee9efb268dd6a9acec79dd139d174282f0f7f2d35c6fbe16feda9f3daf7`  
		Last Modified: Thu, 03 Jul 2025 23:03:48 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c75ef7b928a71240bcea048ff30e4a2eb501f68095713bad430d17d52ca9165`  
		Last Modified: Thu, 03 Jul 2025 23:03:49 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74af6633c424102cde1d5d1e0ca24f42e6495759672a3df509b092ac63b4c83d`  
		Last Modified: Thu, 03 Jul 2025 23:12:05 GMT  
		Size: 1.1 MB (1092578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabea100879a5fe1a7c70c3bc4dac7fd6049682983120d393fe4bdd886160d85`  
		Last Modified: Thu, 03 Jul 2025 23:12:06 GMT  
		Size: 996.9 KB (996904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e071c4803099b37569899aac183ceea6fec8ea6636364529ea0d942363a205a0`  
		Last Modified: Thu, 03 Jul 2025 23:12:05 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef79f21d2a53a20c59eeeeacbb27192cefcbbf467bc1c0e3063527fe0cb37be`  
		Last Modified: Thu, 03 Jul 2025 23:12:06 GMT  
		Size: 1.9 MB (1861471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6182d3959865598805d7df88387a457a1507d7f5912949f95e0f34b11db93546`  
		Last Modified: Thu, 03 Jul 2025 23:12:06 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:d4ddcf90cca41abbe2a873b66c63b5025992b3f636ae2b3ba78142c5cce0d391
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63075186b4522146dd8dc6c24393ffa4fa985c3cc939dcda43e88f52744f84e4`

```dockerfile
```

-	Layers:
	-	`sha256:5d44d6bbba821dd0256e8ecba232d2e714243a9856692aeaa1f658f0d9ccebb9`  
		Last Modified: Fri, 04 Jul 2025 02:10:31 GMT  
		Size: 36.4 KB (36428 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; arm variant v5

```console
$ docker pull postfixadmin@sha256:dd93b25ab76d9277b447652aa021f48efbe245a868737b779cad7568360a1705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154365447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bc255e8af4f5ad433adf65fce33c26067744bc5d8958cfb5197e279d962cf6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.23
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGWINCH
# Sat, 21 Dec 2024 02:12:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[80/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b05322491f7f224fdb6afd1a4feb0c269fe0910bd44e82e37a846aec3e465c`  
		Last Modified: Tue, 01 Jul 2025 03:03:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b493a89b33667d984de07320c027ba0599d73427f434c8ec42c944a6bd4aa`  
		Last Modified: Tue, 01 Jul 2025 03:03:27 GMT  
		Size: 82.0 MB (81973614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef43b7ed80f2af53848f0179316741b5f6d73203876a5f0f62b038d570f6c8`  
		Last Modified: Tue, 01 Jul 2025 03:03:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1601706ea1ce67f559cb97c579c16dd941d3841c0536aea9a41a8892de970a15`  
		Last Modified: Tue, 01 Jul 2025 03:07:29 GMT  
		Size: 19.4 MB (19418152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc8e91d03bdddc0ecb98561647c397edd946b0e408f3e4b937dd86f102157fe`  
		Last Modified: Tue, 01 Jul 2025 03:07:28 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8793820eb88ba267b7037f6242d4786a223433f5744eebb87088af136b6b8015`  
		Last Modified: Tue, 01 Jul 2025 03:07:28 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d1627b8c1b7025061ef2a2b813a16b0f924a73681c0a2695a467979487ff60`  
		Last Modified: Thu, 03 Jul 2025 23:30:23 GMT  
		Size: 12.7 MB (12704341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1abcfb676071ad55de9c6d172d16deb71fbcd4f1e9211a2bac29759e6263e5`  
		Last Modified: Thu, 03 Jul 2025 23:30:21 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209c4e368a8415f068a8ce2a1acdf5dce1e96782ca45442380be1b916677e91f`  
		Last Modified: Thu, 03 Jul 2025 23:30:22 GMT  
		Size: 10.6 MB (10629910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958537a9775be6cdb5ddd2994b2dbf7690a992c2d3a894b8551914df38f8c7b5`  
		Last Modified: Thu, 03 Jul 2025 23:30:21 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1085f2e47d4d841b6b2c0a9ccc23dc751a350efee78320095b0ea8fddd0d076d`  
		Last Modified: Thu, 03 Jul 2025 23:30:20 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e490abab42fc45ece23a73c6a0af4fc66970fd3467ec34ddd261700958a0c24d`  
		Last Modified: Thu, 03 Jul 2025 23:30:21 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c98fc2e8a4eb03231e0914c6ab256269ca706c4a5d9a73920693c6c69e6541`  
		Last Modified: Thu, 03 Jul 2025 23:30:20 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322636ee952cef1d13aff3ed9aabcbaa4ea5436c785b25a25a8f45a023e44aa0`  
		Last Modified: Fri, 04 Jul 2025 00:29:34 GMT  
		Size: 1.1 MB (1065629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee87e75fa8411c711302a4b7496fad33d8fa7212e212a4f75bf684ed3a6695f`  
		Last Modified: Fri, 04 Jul 2025 00:29:34 GMT  
		Size: 934.4 KB (934441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7b681b6cab6eedd2fe22bc88827ae7ba15e195e08acbae879955866bf3ca39`  
		Last Modified: Fri, 04 Jul 2025 00:29:32 GMT  
		Size: 8.0 KB (8045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b51e286b9a4eb8dbc95b2d5c5e8e20f1e903944f250f7cd0e129af227bb6b98d`  
		Last Modified: Fri, 04 Jul 2025 00:29:34 GMT  
		Size: 1.9 MB (1861467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6873321fe1df59057aefb485dfb8475e939c1b86b4ed84b549f54a26ebedc140`  
		Last Modified: Fri, 04 Jul 2025 00:29:33 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:600552cb26911bc3d3ca64e9661651921e9ccd89790c0b3c9853a8d41d42692f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e10dd313a6e09c6af9767d80b03e3e92c5b8208d35760ca26d322567cec12757`

```dockerfile
```

-	Layers:
	-	`sha256:1184173ac2657b94efbadc18fafd75ecd4432245a1bf35aa09dec7b7884a57d7`  
		Last Modified: Fri, 04 Jul 2025 02:10:35 GMT  
		Size: 36.6 KB (36569 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:23ee73bb5a869e17460d150ed0cfc36fc75c7863b444f332345d9f3cbc56fe65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145519833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2976b1a21075024b22ece38c51262ea6713d5ea8a0780b1525de83e9acd0b633`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.23
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGWINCH
# Sat, 21 Dec 2024 02:12:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[80/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef237a39acf4f8b50140ea0e65e44fb78759dd5c3014dea07a2e868cbaea5448`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d1f66f2aaac83b6eaf2006cda16a0feae7d183fb4de3fc7f021a3b94f4d2f5`  
		Last Modified: Tue, 01 Jul 2025 02:37:09 GMT  
		Size: 76.1 MB (76149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834cb9f18ec360ae1dafdba9049fa98c9a4c9dff8f407122be76f6644c8deb27`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f48e36c51ca567e00204b7602dd2f3197ed65c785e21a191aec888d5acbe886`  
		Last Modified: Tue, 01 Jul 2025 02:40:42 GMT  
		Size: 18.9 MB (18855730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739500a213db554802bf5a3a6ea64baa201f9a9e42247c34a186877ff2824052`  
		Last Modified: Tue, 01 Jul 2025 02:40:41 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a65a3ecd90f92c07f97694692d2624d48f057c9b5aa300524021d73c2c682a3`  
		Last Modified: Tue, 01 Jul 2025 02:40:41 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2faf9d275a5d34fd8aeec8a32205cc2fe1f7e77d5bb510bb7004ea4f4e8e462`  
		Last Modified: Fri, 04 Jul 2025 00:27:13 GMT  
		Size: 12.7 MB (12704328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0894da8e843ebae63ddbbfea51ceddeecd42ee1940b53f919a5253babcbcc125`  
		Last Modified: Fri, 04 Jul 2025 00:27:12 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6a84b73f917d85784d4cff0a571e446dd8aa62d2fee0806ce22bf3016446ee`  
		Last Modified: Fri, 04 Jul 2025 00:27:17 GMT  
		Size: 10.1 MB (10053627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cfcabf298644da43f656eb0442a81f923a5c6c58b1d735396c027952df104b7`  
		Last Modified: Fri, 04 Jul 2025 00:27:15 GMT  
		Size: 2.5 KB (2459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167e140e94724bf3cf2807832e13c320d6bcc17b4e7a02e1d1aaa75866a10048`  
		Last Modified: Fri, 04 Jul 2025 00:27:14 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:943069f34d5fbb9b7d3cb127fe157273340629e55b5739682d215752ab6e04c2`  
		Last Modified: Fri, 04 Jul 2025 00:27:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54fa7f20f0bfd57530f62fc8a677d6ff8eea9b39f90e360663f77161dfa8b10d`  
		Last Modified: Fri, 04 Jul 2025 00:27:01 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223066e9c233cde8576bf1e30d8900fac17d45a56858a9817abae685f8958157`  
		Last Modified: Fri, 04 Jul 2025 02:55:00 GMT  
		Size: 1.1 MB (1058457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ffef6da6299689cfc0dc287f1eaaf461d9b0c89e893c5ffd869347bc141a6f2`  
		Last Modified: Fri, 04 Jul 2025 02:55:00 GMT  
		Size: 882.4 KB (882422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdb012889c3f00c4b3bf5703805e562ec79c13b022c9da5c5437aa381769615`  
		Last Modified: Fri, 04 Jul 2025 02:55:00 GMT  
		Size: 8.0 KB (8048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e403dee0139093b05ebbd4eeb9202887591b9726c667317979fd5ec5459070`  
		Last Modified: Fri, 04 Jul 2025 02:55:00 GMT  
		Size: 1.9 MB (1861470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30603194a281316ad5ab922b1504c2b99340f08d244bad96079d1c291df0b8a`  
		Last Modified: Fri, 04 Jul 2025 02:55:00 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:9a904dfe402b99ac33de502b595fd538a268c364356660c272ce090bc4f4f779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e0470310463a5974b92b1863d9ff2e887427073e5c770d16b87dcde1f662454`

```dockerfile
```

-	Layers:
	-	`sha256:563dae0bf2c9c70cbd7663504c10f7217d50fce7420c395e4ca93f90e5feffb0`  
		Last Modified: Fri, 04 Jul 2025 05:10:40 GMT  
		Size: 36.6 KB (36569 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:610ec3533df667abd8fd694ad776db7413bf6a3876ea7fc6383b673bbc3de642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.6 MB (174619993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb084c28598564dddbf44b48ea0c458044d96127b48178736d8309a5ccf2d17`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.23
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGWINCH
# Sat, 21 Dec 2024 02:12:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[80/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06f0a25db22853df6a6e6e4155e86895f626a540d37bf7e50bf413fd1fa8f12`  
		Last Modified: Thu, 03 Jul 2025 22:57:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d119d74c86b221b030b9083d0f51ada6b53b7c58ec2a87c7276bf5229a2d16`  
		Last Modified: Thu, 03 Jul 2025 22:57:42 GMT  
		Size: 98.1 MB (98130784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81367bd3a505020af3e40d8bc05177f06efe70245dd3740395c2183000421e42`  
		Last Modified: Thu, 03 Jul 2025 22:57:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923763a309489408edc63cbe391e3bb65308445ae68fadb93cadf1cdc4e24330`  
		Last Modified: Thu, 03 Jul 2025 23:02:12 GMT  
		Size: 20.1 MB (20136099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4505b45d37187cabdcb58525226c56fe8cf483cdb1eb04e0175fc3d9a044e40a`  
		Last Modified: Thu, 03 Jul 2025 23:02:10 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a42b9bb391186e51edaf896a57430f8b3908164d261ae41e974eb92ce6f1b5`  
		Last Modified: Thu, 03 Jul 2025 23:02:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561678cff3607fdc770b99eaef149cc13d9a95d4d3cc96e0fde1e98ee5de1dac`  
		Last Modified: Thu, 03 Jul 2025 23:54:44 GMT  
		Size: 12.7 MB (12706218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93079bb63d4b413d81de0db44bc615f11b9e87f6fd272425ee8478bf4794be93`  
		Last Modified: Thu, 03 Jul 2025 23:54:43 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0af689377c5c2bc9ba7c81a1266adcf5cfa1d5d0f21da682be0c24d91adb0fe`  
		Last Modified: Thu, 03 Jul 2025 23:54:44 GMT  
		Size: 11.7 MB (11682039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59eb13655cb9565eac202912e992d6778d50ee2d4805b96f6fe9ac8bc1433dc`  
		Last Modified: Thu, 03 Jul 2025 23:54:43 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cdf971baee529e4cd7782d40a9db52479624ebbfcc7e3e7791f04a32866286a`  
		Last Modified: Thu, 03 Jul 2025 23:54:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717bc93c2f2694d095a429eac1fb67a4afb771e039fea4c60dc6cb87de4c1a96`  
		Last Modified: Thu, 03 Jul 2025 23:54:43 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8bc2b72dc2931d63b2dd702ab5f4a81fd8467cf9ed55793e002f45c32375334`  
		Last Modified: Thu, 03 Jul 2025 23:54:43 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4645c13415a777ebead12b364ac067317c18d1fb0c961cf87ce9229229b16b`  
		Last Modified: Fri, 04 Jul 2025 03:28:03 GMT  
		Size: 1.0 MB (1022458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1440cf19cf415c104335e334393d1c515b731be765a8670b089b91f231bbe9bc`  
		Last Modified: Fri, 04 Jul 2025 03:28:03 GMT  
		Size: 987.8 KB (987826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7824694ab1a2d3753009f99c0a2a58547cee7e16a106cfdbb3a5d08044b8409d`  
		Last Modified: Fri, 04 Jul 2025 03:28:02 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d69fe5e8d0e91e4670688d04909548c0428a5b67a125284e03fc4a85c43b54e0`  
		Last Modified: Fri, 04 Jul 2025 03:28:03 GMT  
		Size: 1.9 MB (1861471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1064f055ca3efa31441b74992f03fb5b53adc616d91247870b1d92b4264790fa`  
		Last Modified: Fri, 04 Jul 2025 03:28:02 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:38777493643e04e67f43c397570c3430fe2fe8f4a7cb49ec22c1266497815d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.6 KB (36619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34999b24a864d2280fa87cbb1e065184b7caad5018c3b600560890ee0e73eb0d`

```dockerfile
```

-	Layers:
	-	`sha256:0e7bce7e61578f4b237fca5e67c32ad9a9bdf75d93f36fcbc9e84bb465119f45`  
		Last Modified: Fri, 04 Jul 2025 05:10:43 GMT  
		Size: 36.6 KB (36619 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; 386

```console
$ docker pull postfixadmin@sha256:207a1a0e63baf46e961e3f11715b79e183640d01c33b8906e875e9aad7e02475
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179927091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d54e2d7885d6dabe1ce2450f07f26e7c82604c5784df25ba937097eafe56044`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.23
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGWINCH
# Sat, 21 Dec 2024 02:12:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[80/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db0a36f8ca7fcbee6bdbbf455e607d8410275869cf81b39669ba07c3313c31a`  
		Last Modified: Thu, 03 Jul 2025 23:04:04 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f001cf40249c4c6c9360415d99e14c1df6b22cd0b6fe9616ca95511e3b18c2`  
		Last Modified: Thu, 03 Jul 2025 23:04:09 GMT  
		Size: 101.5 MB (101515351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c48d4e645f62cabdbd73d543b9ff08bb4b754b481c641cc8fc454ed0ad5c96c`  
		Last Modified: Thu, 03 Jul 2025 23:04:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ef2629d7cd84662c53c90aca8e050c782f834a1c8e626eff32c33096647317`  
		Last Modified: Thu, 03 Jul 2025 23:04:05 GMT  
		Size: 20.6 MB (20638483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2051e4c17be26a7bda27b4a07ebffa1becb6f10fc8210846ce9143d3ea5daf74`  
		Last Modified: Thu, 03 Jul 2025 23:04:03 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77f91f111374c9a5e4c6e41bece5b9f3b2179a65879020e807836db59536ba5`  
		Last Modified: Thu, 03 Jul 2025 23:04:03 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c899890cd93639221d9b5cb7c1a97a465c9fc6f66dd2caf3bf2963f19d0840e9`  
		Last Modified: Thu, 03 Jul 2025 23:04:05 GMT  
		Size: 12.7 MB (12705379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4c11e280639dc50d2b9f7814200a867aa74ff935f6afa79d93bd701a4f6c4d`  
		Last Modified: Thu, 03 Jul 2025 23:04:03 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb537ab3829874865705510b0389c77cd9d16bf1bc483359c99f8ca8b61ceff7`  
		Last Modified: Thu, 03 Jul 2025 23:04:05 GMT  
		Size: 11.9 MB (11886507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104365058a68686c76ba2f751fdb0189743928c17fea320c041e79d29a9797bf`  
		Last Modified: Thu, 03 Jul 2025 23:04:04 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c4e4f8d02d0417b09e5ea68f37f5570b7ee4118c476a0fc7aabbf7c76ea5e3`  
		Last Modified: Thu, 03 Jul 2025 23:04:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5083fa466add4b1b844f9b4992164d7190ba5281090dc681fa59137b9179998`  
		Last Modified: Thu, 03 Jul 2025 23:04:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c4d7702871287de302dc48ea9ed6deb547eef84b4bda6c0550808f08dc9ac79`  
		Last Modified: Thu, 03 Jul 2025 23:04:03 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbc47ba5145aa550f7d25a8ae61491a311bcbdc0fe79d94b73bb40ed5070737`  
		Last Modified: Fri, 04 Jul 2025 00:25:42 GMT  
		Size: 1.1 MB (1077172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f24d2ae60e242c5c3b628390576ead4a554adfd57992b10a248d490155bde7c2`  
		Last Modified: Thu, 03 Jul 2025 23:12:05 GMT  
		Size: 1.0 MB (1014872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153e00f059df59110ecb79446915de7943eb694cddd7743c0032a069b47f85da`  
		Last Modified: Thu, 03 Jul 2025 23:12:05 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0983fa6d81f29821a2994653f043074d6b9a0fc4586c451d9cd23ea465c7fddc`  
		Last Modified: Thu, 03 Jul 2025 23:12:05 GMT  
		Size: 1.9 MB (1861470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99045b085873f771f2dada342d256858f40514ac9e3a21ab7029398414f98493`  
		Last Modified: Thu, 03 Jul 2025 23:12:05 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:19b18fda7262e5968896a548ad9571e5c89e8d5ef0a84e8e80c4cefb635524e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266e71aa4a0e29991f2e48b681e9be7c32f4e7204ef6d11cdae75895c659265b`

```dockerfile
```

-	Layers:
	-	`sha256:f80000d6502e77c8f2220180034c5078223e9d27e623a80764be85d0037915f3`  
		Last Modified: Fri, 04 Jul 2025 02:10:43 GMT  
		Size: 36.4 KB (36374 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; mips64le

```console
$ docker pull postfixadmin@sha256:9cf83e356ac986cf8eb5c2d1e9e77564c7a9cb9849f31e9046b4f59fe5ca74ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156497941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c8d6b2c2442b42ff2cbca04664c54a03da9d893d11ea53c9eecaa48fabce96`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.23
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGWINCH
# Sat, 21 Dec 2024 02:12:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[80/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5e69eb612928f2b1edb8b79310fa7eb01b97eda1179aabfcea5395120a404`  
		Last Modified: Tue, 01 Jul 2025 04:33:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60c6c65191f30a3311d0f913382becc510cfefba81063f7617c9b537f70c6f7`  
		Last Modified: Tue, 01 Jul 2025 04:33:43 GMT  
		Size: 80.7 MB (80668384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bdcd15545dd72fcd7e549e199c0795e04a22a395d9ecc76e94dbc2d57e32d7`  
		Last Modified: Tue, 01 Jul 2025 04:33:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554ed581434f4504a391f8e646f305d1afb4d6940b123246358f7d765d8071c2`  
		Last Modified: Tue, 01 Jul 2025 04:53:26 GMT  
		Size: 20.1 MB (20069286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc96140eff9b375b8f34b88c126f947ce6fcbbefb6e2391f1433c0b98f5412d`  
		Last Modified: Tue, 01 Jul 2025 04:53:23 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b41b9b337a9c969abc2eae5405e43d9ae17f5d40811131fa325042d7c044648`  
		Last Modified: Tue, 01 Jul 2025 04:53:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2b3c9982350ed16b66953607199acfafba762f9509c60977e7b45087403208`  
		Last Modified: Fri, 04 Jul 2025 00:42:33 GMT  
		Size: 12.7 MB (12703891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcd005f996382b17560a8cb8c4f24c751550da47844313de90ed55643105d43`  
		Last Modified: Fri, 04 Jul 2025 00:42:33 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3b13ca84c5a3d2c9d3306e623573c2eee061a61da7af7e824ad34ebfc33b66`  
		Last Modified: Fri, 04 Jul 2025 00:42:34 GMT  
		Size: 10.7 MB (10729732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8083416b4b2801612ee5ece6d0b1a5347603e926483dbf99c5654b5767a840d3`  
		Last Modified: Fri, 04 Jul 2025 00:42:33 GMT  
		Size: 2.5 KB (2462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dfaa6069aaa471bf08b3909067ca0d6ef7169511ef9cda21ac66993852f9ed`  
		Last Modified: Fri, 04 Jul 2025 00:42:33 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7504f5f06a2611f97c5b1df42cd945420257a0232f32b19c5b70241b3aa8928c`  
		Last Modified: Fri, 04 Jul 2025 00:42:33 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c767c554c925d33cbf171339241f176d25c68dc053a538701c66c9fccd9029f9`  
		Last Modified: Fri, 04 Jul 2025 00:42:33 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1538f31620546f8a837b2ff218c32cc75f85ae4fb7948e22de8717ef5deb2661`  
		Last Modified: Fri, 04 Jul 2025 03:42:15 GMT  
		Size: 973.9 KB (973923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e497ef9b81cab86a7ed9a5f1b7627d5bdce44d81702ff5ac58d1494f2f5e3650`  
		Last Modified: Fri, 04 Jul 2025 03:42:15 GMT  
		Size: 959.1 KB (959069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c202e160e487035b112ea3940fa0c0ff6b5a6bfc54fcbc420cf5ee2cef4583c5`  
		Last Modified: Fri, 04 Jul 2025 03:42:15 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b83e0dce091aa3e57ec77f29540094d5e4e404b65673182572607a30446b10`  
		Last Modified: Fri, 04 Jul 2025 03:42:15 GMT  
		Size: 1.9 MB (1861471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2fef1c5c5d452163de603693fe88c211e3398424f64c904f1b8a73748565584`  
		Last Modified: Fri, 04 Jul 2025 03:42:14 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:efdc45b6b729cc949790a4cbc10df878cd674923c80dd72d697e98de0a3d6666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d3f8e20a9969aaacdd2a8ac079e14b91d0fae5a14919854160656614ba96b3`

```dockerfile
```

-	Layers:
	-	`sha256:bdae104049a58c7104e001807f458fe801acc67b841219c4f5a42e03c4a7bd93`  
		Last Modified: Fri, 04 Jul 2025 05:10:49 GMT  
		Size: 36.5 KB (36528 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:755781d0aef02d560355b14e6200c64921492e8749d3b3f123f5c2090a98e479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185503072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341011d2572b7abea96f0510a495142689da766e66f6d423abfb0ea967d02628`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.23
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGWINCH
# Sat, 21 Dec 2024 02:12:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[80/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36b68bed4d5c4fdbbd3f66cf1ee62569453e6d1dea00500a229578b96f8f6c3`  
		Last Modified: Thu, 03 Jul 2025 22:59:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c94ede1a54d9ac4e13b34ad1cd441b94ad5436ccfacbf6f1e5deb2957a47257`  
		Last Modified: Thu, 03 Jul 2025 22:59:12 GMT  
		Size: 103.3 MB (103326831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83487f2c5b5e9a02c2d3911052a6efe6e28cc68c5a06b7a0080d8ff6f6a2c72`  
		Last Modified: Thu, 03 Jul 2025 22:59:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35c67000e323388d19a55a9c5add154479cfc0fadfc7b08718851d38436f10c`  
		Last Modified: Thu, 03 Jul 2025 23:03:58 GMT  
		Size: 21.3 MB (21308277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e429ee02968ccf407fd388a5e7fdbbc3cbf9ee2fbcb868224604ee73fcebab7`  
		Last Modified: Thu, 03 Jul 2025 23:03:51 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1eb613b404f93974eadc63042d47613e9a7c597ba569a0d16dbd3788380a77`  
		Last Modified: Thu, 03 Jul 2025 23:03:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c82be0b7d24231a4724795a4fb9ea7c82178063558f14f4a8c01d1eac78664d`  
		Last Modified: Thu, 03 Jul 2025 23:44:00 GMT  
		Size: 12.7 MB (12705841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bdf8958926c48621a1aecc653d1d19b7d57d0314e159e120b8cd68687907ab`  
		Last Modified: Thu, 03 Jul 2025 23:43:55 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dae28156c7f085a575036c625e75c96e7a0c5f7f898bb4d5a922509c04aba20`  
		Last Modified: Thu, 03 Jul 2025 23:44:00 GMT  
		Size: 12.1 MB (12074575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490f878adbd5703577d288b56c7a2101d2e770f8743ec35e1305501d6a732475`  
		Last Modified: Thu, 03 Jul 2025 23:43:57 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230dfe296e71f8fa81a682a98ba7937a7f4fb7c0e599cf1302a2c22693d6d12b`  
		Last Modified: Thu, 03 Jul 2025 23:43:58 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc2d30a45c442f295a54e8a7cb1f9bf8211df8ecc00e366304c6c8be58081c9`  
		Last Modified: Thu, 03 Jul 2025 23:43:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b17ce9faa473e6d9667920ef66e6a7122d1631aef7d7ba266daefe9ccf91d407`  
		Last Modified: Thu, 03 Jul 2025 23:43:58 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e55ef1632dec343e7182f2aca2406f3ebc7edef9ab70841431f334d815f32a`  
		Last Modified: Fri, 04 Jul 2025 01:33:11 GMT  
		Size: 1.0 MB (1009452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92145eb47315ab543592086aa533f92630bd8b40ae09058a2acbb90d4980229`  
		Last Modified: Fri, 04 Jul 2025 01:33:10 GMT  
		Size: 1.1 MB (1128365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e26526606c167a15dd8796b3f55d813daa68e78c3080503957f1e5098689fd8`  
		Last Modified: Fri, 04 Jul 2025 01:33:09 GMT  
		Size: 8.0 KB (8048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e67049ecbf8bf2ef8b0ac5de047b7019c3cd63a01f0ec09dbbd3e04a838c48c`  
		Last Modified: Fri, 04 Jul 2025 01:33:10 GMT  
		Size: 1.9 MB (1861466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b264a20346a6b8406179a1d625d7d8d64de4628859a66f71ec7695d4dc0d2b5`  
		Last Modified: Fri, 04 Jul 2025 01:33:09 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:d552bd28edefc09b0fbd71324654f5013bf6d1a8bc27e170a77998c96edf0e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.5 KB (36506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27cc3196e0ca4210ebb23b27625a86deb1037d5b9301f46e3e65b8bf48a92773`

```dockerfile
```

-	Layers:
	-	`sha256:f70e621f386fad0ce98acc93a392b5ae960c9343dc4e713c3f285f444a04d2b0`  
		Last Modified: Fri, 04 Jul 2025 02:10:52 GMT  
		Size: 36.5 KB (36506 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:apache` - linux; s390x

```console
$ docker pull postfixadmin@sha256:8c04ec89ae9a99ec4a0527f8782f83cbebf5b3c05dba0b6348df294b22e3bc47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155111538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:840a36cf794fca273c4619e9c2d1c4faca07ae4b71abb9ec091735067c5ad806`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_CONFDIR=/etc/apache2
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_ENVVARS=/etc/apache2/envvars
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends apache2; 	rm -rf /var/lib/apt/lists/*; 		sed -ri 's/^export ([^=]+)=(.*)$/: ${\1:=\2}\nexport \1/' "$APACHE_ENVVARS"; 		. "$APACHE_ENVVARS"; 	for dir in 		"$APACHE_LOCK_DIR" 		"$APACHE_RUN_DIR" 		"$APACHE_LOG_DIR" 		"$APACHE_RUN_DIR/socks" 	; do 		rm -rvf "$dir"; 		mkdir -p "$dir"; 		chown "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$dir"; 		chmod 1777 "$dir"; 	done; 		rm -rvf /var/www/html/*; 		ln -sfT /dev/stderr "$APACHE_LOG_DIR/error.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/access.log"; 	ln -sfT /dev/stdout "$APACHE_LOG_DIR/other_vhosts_access.log"; 	chown -R --no-dereference "$APACHE_RUN_USER:$APACHE_RUN_GROUP" "$APACHE_LOG_DIR" # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN a2dismod mpm_event && a2enmod mpm_prefork # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN { 		echo '<FilesMatch \.php$>'; 		echo '\tSetHandler application/x-httpd-php'; 		echo '</FilesMatch>'; 		echo; 		echo 'DirectoryIndex disabled'; 		echo 'DirectoryIndex index.php index.html'; 		echo; 		echo '<Directory /var/www/>'; 		echo '\tOptions -Indexes'; 		echo '\tAllowOverride All'; 		echo '</Directory>'; 	} | tee "$APACHE_CONFDIR/conf-available/docker-php.conf" 	&& a2enconf docker-php # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Dec 2024 02:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_VERSION=8.3.23
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Dec 2024 02:12:45 GMT
STOPSIGNAL SIGWINCH
# Sat, 21 Dec 2024 02:12:45 GMT
COPY apache2-foreground /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
WORKDIR /var/www/html
# Sat, 21 Dec 2024 02:12:45 GMT
EXPOSE map[80/tcp:{}]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
# Sat, 21 Dec 2024 02:12:45 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ARG POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_VERSION=3.3.15
# Sat, 21 Dec 2024 02:12:45 GMT
ENV POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
# Sat, 21 Dec 2024 02:12:45 GMT
ENV APACHE_DOCUMENT_ROOT=/var/www/html/public
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; sed -ri -e 's!/var/www/html!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/sites-available/*.conf; 	sed -ri -e 's!/var/www/!${APACHE_DOCUMENT_ROOT}!g' /etc/apache2/apache2.conf /etc/apache2/conf-available/*.conf # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.15 POSTFIXADMIN_SHA512=02c4a7fb0d5b148a2f9e73e0278a47d1ee63b29a0019cf510f04d33386fc50727c0dae728eafee688a136159ba462af1931fe0658daa06671459c43668867865
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Sat, 21 Dec 2024 02:12:45 GMT
CMD ["apache2-foreground"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eb609875faf51e20c0ced671506012769a509c263093fc793d0aae0bcc9b5b`  
		Last Modified: Thu, 03 Jul 2025 22:58:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528c62694487a8c0f3520f828eaa12f12ec29ad4944569d71931f79d7011e046`  
		Last Modified: Thu, 03 Jul 2025 22:58:51 GMT  
		Size: 80.8 MB (80825817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbc2722da34fe4bf90187950be5838def4ad6dd2e97500d7f8d44fbb460783d`  
		Last Modified: Thu, 03 Jul 2025 22:58:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea70cb16775519e1e6afea5f92a6f4df6643e707ce14834c6acb8c1e10bad6a`  
		Last Modified: Thu, 03 Jul 2025 23:03:46 GMT  
		Size: 19.9 MB (19895050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82dbf2a6af0aca3924a417d5be70d3d097fc543e4b2d173daddca1249975b74`  
		Last Modified: Thu, 03 Jul 2025 23:03:43 GMT  
		Size: 433.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3cfd97636634ef167a662eb6365ac5d946e0a02d428ae74943831599600faf9`  
		Last Modified: Thu, 03 Jul 2025 23:03:43 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb293437244b12cd2700eb51a2980303dfb72a0a82c237560ec0d7480fac31b`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 12.7 MB (12704639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66bad0e411ea2e48c55bf9778f20a592365c753c30cf1676eb411791cd6587a`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc6015838c525465d19bde2ade7216c349169d953ce92c4d0a70b5894956751`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 10.9 MB (10877619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9efec24a0b36f242a2db8358e73bb8a958845718262ad7a1f47a34c99fcd96`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 2.5 KB (2461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f159643383b9df838c4df3e7d46788f0f6b1ac5266d5a6766b24b3ecb63132fd`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b6a703f1d5d70fd4684399acb51d4d684dedfa152f1464a07b6066f557cad81`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e530b7b7c810e86c436bd5ec262f8b2fac0990a003dba7c9083ccea5bb61a0fc`  
		Last Modified: Thu, 03 Jul 2025 23:46:18 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13de3c73642f0a54bd343580b401b07b183f22e77f6fb920cf28507b81723384`  
		Last Modified: Fri, 04 Jul 2025 01:31:32 GMT  
		Size: 1.1 MB (1057672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c2f5d25e29e0293eb1a8f47c4bf3d9a973e3aea18069d48f41c78ffeff11ee`  
		Last Modified: Fri, 04 Jul 2025 01:31:32 GMT  
		Size: 986.0 KB (986016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1211497b851198a6c052162dd01776b0c599ab80a85cb4cbb60d34d0bcda101e`  
		Last Modified: Fri, 04 Jul 2025 01:31:32 GMT  
		Size: 8.0 KB (8048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99cc269ead9b0ae89c888ee00664768d19f0014b5713b6a6920d6dd493863ae1`  
		Last Modified: Fri, 04 Jul 2025 01:31:32 GMT  
		Size: 1.9 MB (1861469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438a7d2774579eb843395d749274028065c58e3f0ae4b205323eb413db0e8837`  
		Last Modified: Fri, 04 Jul 2025 01:31:32 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:bdc1c771929c7e11f5569f134e41ac5e0683d3588f25e9413e030ee43e83a4df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.4 KB (36422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8bf9ff5722c5dad74afd3ddd4279f7d3f9a3662a50dbdd7dbc142e7dccc1f75`

```dockerfile
```

-	Layers:
	-	`sha256:9373c32193b70c9a3852af4183ff61b8a09b672c2f5dae1d5e3a99eabe930153`  
		Last Modified: Fri, 04 Jul 2025 05:10:53 GMT  
		Size: 36.4 KB (36422 bytes)  
		MIME: application/vnd.in-toto+json
