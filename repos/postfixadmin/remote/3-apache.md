## `postfixadmin:3-apache`

```console
$ docker pull postfixadmin@sha256:2bd191f5e8fd88f5260fa40dba72d16b29e313b6220c803e86154a2ba6cc24d3
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

### `postfixadmin:3-apache` - linux; amd64

```console
$ docker pull postfixadmin@sha256:06317a900d490723f8b205758e85dc014f0dcb169f05554d347438b8cfb04502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180991423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630a1b148194516a1f17de9bba0cca83dc0e3da5bb3946cfd4746f835b71d51c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
ENV PHP_VERSION=8.3.19
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5f6e53c351de1b5161c0035600ea659f596aafa631f3377df9a4204ff70fa`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63a1878e2890d14d57fb22d732b4d0a3d5557790695df9fa3cb0b03b2efdd80`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 104.3 MB (104329155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374bc94691bf532c02664812e24725e858c994195d15d160aec0006ca8ee4783`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10be233c465c8e62fe111d971861c75a7ea58fce6baa695d8ebb44bd356ab88b`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 20.1 MB (20123808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5aefa1cc109ae6c23c9b43828b91cc439bedd81e6998fb150fb6f8ec314b90`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d834dcf194e62bd3889223a9570b857db556fe9d0ff9fdd62da038646c4e9b7`  
		Last Modified: Tue, 08 Apr 2025 01:20:39 GMT  
		Size: 480.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae87df1c29d8d9e73f7abf5f0331b06ba6655b3edeb1b979fbc68aaaf3081fcd`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 12.7 MB (12689804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ab1c75e08c290147bc75256b96d044e311d2543136e436fd5365133764f2b9`  
		Last Modified: Tue, 08 Apr 2025 01:20:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e648bd91357d9694c3497cbae945624b5abbc2c82b0a35c4e1bf9379e692247`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 11.7 MB (11656055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be4d97a90d401096242c929db8ed51a1bbb9e1644b80f15bfe8db5652efa5610`  
		Last Modified: Tue, 08 Apr 2025 01:20:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580970411a96439d603eac225bb8d649ab6862690a082de61edf789a38018bb1`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c59f70a4316a5ca8651433e21ba2a8734ebbe759ff5e168c644d3e182bba5ec`  
		Last Modified: Tue, 08 Apr 2025 01:20:42 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46df4c834e54865fdb6e1b426c60607107dabf0eca5b06be06866f0f2367bebb`  
		Last Modified: Tue, 08 Apr 2025 02:13:44 GMT  
		Size: 1.1 MB (1092508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fab91a98fdc0bcfc9c6d2471822a1d31d9a1c694785831f2fb619164beb67b9`  
		Last Modified: Tue, 08 Apr 2025 02:13:44 GMT  
		Size: 996.2 KB (996202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d58257d07de1a2551d34ffecf864397fba70e61ec4abdccd6c3a6ca84d6a14c7`  
		Last Modified: Tue, 08 Apr 2025 02:13:44 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708884ce2c9a7710a4eaaf0b4e2fe20beec5f74fd22f721c97f6715706a2da86`  
		Last Modified: Tue, 08 Apr 2025 02:13:44 GMT  
		Size: 1.9 MB (1861467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba00e0974432fedb01f95219fa5151b3cd070ffb0d59c1ad89507489197d9cd`  
		Last Modified: Tue, 08 Apr 2025 02:13:44 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:b7cf76c91b031ce2e5a81ed7dd7da770f007e10c8b000a54bb8b4c66bd6bfe5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e985a168d65e80fe64ea5b31e946c2f98fcb1b697b54a46f2df894ded6ee9668`

```dockerfile
```

-	Layers:
	-	`sha256:933915f2775f1d9e0c6d2befa3ab2bffea0e6bf77276abcad3387e773caf79e5`  
		Last Modified: Tue, 08 Apr 2025 02:13:43 GMT  
		Size: 35.5 KB (35504 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-apache` - linux; arm variant v5

```console
$ docker pull postfixadmin@sha256:cfb541793cfb5a3910aaa487e390a805ddcde5a8289fcfac2b5aa6b6ec713f17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154361552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd63129d98f375778d39ee4d3260316dd0f351bc1525ea405d4a5929d2157e56`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
ENV PHP_VERSION=8.3.19
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:6bc9a3c94c333faf2488bd82d1b9c3d692b6250c0ba5ca05c2c815cbc7a2cd53`  
		Last Modified: Tue, 08 Apr 2025 03:01:22 GMT  
		Size: 12.7 MB (12687714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d04552a9659be46e8396421dd725b915ef77f81b9aac5a56982992c68ce067`  
		Last Modified: Tue, 08 Apr 2025 03:01:22 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd992638b82460942cf493b9240b9d00fdc8aa15441cbd17e0e82149ac4d22d`  
		Last Modified: Tue, 08 Apr 2025 03:01:23 GMT  
		Size: 10.6 MB (10627573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c096c81844591ed29945a7b5d752428599c2d23461adf53458ce1d8bcd486d`  
		Last Modified: Tue, 08 Apr 2025 03:01:22 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2795c0004e4073dcbae29b8036bbde3bb7946038506ab3344384fc343d03dc`  
		Last Modified: Tue, 08 Apr 2025 03:01:23 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5275984ab08e6ed79dcc5f953f6bc41aae74c42ebcd03264f0223b794c0c878b`  
		Last Modified: Tue, 08 Apr 2025 03:01:23 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f972b53514d38c5fe581eea6d3ec3fd65623c00d5b2ef41954c427efad5ff2`  
		Last Modified: Tue, 08 Apr 2025 08:08:25 GMT  
		Size: 1.1 MB (1065460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad940e85fe4c8d803d3c73daf55b4f16cb9d19faa5e0dce2c8d1a18af303db5`  
		Last Modified: Tue, 08 Apr 2025 08:08:25 GMT  
		Size: 933.6 KB (933573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87e939c8b1082463f928cbff826d4ca9c3a68bf6abca4e1ee0ada3d0a6077db`  
		Last Modified: Tue, 08 Apr 2025 08:08:25 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf6b011b50ef47031e11715230e56a51905afc4535b8ee90659e751eb55aa47`  
		Last Modified: Tue, 08 Apr 2025 08:08:26 GMT  
		Size: 1.9 MB (1861474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6406b6a0b7fae42dacfd02d80fa3d5ef05b820b30f7a6a422c84a8ecd2755a`  
		Last Modified: Tue, 08 Apr 2025 08:08:26 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:10b0be9a4b6fcca25f7778bd4eb1399e9581853d6a2c828456053af93d8d082b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1031a8ee2146b58f997c9a923e622c241dd405cff612eefadb3b9de78b469dd3`

```dockerfile
```

-	Layers:
	-	`sha256:54cc7f7c75f0621295f893a5dc4ad5c68bf669f40e1d255fcd9e00ae88b3d8ae`  
		Last Modified: Tue, 08 Apr 2025 08:08:25 GMT  
		Size: 35.6 KB (35645 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-apache` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:e32262b26e4f19f3cf6f18c979e5f9dfac1b0ec0853028ceca107b937efc6acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145490165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec3628257ee05f7538d8917660d4dbe011967e320f154d40c25dc5b713237444`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
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
ENV PHP_VERSION=8.3.19
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:676cf117f557880ff2e894692781cbce1b2a04502aff2e34b58c230b14731b8f`  
		Last Modified: Mon, 17 Mar 2025 22:18:43 GMT  
		Size: 23.9 MB (23915088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e617588c40680b3f1658a4a3364c14dc2bbb5375a67749657cf8dbe55d7f0c01`  
		Last Modified: Tue, 18 Mar 2025 06:41:43 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4553f56272d8fce2a78fc29124d67ecf355fe0135e44488afb3056d1fcb89ff`  
		Last Modified: Tue, 18 Mar 2025 06:41:46 GMT  
		Size: 76.2 MB (76163018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b26744e01528566e84c9a1ca4e7a4ddc5b9fc1264fa031d1947d7082552964`  
		Last Modified: Tue, 18 Mar 2025 06:41:43 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6c5900ff8434306b5d6ea6e236c6db6ac30b0f0b9a4c29b79dc6c9496d427e`  
		Last Modified: Tue, 18 Mar 2025 06:45:41 GMT  
		Size: 18.9 MB (18857267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bca0458f5f531449901d0b0ee375e89f5f3f1ece8533f57b900bbcac7e8ab67`  
		Last Modified: Tue, 18 Mar 2025 06:45:40 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51adcb00c3034156da9825eae4d905c7d509cb802fce0704ada3dc1df9f503a`  
		Last Modified: Tue, 18 Mar 2025 06:45:40 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576ed8b83fa0d26619b99f24c73437b92dbbf7bb9f277cf4cdad18fa6eb8289c`  
		Last Modified: Tue, 18 Mar 2025 08:34:02 GMT  
		Size: 12.7 MB (12687650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c85b84a1e48e8d01794cf4ada90e7de0b9da425a493f0f526d54eae8744de7f`  
		Last Modified: Tue, 18 Mar 2025 08:34:02 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb78479fb45de473a2c7c6a0b1965e567580313891930e7b70711246285349f6`  
		Last Modified: Tue, 18 Mar 2025 08:34:03 GMT  
		Size: 10.1 MB (10050321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb0ecf9dfec84857b814e8eecf9ee13b2012771dd6554e23c546be309caca33`  
		Last Modified: Tue, 18 Mar 2025 08:34:02 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2509b348f6440bb34aad084b5a6cae6e21d43448453a3cb08bb8b7356ea7b7`  
		Last Modified: Tue, 18 Mar 2025 08:34:03 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231d95c1a248cea87fb299e99e73421fb9ec96de7b47efd5342dc93bc12f738b`  
		Last Modified: Tue, 18 Mar 2025 08:34:03 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff5331abbfe37fb90adfb4e283b6476c1af627e7017ec386892b0fb45c0aee3`  
		Last Modified: Tue, 18 Mar 2025 13:59:54 GMT  
		Size: 1.1 MB (1058350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092aa28fd1d2d0a8f0c1e68f6019f44526a9efc4bfa19fb3159b73ac24c0475e`  
		Last Modified: Tue, 18 Mar 2025 13:59:54 GMT  
		Size: 881.8 KB (881816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843b2e42fd67bb2f056886f1ef21ffb48883ca8faf118d7760f0627489644ced`  
		Last Modified: Tue, 18 Mar 2025 13:59:54 GMT  
		Size: 8.0 KB (8048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a140f27724f99f0a627a0c7e6d7f58ecfcdd45fd38e43d93a50281ba616b74c1`  
		Last Modified: Tue, 18 Mar 2025 13:59:54 GMT  
		Size: 1.9 MB (1861474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb3ae48ae9e870ad1491eef39a5ebf16f7038cf0740a7b87dd98f14297a44c4`  
		Last Modified: Tue, 18 Mar 2025 13:59:55 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:b0289cf77b4911d3bfb3001934dc58f9b783897e7ccdacc65b364056a381f00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab35372fb928913b2750a72287c8dbea51e3d01bb00182b622dc57121ad8858`

```dockerfile
```

-	Layers:
	-	`sha256:2dcb3d8bc05b5a70f321c4e5b10b025a5e0eb623376870deafbfe7fa6771879a`  
		Last Modified: Tue, 18 Mar 2025 13:59:53 GMT  
		Size: 35.6 KB (35645 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-apache` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:c47d773515c3ae7491a68dbc193561bb35d685a2a6eff3d67753853289d9db0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174545985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994b9674f76ce0a29f444b4df98fd431937ad805fbae2bb9e7ee555a1864ecf3`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
ENV PHP_VERSION=8.3.19
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:19185b5bf48e20987f7b54a437f2cf03f3e1e9aa6987d5f5f962fe6d1fba4d5e`  
		Last Modified: Tue, 08 Apr 2025 03:55:17 GMT  
		Size: 12.7 MB (12689570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5bdcc233df8f327b643ff56bbd5669f60e8a0367c2699c0c996b1df23f59fd`  
		Last Modified: Tue, 08 Apr 2025 03:55:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0381e344ef30b726584d162983ed8f0b8272fd4d6fdbcdbdf6e283c1e1ebc8c`  
		Last Modified: Tue, 08 Apr 2025 03:55:16 GMT  
		Size: 11.7 MB (11654148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ffb7b92becdb1951f2fea66137d138ced192fb67173fb47d3009cbf369e267`  
		Last Modified: Tue, 08 Apr 2025 03:55:16 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2377a40de1ac2cb7b5be154ddcb0f7c34e9f4960fa2ef8472c53f2bddca6f4b`  
		Last Modified: Tue, 08 Apr 2025 03:55:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5522193af1f084c6a63f3e12b000e507297b1165dce1718515c70ee302f739c1`  
		Last Modified: Tue, 08 Apr 2025 03:55:17 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f87d9d8f53e9ff32ab6ac9a7cb809d99251320c0413f4178601d6d1809238ca`  
		Last Modified: Tue, 08 Apr 2025 11:53:01 GMT  
		Size: 1.0 MB (1022319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60ae1037d80de0995c02a71362d4ac22ece6553393992eead609e09edad21a6`  
		Last Modified: Tue, 08 Apr 2025 11:53:01 GMT  
		Size: 985.6 KB (985595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ddc90a4b28801d3322344a3f2447dc3a4cdddee1e409fbfb958bea8942d9f6c`  
		Last Modified: Tue, 08 Apr 2025 11:53:00 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb084481280df04fe894adfc841f8b699979f88ccea0c62a998053af9c364642`  
		Last Modified: Tue, 08 Apr 2025 11:53:01 GMT  
		Size: 1.9 MB (1861475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e6639d081008adc15ce18630669c9c591764a47eb5e091102ff75c5e6f6ddc`  
		Last Modified: Tue, 08 Apr 2025 11:53:01 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:a4913eb1e279086cd1cf66c520803105f4bb524e7dded38e37be8bcc622dd4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 KB (35695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b697ed8109c04bf0224460919f60989fb9206f80a0161eecbba71bb826e65d0`

```dockerfile
```

-	Layers:
	-	`sha256:0bfaf72b7982e86e1b4ee30cfec244f51b5459351c85696f378d3b3fe16dc05f`  
		Last Modified: Tue, 08 Apr 2025 11:53:00 GMT  
		Size: 35.7 KB (35695 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-apache` - linux; 386

```console
$ docker pull postfixadmin@sha256:0ce806306e2b8968ec2c9688bee2dd2133cd7d0fb836ea4ad6c8295fbfdf0ab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179899292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925571648885b2e9d980029d6e08bed794b4a83c4ae5f182b1611b2cc3fd783c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
ENV PHP_VERSION=8.3.19
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f20d46b2d2e0674f127232b8fc50a23132cc7e8bcd022c509d82f61118c7e`  
		Last Modified: Tue, 08 Apr 2025 01:21:33 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c004002d94f359f7ae1e023832e26bbadaf831e585cea56921d8d9ca03833e53`  
		Last Modified: Tue, 08 Apr 2025 01:21:37 GMT  
		Size: 101.5 MB (101511981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965cf6e9b9616efb93914a32de85e04e787c02234bfa9535582300d9f94f738c`  
		Last Modified: Tue, 08 Apr 2025 01:20:59 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d1565f968ca10bd5b62527dc4fd7435b1a0f88db2e9893393e700c33a225d`  
		Last Modified: Tue, 08 Apr 2025 01:21:34 GMT  
		Size: 20.6 MB (20638476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21567f40b53841f544cbc38850f25115b5a1ea0d3ccb9671b69596c49d36a623`  
		Last Modified: Tue, 08 Apr 2025 01:21:34 GMT  
		Size: 430.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c6e2782eeeb054cb45950d1da3e6b214f6af47d52e5c91c1aca15d548b7931`  
		Last Modified: Tue, 08 Apr 2025 01:21:34 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3baacf3073c1a8e2d1f3948d65d23e2a7abb72ef045fba961dfeebad490ca45`  
		Last Modified: Tue, 08 Apr 2025 01:21:36 GMT  
		Size: 12.7 MB (12688761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382ce0ca6666b80d471871bca33abe94dbf4c1d48e4bf292ccae735140f4c908`  
		Last Modified: Tue, 08 Apr 2025 01:21:35 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6581db79a07a62f85aac19093f8d401a07116b87d43678a156c34ecf783c87cc`  
		Last Modified: Tue, 08 Apr 2025 01:21:36 GMT  
		Size: 11.9 MB (11881679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290d8a36de407cafebc99b9342eec2a465c06c8deff4e76f6f3dad5fc8128a16`  
		Last Modified: Tue, 08 Apr 2025 01:21:37 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e925e9c7fd968a6710280c13bb0426afac9f12b21d081ac1f0a7fe3648e0465e`  
		Last Modified: Tue, 08 Apr 2025 01:21:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8318945cf14ba4e4fd851ee8bc52dc44020e8a64c545c7ce6e7c252ac1aa30`  
		Last Modified: Tue, 08 Apr 2025 01:21:38 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:961551e40fdb5016d2435332f992fc4a5571888295fa5972dc7233944352c39d`  
		Last Modified: Tue, 08 Apr 2025 02:13:41 GMT  
		Size: 1.1 MB (1077084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c30e4752b273c1bcbb6ec5431013282dcbcfe008038d4534640a1624c8704ee`  
		Last Modified: Tue, 08 Apr 2025 02:13:41 GMT  
		Size: 1.0 MB (1013931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2024dc3df154683e3ad16f9ed70915836979b8fd45afce77b6618b4b59c7ff13`  
		Last Modified: Tue, 08 Apr 2025 02:13:41 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdaa03d33431322e745b7fd922fd67658f03fa4504b771bb9d1cc24a5c2d6a4`  
		Last Modified: Tue, 08 Apr 2025 02:13:41 GMT  
		Size: 1.9 MB (1861468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4174cd1187d067ae1b8f6827ba8aa34219a11895651ea910d57e7b5ea772b355`  
		Last Modified: Tue, 08 Apr 2025 02:13:42 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:ded7f7206289f734f08e05fad551e7d0bfe429cfa1a6c030e8ada1fbb5f4127c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.4 KB (35449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:258fcba0e4c06791429228c21c02588476591f70cc1ac66de68c7965e2681efc`

```dockerfile
```

-	Layers:
	-	`sha256:10b8c1184965b0044a5c469f5adf5f86cf3ffb7a5a13bf1a3c7d9e57da34d28b`  
		Last Modified: Tue, 08 Apr 2025 02:13:41 GMT  
		Size: 35.4 KB (35449 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-apache` - linux; mips64le

```console
$ docker pull postfixadmin@sha256:90c5675333da95ba2b36906b65b2a55178c5e059e095d82b21388fb02a21fb7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156449668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e2e9c474c39c94d4d35e1dbee60d3208cfdba3ba82284d7890ed17343ad43c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
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
ENV PHP_VERSION=8.3.19
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:18c44d6735d044d9bace3fdbe647c9b8187637683376f05d85dcb1185876721f`  
		Last Modified: Mon, 17 Mar 2025 22:19:04 GMT  
		Size: 28.5 MB (28489456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bd269b985ea48bf86dc037dcb35294087cf3e065dfd7434e164bcb8bf64c60`  
		Last Modified: Mon, 17 Mar 2025 23:39:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:050973a1180f92d98b90c6f886eea7dc5c0773a0865b32d686e655ebd949c7dc`  
		Last Modified: Mon, 17 Mar 2025 23:40:05 GMT  
		Size: 80.7 MB (80670361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a05fe1708dc8633bcc81ee7c4993a38f845ff79bae7822be81357b02993fac`  
		Last Modified: Mon, 17 Mar 2025 23:39:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26e7687fef2f8df78b40270694d61bcff539561cdb349bbad638075ae089308`  
		Last Modified: Tue, 18 Mar 2025 12:04:15 GMT  
		Size: 20.1 MB (20069237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0fdb534d04f5030ebdd4c0b405102b47e11c1a0ce999d2a7d6ea70ce0d2074`  
		Last Modified: Tue, 18 Mar 2025 12:04:13 GMT  
		Size: 442.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e0ff697414adac64704738f153f1ece58deb7c9ede9ccab7ac6eb920b761f5`  
		Last Modified: Tue, 18 Mar 2025 12:04:13 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20d6402f74164db245d577cf46c4bbdef42833035cc8fd29bfd790f49b6d4b8`  
		Last Modified: Tue, 18 Mar 2025 17:46:58 GMT  
		Size: 12.7 MB (12687372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab984ea2fe8f99c0df5a371163be157839f83e0350c8b29c61f9885309d7a559`  
		Last Modified: Tue, 18 Mar 2025 17:46:56 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360ab75d46b41b13d9b31327d5fa6fbbd779b23166e94f7e3a633cc6f87a01fd`  
		Last Modified: Tue, 18 Mar 2025 17:46:58 GMT  
		Size: 10.7 MB (10724250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ff24df102d56d7cfaf7855c8b2dc0badf1691661511926df7c5dc1b046bede`  
		Last Modified: Tue, 18 Mar 2025 17:46:56 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd66ec95e6a1130538a218bd5a0449c5945dfcd9b0ceca8c3e6ed4b79608901e`  
		Last Modified: Tue, 18 Mar 2025 17:46:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4901c18828c668b22ea2265e17d6677f818d751b6ef1cdf13684ba9bcfb6d30d`  
		Last Modified: Tue, 18 Mar 2025 17:46:57 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43fd7a1b3a2c7b82103274a61cda5dc1181c681d9bd15025d202b127c0e97da`  
		Last Modified: Tue, 18 Mar 2025 21:26:08 GMT  
		Size: 973.8 KB (973814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb34643d8a332a6929821d3181e5a4622c801fe16fbe7ec4f212518bf3dddc6`  
		Last Modified: Tue, 18 Mar 2025 21:26:08 GMT  
		Size: 958.5 KB (958510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e3223f53dd3f54ec65c2e24a081aef8e29c73d29b0652cd8bc7c21933a71ea`  
		Last Modified: Tue, 18 Mar 2025 21:26:08 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041ecee7c03b2c7b36ecebb11ed0526abc4f3376407be64956656b6f018fc7b3`  
		Last Modified: Tue, 18 Mar 2025 21:26:08 GMT  
		Size: 1.9 MB (1861471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a463e9ab6e832da56907da0a543de9f262882cb6e4e8f4af973522f77f4e4e8`  
		Last Modified: Tue, 18 Mar 2025 21:26:09 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:6f9385fd1154a730d51645dafaca4785f40f4313631859fbce92bb87122e19ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb80fd3efc79c7b195d77a0ecd0d9117df6072fd92af8cf0da12d02ab894f3fe`

```dockerfile
```

-	Layers:
	-	`sha256:0a0f48a4d319afaa85d4c05c37f5ba1156ebc05d5e6dd0cb02f896e535150c39`  
		Last Modified: Tue, 18 Mar 2025 21:26:07 GMT  
		Size: 35.6 KB (35604 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-apache` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:b936645d9472de5c6de4ea6a8d73db4fd05f1ebfb25dc529afb83f4e0da1304a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185476094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d898b3e48e37cca6421d622e1b97db162ee5e581f3139ab07fc799887d25774`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
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
ENV PHP_VERSION=8.3.19
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:adf82337b4fb183f4596eca3d2cc8a57b7bf0065c1287b8f0db37224e3a0584b`  
		Last Modified: Tue, 08 Apr 2025 03:04:47 GMT  
		Size: 12.7 MB (12689250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3bce4e0f03b7d33a379d3499ba099a83c2259f68c02763351fab4a56f644be`  
		Last Modified: Tue, 08 Apr 2025 03:04:46 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba770508eedc86cf45cc4a49d05166148eaf8ba8563a76a6b1cef97f4da17271`  
		Last Modified: Tue, 08 Apr 2025 03:04:48 GMT  
		Size: 12.1 MB (12071767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd0ab79dbdc3d100f1e6daeb65422d541d9606f07379b592499b4ee23c8d9399`  
		Last Modified: Tue, 08 Apr 2025 03:04:46 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6861aaf2c5e01aa81aea50dc409de0efd229b5d3e5dddcb2666275f28d78a24c`  
		Last Modified: Tue, 08 Apr 2025 03:04:47 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a6865f480dca460ca18e0abbecb3f26354a08f2df522b0dc0272b4884cd563`  
		Last Modified: Tue, 08 Apr 2025 03:04:47 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d57f61af21f60bbbd0418bfbd1b4a97318af7a3ad12094f2343906e031eb4979`  
		Last Modified: Tue, 08 Apr 2025 07:52:46 GMT  
		Size: 1.0 MB (1009393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f3af292c07d380678788a47d18dc63e64933612a08e8c868159aa007120bf5`  
		Last Modified: Tue, 08 Apr 2025 07:52:46 GMT  
		Size: 1.1 MB (1127604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e6ee94184e57066970c594980bdbf7d4dd8d61d2a4ce0ebdb35a931fcbfc5`  
		Last Modified: Tue, 08 Apr 2025 07:52:46 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a288380195fd4528fbd40c7850de48e778e4495781953a443b6ce668790f18f`  
		Last Modified: Tue, 08 Apr 2025 07:52:46 GMT  
		Size: 1.9 MB (1861472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551ce16b70c3d9b79988cb9b2b96f7f5a09b5a3ca9b67203e08140f68a5f9cdb`  
		Last Modified: Tue, 08 Apr 2025 07:52:47 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:f496bc7c9ccdd4857b160789289c5ed291d7bb7c580670911f0be45f49b84f0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a1e0735044b2b327710abbd7f793b64385526cac40c4fd290af4e011baa598`

```dockerfile
```

-	Layers:
	-	`sha256:471ba5e2b483ed5e4a4c5fec60f81109a23eff82b8a94f6cacdb2a5c7cea649c`  
		Last Modified: Tue, 08 Apr 2025 07:52:45 GMT  
		Size: 35.6 KB (35582 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-apache` - linux; s390x

```console
$ docker pull postfixadmin@sha256:eb096bd450455d0ab6f1e453c75a011620e5f8dd3eeb1de3a251805e90920ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155079620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d5e23da970242bdea006ddf943f10a2f4c39c729f2649d9d10c7f46d73602c`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
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
ENV PHP_VERSION=8.3.19
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Sat, 21 Dec 2024 02:12:45 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		apache2-dev 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--with-apxs2 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 21 Dec 2024 02:12:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:9cd31eff3b8a6cfabc2a2e5d9795b727db3423f1ca9cf3d29d04e474f80e955d`  
		Last Modified: Tue, 08 Apr 2025 02:47:33 GMT  
		Size: 12.7 MB (12688065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006facada5256802acd610b8dc89a2d7d9c5537681e7045ef89da4326390fe0c`  
		Last Modified: Tue, 08 Apr 2025 02:47:33 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47c4630308e941a34391eccf75a9ba0b7f10e46736ba7777e8bc3a76f2066264`  
		Last Modified: Tue, 08 Apr 2025 02:47:33 GMT  
		Size: 10.9 MB (10875665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d074fce59ecd3fc183053ea49fbf558ac2dd84c9d4b102e15ca06fa021153ef`  
		Last Modified: Tue, 08 Apr 2025 02:47:33 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8011374f5d4c22e4cea4a4f513eb4438ecca6fe276620aca8ea35525cade6f`  
		Last Modified: Tue, 08 Apr 2025 02:47:34 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a614aefebd3fb10f947985fb191b423ccf1ef7ba56775fab9ae5e70658bdb3`  
		Last Modified: Tue, 08 Apr 2025 02:47:34 GMT  
		Size: 892.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:130d255d6b874f2de5325ac1d8fe7ad2f35e4db7ea642e60a46256d0a3b60587`  
		Last Modified: Tue, 08 Apr 2025 06:27:15 GMT  
		Size: 1.1 MB (1057616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813ad21f1a56225719c529e5df525d3f5b6db600bb4bf8d6d8851844ce134852`  
		Last Modified: Tue, 08 Apr 2025 06:27:15 GMT  
		Size: 985.2 KB (985218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d25a51c631c17c6bdcec7eb8047a9dfef29ad31676e45151ef29d6df230e71`  
		Last Modified: Tue, 08 Apr 2025 06:27:15 GMT  
		Size: 8.0 KB (8048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4349207abd7fc4470a415d8031966fcea1a192cbf3a883be17dc0dc7d00d530`  
		Last Modified: Tue, 08 Apr 2025 06:27:15 GMT  
		Size: 1.9 MB (1861467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfde6a8a1b5147dd29c2ce09b1a4e8035cf92e4d904ca59d9dce7d2d71073d96`  
		Last Modified: Tue, 08 Apr 2025 06:27:16 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-apache` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:5406c9d0c59f7a276f3fc58dae72479771da2b1ff3080ca93f14166eec649537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06b0358996fbf9536b4f802b2f473751f09dbed81539ae54b16fb644a8bbcf6`

```dockerfile
```

-	Layers:
	-	`sha256:4dd0dac03d3a9f36645a2b9f2b80f9eb3689f95dfd5f1fedce12e151bc2ebeb3`  
		Last Modified: Tue, 08 Apr 2025 06:27:15 GMT  
		Size: 35.5 KB (35498 bytes)  
		MIME: application/vnd.in-toto+json
