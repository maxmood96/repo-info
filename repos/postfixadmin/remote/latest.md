## `postfixadmin:latest`

```console
$ docker pull postfixadmin@sha256:69d579894656d3be50bcb237d55b7fc41cbb2014ad270a6403529adea1aa96b8
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

### `postfixadmin:latest` - linux; amd64

```console
$ docker pull postfixadmin@sha256:2b95d06d3144d5593004fa715cf69a817567df68cf134c2bac1c664f34e0a7ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180968564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f9af5c16248a84737a1fca53df1a74fbde844db4f04dfd0dadc1c43b4d84f0`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9439b75f7025bbf5b7cdfe2453f822653c3385bf443afa14c38aa536c4d61bf0`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480b11587afcc7b0e9526fa67bbda90f5592b6c5fa0f55805b5db4993909552e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 104.3 MB (104328639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ac9628630da264f6ec7d165645a739812dd044f1b37bafc2a13444b77b505d`  
		Last Modified: Mon, 17 Mar 2025 23:17:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e70aea67e763d8228bbbd929f27eaf84aa6df2ac4401575d9eb79dc03eec4d`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 20.1 MB (20123820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a7f56a88199fab64827903e4dae42ab0401849ae6e175a8383ed6eba2c2af9`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 432.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108ebd4ec1f6e7d2da7ff384e17c3314c4ccba92d16c7533ec9bd3437084b01c`  
		Last Modified: Mon, 17 Mar 2025 23:18:00 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a022dc65d674e1dec779e099d864e881f65861aa8b6da7534239c75d9414d29c`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 12.7 MB (12689809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1cccd7bd4cefd35eaa098aa27c99f7c8d0b4c5ae4161367ce6963a9e5e448b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a3a4deb9512ce156667937843b6a1ce2e8e180bf6e36e64959f1ca9cfd9382e`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 11.7 MB (11655939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c68f3c3dfb54c1e1babe0f90952b054f4f235061b5fa6143883d728c975cb2b`  
		Last Modified: Mon, 17 Mar 2025 23:18:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4ed2fe59b45b24e36ff7c79ae1dc377ca704df0f9c6680aec2cb5c40ba5047b`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6451280804a1f0aeeaf07c210addf74d7bc8401eb62d553d0a595f581f8f7809`  
		Last Modified: Mon, 17 Mar 2025 23:18:02 GMT  
		Size: 889.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41750a0e63eebefdafba36c456695b34fe6555585e9a5a96777f19c822d0a731`  
		Last Modified: Tue, 18 Mar 2025 00:16:22 GMT  
		Size: 1.1 MB (1092580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a403124c19d4ae9445b2d682c0d99727de0a6432879205d25692f13c5ae60192`  
		Last Modified: Tue, 18 Mar 2025 00:16:22 GMT  
		Size: 996.3 KB (996269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4aea60ad47fa469ae2a9842467c2532dfe2f7802dc5d0ee0006b1792e91a60b`  
		Last Modified: Tue, 18 Mar 2025 00:16:21 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba11ded12570f3804ba9c338a48032f2e8a652e4b83f08bdd1b09ad032bfbd98`  
		Last Modified: Tue, 18 Mar 2025 00:16:22 GMT  
		Size: 1.9 MB (1861470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf2f37e47ae0f5703124b35cab4848146950a7a388a59997a50929ee77eaa82`  
		Last Modified: Tue, 18 Mar 2025 00:16:22 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:c48505a49680316b78d8047cea6de1307c609b478cf7b91ddce3b65b70799685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74cc0c0b34fbd14d2bc4136791cf29c934fc28c3e8eb912ee27e88341ac71d97`

```dockerfile
```

-	Layers:
	-	`sha256:8ae68908adc11abe0e3e6da344b6380feb4e4b00ef52215a221a1004cad2ad2b`  
		Last Modified: Tue, 18 Mar 2025 00:16:21 GMT  
		Size: 35.5 KB (35504 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; arm variant v5

```console
$ docker pull postfixadmin@sha256:e6989dc5ca6d7e53e4a40e87671b0b797f81fad115e02ad315dbfda1d81fab6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154343646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96eda068e68ee7eb2203fbc32337d9cc8673d9a02872d09971b9b0b5c17f725f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d8a77b84d73cc90f2bbd622ec970d928c4f14e4be51927c88b7c15b7b6772382`  
		Last Modified: Tue, 25 Feb 2025 01:30:58 GMT  
		Size: 25.7 MB (25740630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3014e21b6e4396df02c7cc3c5f126fa29d531fa5a1ad0b40b80de6794ae2694`  
		Last Modified: Tue, 25 Feb 2025 02:51:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e0a56f6198eb0af5102ce28eda7b5a34384f5b54701b7346487229bff9e9c`  
		Last Modified: Tue, 25 Feb 2025 02:51:20 GMT  
		Size: 82.0 MB (81993202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24b0f2499da71327f565769347ea1f63e9070dfa8385025f0465d80e603c361`  
		Last Modified: Tue, 25 Feb 2025 02:51:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21a0010d00b089e3a34b60fddcac813cd3a1211368d868b76aa3c52acf85f39`  
		Last Modified: Tue, 25 Feb 2025 02:55:46 GMT  
		Size: 19.4 MB (19419190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836efc0ee062aca6556d741fb3e390ca6b509fc639049bef1cfc24e29616d566`  
		Last Modified: Tue, 25 Feb 2025 02:55:45 GMT  
		Size: 434.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb27253beef75bf260f9071d9fb96a1614335f2b1af270afddf706a8142cb7b`  
		Last Modified: Tue, 25 Feb 2025 02:55:45 GMT  
		Size: 483.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedd4679084b4778112418e02c5284175452764c5d5b99098cf493114704c2cc`  
		Last Modified: Fri, 14 Mar 2025 00:53:28 GMT  
		Size: 12.7 MB (12687702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:342a927c346bf397e57b79734f5690151c273f3f1df370ba793c8c8214e0de87`  
		Last Modified: Fri, 14 Mar 2025 00:53:27 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba27bffd671229acf3d0929a2e062ef2b2b9d5d6f1a2453c41e965028ae3b0d`  
		Last Modified: Fri, 14 Mar 2025 00:53:28 GMT  
		Size: 10.6 MB (10627469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68624c765c0ce2e8391900f4b77f6332d2a03d841f41ace5fc29ed232c843270`  
		Last Modified: Fri, 14 Mar 2025 00:53:27 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304ec4b450ed8bdcc16b8965c175dce70326f1543981d0e01b865829d4507ec1`  
		Last Modified: Fri, 14 Mar 2025 00:53:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edbca8a4a8fbe967e4fa4fc26a4a40df2c93f898f69366858f639bbd41539962`  
		Last Modified: Fri, 14 Mar 2025 00:53:28 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84532fa000c913d1f4f1553afef6311f1a8b4b54099202b811665613568e7e8d`  
		Last Modified: Fri, 14 Mar 2025 01:38:58 GMT  
		Size: 1.1 MB (1065466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f503f99a5a771de0cb490720a63b8de5f7cf8af8245fa2cb19049fa189bfe66`  
		Last Modified: Fri, 14 Mar 2025 01:38:58 GMT  
		Size: 933.3 KB (933333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d8a04259b40167618fba0c27f8ae1c7af7fb40b225d6fcf6add0de8f376d19`  
		Last Modified: Fri, 14 Mar 2025 01:38:58 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc2aecbb12318f1e58ef4c90e1210275cfb6e56a6e44cd553f9127088344fd3c`  
		Last Modified: Fri, 14 Mar 2025 01:38:59 GMT  
		Size: 1.9 MB (1861467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53fb61c8bd4dd26c6761478428cbfdf965f97b59bea19d2f247e086885d98076`  
		Last Modified: Fri, 14 Mar 2025 01:38:59 GMT  
		Size: 1.7 KB (1657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:a6995e9f5f71c0db2a14ae12e3f7d8868250809b76fd03bb540348929141772a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c811e82f396cee74d549afdffdfab9e1964f515e321af518813d78eac7f13974`

```dockerfile
```

-	Layers:
	-	`sha256:1705befe3e3fb102641be56214b9287b059ddfc0e684050a113ea907d81e3292`  
		Last Modified: Fri, 14 Mar 2025 01:38:57 GMT  
		Size: 35.6 KB (35645 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:58790dce32a526e2cc581e18e99ee0f06e6fac78ea59cc435e92d1643c828351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145494655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc4e9e15c3b6927ac5a48795a234088ee922bb384350d53be268bcf8cba9db7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d7e09b1d1dfb9227526dbb14ab0477c0b3e235584b36c16282a130f9eb0f3c`  
		Last Modified: Tue, 25 Feb 2025 02:45:28 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195d4e13a8d04cec48669402c294b437f110e69a04f231bf7f4fb038ce009feb`  
		Last Modified: Tue, 25 Feb 2025 02:45:31 GMT  
		Size: 76.2 MB (76162862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86b4b4427af4c394c935ad45142cba4e205bc21eb933d83f2d2432a5bb3cb64`  
		Last Modified: Tue, 25 Feb 2025 02:45:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9b346bd0d0d97918e8cf0f24429f88856b2aa9caf305b66eabeebc6aa67c68`  
		Last Modified: Tue, 25 Feb 2025 02:49:24 GMT  
		Size: 18.9 MB (18857331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffc087e149899d6dd0d9896e9ad11e94fde980bb585468298c7ea4818bc83fa`  
		Last Modified: Tue, 25 Feb 2025 02:49:23 GMT  
		Size: 431.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b7d03bc48135c9bb3b0743190bd1e7146614e74be185bd6df7aefdde677f36`  
		Last Modified: Tue, 25 Feb 2025 02:49:23 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24bcfaa9d8e569ebcf7f1cd24990f9fc31aa55de4a0053e60d259735db202c83`  
		Last Modified: Fri, 14 Mar 2025 03:58:59 GMT  
		Size: 12.7 MB (12687661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0542fe2d20bbca7a3ca6b234dadd44f7277d074c6b8f9df946c90ecd868437`  
		Last Modified: Fri, 14 Mar 2025 03:58:59 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80cd333cb91ddeef49736e95ebc251f7b783de10b0f3920eae31161287c21b3`  
		Last Modified: Fri, 14 Mar 2025 03:58:59 GMT  
		Size: 10.1 MB (10050322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ec195a169a2d4cc16628a00cf9ca0735e475e5ba711dd1feba8a8f53f5f42e`  
		Last Modified: Fri, 14 Mar 2025 03:58:59 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cc046a82c3f2224eb1a15356ca8c2bdbd28612891fad622aa0d21606b9ee1c`  
		Last Modified: Fri, 14 Mar 2025 03:59:00 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06c5acc389b6baa7ab6299084b0e164096961453c6457985cec5df064d5f388`  
		Last Modified: Fri, 14 Mar 2025 03:59:00 GMT  
		Size: 890.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6768efd3057023c6160e30c1f98084580115bf96bcead8a2a0f26e2419bc816c`  
		Last Modified: Fri, 14 Mar 2025 06:54:03 GMT  
		Size: 1.1 MB (1058373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dbe1851f364fe9088a05b659ca7d44e230db0ea6cc7b85737adf371ce9666e`  
		Last Modified: Fri, 14 Mar 2025 06:54:03 GMT  
		Size: 881.7 KB (881719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87d1ac178d63019870940f06f2e8dee65c40e369a8fec3e7d3cdf93e747fd46`  
		Last Modified: Fri, 14 Mar 2025 06:54:02 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8d18a3e6bf86f22b8b04124b8ffae70bdc6bdd0f4890401f918f48f36a993d`  
		Last Modified: Fri, 14 Mar 2025 06:54:03 GMT  
		Size: 1.9 MB (1861470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6306c8265dfb69e0ed21e8cb445d0491866429592921635d3840cb5ea6583a3e`  
		Last Modified: Fri, 14 Mar 2025 06:54:04 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:215276e5f9cf8770138eca13efa502db90d1fe2827c87ff6e20f6316797967de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa66f17a48abefde00afe0edae883c9b0864457ddf82074cd47c667ffcafe5c`

```dockerfile
```

-	Layers:
	-	`sha256:bb1ab328943473768783ab8cfea9f18ed92eb2ee1e4e61a74338d1bd545a5507`  
		Last Modified: Fri, 14 Mar 2025 06:54:02 GMT  
		Size: 35.6 KB (35645 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:9d23f812a4894937dc49fdf7743eb78d114067d6278c5ab531f4fcb664c30872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174527613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4fb108dafed110dffe8a2dd0964a850b020cafc00908f16c7b8d710eb1e1ff`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ffecde8bd985cf96f0467d70fccc665026fdab770dcac3f793be1deba85a30`  
		Last Modified: Tue, 25 Feb 2025 03:07:28 GMT  
		Size: 20.1 MB (20120919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab17c0b9534d8803a88e819a77b6257c8c52458e1501948f051ab897599e4bb`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 429.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72d58237634f94d2abae7d95c65d651fb63692600b04577a084ebafecdf4289`  
		Last Modified: Tue, 25 Feb 2025 03:07:27 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:348a98e4bc287d526952cbfa7b8330493aaeaae34c431b3aba16149e2cd12c5d`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 12.7 MB (12689592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5070376f829a2cbe78f83aa714c657bab3bbca47a5492122dba5013ee1b9d93`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3733ce1dc8f098a728afb8e03c6db51725ef7568195a33d233ecbff65fe0365c`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 11.7 MB (11654097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a3acd1e8600e03632e7ec241fa1a70ecf2665a025afad021c1d56e3b3bd094`  
		Last Modified: Fri, 14 Mar 2025 02:45:52 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d953954f5eac551497677900cd3cc940165a0d978b93bc29c6ce8e4f38349f`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8adc5b9462222353d17d6bfcce3af5cc93fda9bce6eb69281f45cb2f3bb6bce7`  
		Last Modified: Fri, 14 Mar 2025 02:45:53 GMT  
		Size: 891.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df986413967384732998570916c7927c7fecb45f89de4f0275377082abfa0ba2`  
		Last Modified: Fri, 14 Mar 2025 17:48:33 GMT  
		Size: 1.0 MB (1022343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950a7d9cbdd88d87262ae9a854d8a0be17995c8f2d1a0a6c0efb8961a6672c64`  
		Last Modified: Fri, 14 Mar 2025 17:48:34 GMT  
		Size: 985.1 KB (985127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398ed96fe07e9606b91e129bb38d335ad92f020282efc996faf8f3a67adb5684`  
		Last Modified: Fri, 14 Mar 2025 17:48:33 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dd0ed5e23ddb4fc850571ea9ab4ecb97c7496edf03616ecb8a24878109ae6f`  
		Last Modified: Fri, 14 Mar 2025 17:48:34 GMT  
		Size: 1.9 MB (1861472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28c35966b826ec10c106cb7f6f306e0d4e74e42313fad8350eb9ed75c6d8717`  
		Last Modified: Fri, 14 Mar 2025 17:48:34 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:c13ef316ec9f3d42c2e95dd985431482f841387d9015b9e435b87a570795bbfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 KB (35695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e361fae10d8eee04cd30eb8ce229d5ac73044eba4ecb766bbbe44820c974fe`

```dockerfile
```

-	Layers:
	-	`sha256:48bd24abd5806b0ed233d03cfc2077195e15aabc9f9ebf8cd680740b9c97964a`  
		Last Modified: Fri, 14 Mar 2025 17:48:33 GMT  
		Size: 35.7 KB (35695 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; 386

```console
$ docker pull postfixadmin@sha256:88c5f91a0677a04ff37b412a8c6069837654f8afca8a52c39b0651f0bc70696e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179878501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fda3c86ce44d8e17007b2bdedd1d09a3a8c205d52f013481d86fbc4b1bf0239`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79dba1fa920a36e428e30031419dde40aae699a5570151822a6a3ad05c5331bb`  
		Last Modified: Mon, 17 Mar 2025 23:31:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cee7a566712daf781192f7082eda1bf7fa7a006eef1ed6ca47e6ffdc71fe3b`  
		Last Modified: Mon, 17 Mar 2025 23:31:45 GMT  
		Size: 101.5 MB (101512722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077cfb20b009652dc868185465a18479e08a31a6cae7b8f489e2ac5c68780eec`  
		Last Modified: Mon, 17 Mar 2025 23:31:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1274101f4243944a70e3f21a59c629d67fee26706121ff36bd62129cb73ae6d`  
		Last Modified: Mon, 17 Mar 2025 23:31:43 GMT  
		Size: 20.6 MB (20638470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6999420998b1c8fe69df4743fb13d51dacfe4a8a031b6b05cfdb1e0df41671`  
		Last Modified: Mon, 17 Mar 2025 23:31:43 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ce37b5ff219f923df668aade73ce40433fc3d6ecfbd7d4ae97162e95698503`  
		Last Modified: Mon, 17 Mar 2025 23:31:43 GMT  
		Size: 481.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9685a66958829e165a2a30fd7234e30ccd16a7aa89223224b31fb443a5d542ac`  
		Last Modified: Mon, 17 Mar 2025 23:31:45 GMT  
		Size: 12.7 MB (12688744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3046a28b1598de1c393b40868685bcb3042ec133597feab257db3c3356b1b5b3`  
		Last Modified: Mon, 17 Mar 2025 23:31:44 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c167c4704fe296d7b7237decec6c41ed980a1723db5ba5d4e1f0181259003000`  
		Last Modified: Mon, 17 Mar 2025 23:31:45 GMT  
		Size: 11.9 MB (11881523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61dd2d016ba27fad7242740a81c61f1bc6904b554d0cf2239abdd521b241faee`  
		Last Modified: Mon, 17 Mar 2025 23:31:45 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f19986ebb23bafa9402dcc33d4e37490b733db8f481bebb4bfb105899ed308d6`  
		Last Modified: Mon, 17 Mar 2025 23:31:46 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:804bfa56085b4d85f080fedd472bbc716b22b2c618f087d80d3fd1515114eefc`  
		Last Modified: Mon, 17 Mar 2025 23:31:46 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd08996c1b6dc250be475b07d69b78f8d186225d3fb576846b1a0c57e0734b38`  
		Last Modified: Tue, 18 Mar 2025 00:16:15 GMT  
		Size: 1.1 MB (1077041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44cae6dfaf928cf7758d1a61a7efbf37dac5d117afa4ded1b1dc5d48531aa1e`  
		Last Modified: Tue, 18 Mar 2025 00:16:15 GMT  
		Size: 1.0 MB (1013828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81cf7b27699cc072ef2910803cb2fc5872cfa776ba131f5bc127ed25cd371b7`  
		Last Modified: Tue, 18 Mar 2025 00:16:14 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6aa139d4c8c015660dbfcda6ae3fa9ff6016f5387e57b3f032867498d4de39`  
		Last Modified: Tue, 18 Mar 2025 00:16:15 GMT  
		Size: 1.9 MB (1861471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599a61cf11c79f4a6cd03fb2ea8de102478b1adacbe48a5fa6d57807c329c05a`  
		Last Modified: Tue, 18 Mar 2025 00:16:15 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:90126c8f04d8733fe6e221f47932c671beb0f35d92409e60460964ea51abe728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bb25a30b0df0063ead6d5416d41ced570a49e55afa8a661e9be57bb1d8e0b3`

```dockerfile
```

-	Layers:
	-	`sha256:8aabeaeb0e8463e33c9fca57607e676412891719e7d4ebeeb21d1ae921308dcb`  
		Last Modified: Tue, 18 Mar 2025 00:16:14 GMT  
		Size: 35.5 KB (35450 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; mips64le

```console
$ docker pull postfixadmin@sha256:be18c35a8469e6b8778a6086066243e74174dc81410c987bbdfdce98a6ef3c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.5 MB (156452094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d462c2c8c2f94830c5446b4667094901fb9a0c7cb91723c044229752eec832d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d36a7b1e0c4904256c3222f554e2f9053a6ce6cb06dac686a36004c2968943`  
		Last Modified: Tue, 25 Feb 2025 04:23:17 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878fe44e60469208a4e6a6cc56a06ba4bd6418ae0d09468c66a29bce7fc35e03`  
		Last Modified: Tue, 25 Feb 2025 04:23:25 GMT  
		Size: 80.7 MB (80668722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03653780888887368ef36859920d833d269d38c1e54ffb86bae392b6bfcfde65`  
		Last Modified: Tue, 25 Feb 2025 04:23:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37d16225b42033fad2e17de37197d7ddf58740cc1e834d88386251e1203d6bc`  
		Last Modified: Tue, 25 Feb 2025 04:43:12 GMT  
		Size: 20.1 MB (20069161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0240d2561c08c1860eeebaa66951069a40fc7b7c112653504c26fe56fc8e30`  
		Last Modified: Tue, 25 Feb 2025 04:43:09 GMT  
		Size: 437.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f085555607131ca41617fae1213ab0cb04ab6a67ce34f84c32f46a658c22f736`  
		Last Modified: Tue, 25 Feb 2025 04:43:09 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b722ef4e352880063d34fb43670365dec25dd3e8cc2ff63f8eb558e84d2451`  
		Last Modified: Fri, 14 Mar 2025 04:10:54 GMT  
		Size: 12.7 MB (12687312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd73db37539ff725d523ea872ee42d7620650fc5e5c95fd45d673bd97531cd3`  
		Last Modified: Fri, 14 Mar 2025 04:10:52 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbb084f0b24ab8483bb91e5a9f3032ef1af9c745d3b6413ca416249537e0a4e`  
		Last Modified: Fri, 14 Mar 2025 04:10:54 GMT  
		Size: 10.7 MB (10724408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210acfda509f7854379bb303a8d3bfe5a681311dc1168bae7f4b9bb9591f06f1`  
		Last Modified: Fri, 14 Mar 2025 04:10:52 GMT  
		Size: 2.5 KB (2460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4cd427db364536c973c4c471c0b684c32af48e0d350f3162b83b8285999c2e`  
		Last Modified: Fri, 14 Mar 2025 04:10:54 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a8e8577d3d43be8770a969a819d002b63b2714a71e4d8ab9bf54af69c199db`  
		Last Modified: Fri, 14 Mar 2025 04:10:53 GMT  
		Size: 896.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4b7327c04aff83cda218c5071095199860c420faea6044d6c47604c82ec73a`  
		Last Modified: Fri, 14 Mar 2025 08:09:59 GMT  
		Size: 973.8 KB (973800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5ca54f8121d21f16b4660f73db5f14252c239391a1db863888ac9314612dfa`  
		Last Modified: Fri, 14 Mar 2025 08:10:00 GMT  
		Size: 958.3 KB (958326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9606130f0e064ece28cb9bd4d396fe25e94d5f95a098aa2220b406614394c0`  
		Last Modified: Fri, 14 Mar 2025 08:09:59 GMT  
		Size: 8.0 KB (8048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebc92679547135842c6fd489f21d0fb83e43bffdb9c0f27a324c4d4a2d67123`  
		Last Modified: Fri, 14 Mar 2025 08:10:00 GMT  
		Size: 1.9 MB (1861473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151af988868c674ba3aacb12f4455af253272f29429cd32eb2f078cfa45533cd`  
		Last Modified: Fri, 14 Mar 2025 08:10:00 GMT  
		Size: 1.7 KB (1657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:76ef977bdf473117d77910687bb8b3a5e1884d2a7b284b465b632af150884520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048808ce8728abc7b0aeacf20d98846a76bcb666e14d7a784b29790facd69b41`

```dockerfile
```

-	Layers:
	-	`sha256:ff9e933462c89d8688b1435a7042c0951bdec26b87474f793b604b268bcbd9e1`  
		Last Modified: Fri, 14 Mar 2025 08:09:58 GMT  
		Size: 35.6 KB (35604 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:3edef554bd6fac4da81beeeccd47af7de084d7e8109e7547e5b5bb32eb97c607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.5 MB (185458732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac135697e1389ee450837ab07afbe37d8918ac2efb3eb705b42fe980809b931`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bbbae4d2dc0350f7df1634e33daf64fe78cb672182650c700a26750b33b64c`  
		Last Modified: Tue, 25 Feb 2025 02:59:24 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7f7bed916e76b3a3b176b4e6a5bcfe6e10e39a6c423be8fc3575115d7b1e06`  
		Last Modified: Tue, 25 Feb 2025 02:59:28 GMT  
		Size: 103.3 MB (103323545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d9943a0d5cef1bf22e1a6d5df4b38af8052474c28fe7d9188d33c9e0190742`  
		Last Modified: Tue, 25 Feb 2025 02:59:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f5eba5668f315d2ef7f70338fc89daecbca191bf9b5b6622280439ff5ceb4a7`  
		Last Modified: Tue, 25 Feb 2025 03:04:11 GMT  
		Size: 21.3 MB (21308442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bec4fde36a5fc026717bc0e1c4a8f85c6397c11d730b4d345fdb0b5014cc45`  
		Last Modified: Tue, 25 Feb 2025 03:04:06 GMT  
		Size: 435.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca66cb544073b521bd3bcd518135c4cf977a5939323c5191473a1b8a2a09cd05`  
		Last Modified: Tue, 25 Feb 2025 03:04:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5572026fea978b5ff4d0454110df96b23191aa3084fbd479e073dbe18f993c8`  
		Last Modified: Fri, 14 Mar 2025 02:17:06 GMT  
		Size: 12.7 MB (12689240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba1edbbf45a7d75b9274cfa349a57f2b4208701b03e532d0551df84211892b9`  
		Last Modified: Fri, 14 Mar 2025 02:17:04 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b740ee0591fb4780874c3a19049f432541ef41f4940b7282d31af84c6c2fb17d`  
		Last Modified: Fri, 14 Mar 2025 02:17:05 GMT  
		Size: 12.1 MB (12071699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90be7d0cd3b710616bd7cb64feab73e6a52e2e9e16173150a9c25045e3b91504`  
		Last Modified: Fri, 14 Mar 2025 02:17:04 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e774d4c5fbe78b0b09974fa80795453ff48bea49a1b9e2e75500f4efd4e2548`  
		Last Modified: Fri, 14 Mar 2025 02:17:06 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a457d31a783c2be318d1acdfb0f81f8dc50ba6e0900a2e8514174ffaeb744ff`  
		Last Modified: Fri, 14 Mar 2025 02:17:05 GMT  
		Size: 893.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc687e3cb6c414ac1758e86a4d7a89baa4d9d528e9c1d0ce254eb2b8dc39df2`  
		Last Modified: Fri, 14 Mar 2025 06:54:22 GMT  
		Size: 1.0 MB (1009357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee870431c82bcbf6cfdcd2dec1641fa1edfe19c897a91bc68c8626b69a91e6b`  
		Last Modified: Fri, 14 Mar 2025 06:54:22 GMT  
		Size: 1.1 MB (1127464 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287abcf5cf17f937848b67606dd45f7ef7c14edcb6273566bed2b30209a0e77c`  
		Last Modified: Fri, 14 Mar 2025 06:54:21 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd13a1b4b9901c1c3d30fd81151b1144805ec36df06172986db5ac225a30af5`  
		Last Modified: Fri, 14 Mar 2025 06:54:22 GMT  
		Size: 1.9 MB (1861471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e93ec33d37a93283c25a024822630f65a4aa1ea9f88d3a94a7ab35df550619`  
		Last Modified: Fri, 14 Mar 2025 06:54:22 GMT  
		Size: 1.7 KB (1657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:393bec2cd4542392b9af5c998bfb045228d839436ca4ec1da2bdcd6dbb429608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 KB (35581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a08a27600f5a016565475876e95981d7d534f48abc1958048a258f2bcab5dde`

```dockerfile
```

-	Layers:
	-	`sha256:49dc28fcce054dd71ddde3a8a27fcb321ebaa7d9967da119a3dec38e4f06d575`  
		Last Modified: Fri, 14 Mar 2025 06:54:21 GMT  
		Size: 35.6 KB (35581 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:latest` - linux; s390x

```console
$ docker pull postfixadmin@sha256:db04f14e0aa175c43749d3307543fdc6fceefb9db94f23b83fc5072e59094dba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155060085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15bde4430850cc390ceb4d1c38ab957a26435e67d8e1402d3c7e82a2b1feaf66`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["apache2-foreground"]`

```dockerfile
# Sat, 21 Dec 2024 02:12:45 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
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
	-	`sha256:6d4d169c55c2ee02478b6705c4ba9e6795bffbbb872a22adfd95fb2484f2e85c`  
		Last Modified: Tue, 25 Feb 2025 01:30:03 GMT  
		Size: 26.9 MB (26864838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f83dfaf87e0f897b620f8faafcd35d93785d305460fb8a1f24f178152dc8ef4`  
		Last Modified: Tue, 25 Feb 2025 02:47:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382c1a79d42d9a6f73ff6106cec8445a8fb8bc6a78380c02024ff5e71c740938`  
		Last Modified: Tue, 25 Feb 2025 02:47:06 GMT  
		Size: 80.8 MB (80817122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd5ce3ea58656e03c29355d087376523130702c7a182e93a6e6c775d2e795dd`  
		Last Modified: Tue, 25 Feb 2025 02:47:05 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ca9e9fc0029c44454cc7b3021d275f272be12d935e5bcbf513a001e160df1e`  
		Last Modified: Tue, 25 Feb 2025 02:50:57 GMT  
		Size: 19.9 MB (19895168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312727822926b01c3ea7b38ae79e9f14f546dab08bbfd780821249610ae4aa7e`  
		Last Modified: Tue, 25 Feb 2025 02:50:56 GMT  
		Size: 439.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d51730a67b490b800306ddce51f95b7fc9ec61621c6c0c350bd502364beda8`  
		Last Modified: Tue, 25 Feb 2025 02:50:56 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c05d920dd049638352737057022d43548e60d552e07936508c99aaae27daadc`  
		Last Modified: Fri, 14 Mar 2025 02:20:36 GMT  
		Size: 12.7 MB (12688028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990ac753b7c72d5c39a5198439252d090c0eaea97c6cffe6d4a22c768778bf37`  
		Last Modified: Fri, 14 Mar 2025 02:20:35 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8a6b0e3863568e1b3dbffe343af1f54c27435a5bdcec1730c8cd44639ea47c`  
		Last Modified: Fri, 14 Mar 2025 02:20:36 GMT  
		Size: 10.9 MB (10875633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e488b5ef7491fd0795d834455208d509fdb654a7697f344b2b1224dc4def8ed5`  
		Last Modified: Fri, 14 Mar 2025 02:20:35 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa001293568c7f0b6771e1c953c81440aa9fe2ab84ba2ec81c1170f4f715a45`  
		Last Modified: Fri, 14 Mar 2025 02:20:36 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b10a28887b80d3d6ea4baf2c6925465b19232af70a1c5e4d34c05367e90622`  
		Last Modified: Fri, 14 Mar 2025 02:20:36 GMT  
		Size: 894.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906e8fc9b59999c4910af678d0ccaae4a979c3c24593c13ec66c7d84f9dc832f`  
		Last Modified: Fri, 14 Mar 2025 14:29:47 GMT  
		Size: 1.1 MB (1057580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5abcc0c88fbfcd85c7aad15b75f61f579262cc9aa9eb7ebcb1d69b34468a727`  
		Last Modified: Fri, 14 Mar 2025 14:29:47 GMT  
		Size: 985.0 KB (985040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d655f4064fd52cdaefc34406e7522e76a243ce55e65093ba5cfcb5de8e05cde7`  
		Last Modified: Fri, 14 Mar 2025 14:29:47 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c49767d8af0cac7e39f82817c15f67912da1736083c6ec8f881719367946b56`  
		Last Modified: Fri, 14 Mar 2025 14:29:47 GMT  
		Size: 1.9 MB (1861471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdbd905d6bc900a2d7e0ef3e04d86b6ba715bfdfb439d7fea57f144cc3a94f0`  
		Last Modified: Fri, 14 Mar 2025 14:29:48 GMT  
		Size: 1.7 KB (1659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:latest` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:dc58736aaeb598c04ed35b29ee7285fb40078ae04a3de37d83769cef2e13fd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 KB (35497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f06051edbda7d0beead38bd1395de1057ad23f10363a28eb826626e800eed6`

```dockerfile
```

-	Layers:
	-	`sha256:380f76795189eecc6bd5060cf1c6f37713c345fb89411ff376e1ba3a76a4d5b7`  
		Last Modified: Fri, 14 Mar 2025 14:29:47 GMT  
		Size: 35.5 KB (35497 bytes)  
		MIME: application/vnd.in-toto+json
