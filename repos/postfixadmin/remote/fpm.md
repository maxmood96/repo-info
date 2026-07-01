## `postfixadmin:fpm`

```console
$ docker pull postfixadmin@sha256:5e279c8e68fc0260390002d9c6a5e1b82145cb142309723116d9139a224f83fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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

### `postfixadmin:fpm` - linux; amd64

```console
$ docker pull postfixadmin@sha256:cee55c7bd16438c39f325d3b5f5d62552c0f15ca3615a88d7304b16f58657125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200609914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9349750c56125544d253730800d87642571b2e5a36e0d687cda520aaa4e9c2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:22:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:22:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:22:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:22:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:22:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:22:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:22:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:22:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Jun 2026 01:22:27 GMT
ENV PHP_VERSION=8.3.31
# Wed, 24 Jun 2026 01:22:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 24 Jun 2026 01:22:27 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 24 Jun 2026 01:27:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:27:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:30:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:30:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:30:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:30:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:30:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:30:15 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:30:16 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 24 Jun 2026 01:30:16 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Jun 2026 01:30:16 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jun 2026 01:30:16 GMT
CMD ["php-fpm"]
# Tue, 30 Jun 2026 19:07:36 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 30 Jun 2026 19:07:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 19:07:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:07:55 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:07:55 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:07:55 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:07:55 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:07:55 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 19:07:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:07:55 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:07:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 19:08:04 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:08:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 19:08:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a467f63f31d2616c310055046c605a93ea1fe48078c67861e78cf37d279d7777`  
		Last Modified: Wed, 24 Jun 2026 01:25:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cd8cf70218fc4e56541cb3e05a22d4ab3812f5f4c5e22072f81d2011085ce`  
		Last Modified: Wed, 24 Jun 2026 01:25:54 GMT  
		Size: 117.8 MB (117840326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bdf34c4bd20e1485cd978330852c28fc37950991d9f50dbd56c921a19888db`  
		Last Modified: Wed, 24 Jun 2026 01:25:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa3ccdc6ffb9b10501c91ce5d0a88494949ec01d8c303f7f4185eabcc0b0d47`  
		Last Modified: Wed, 24 Jun 2026 01:30:26 GMT  
		Size: 12.8 MB (12751425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395de67766e804698a92f42be97873942a39aae7f9424338fe4da702d227ef86`  
		Last Modified: Wed, 24 Jun 2026 01:30:26 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e445e7a850440119c17b76130a9c6536a9102a01e143f7395ab45ffd7f7dc4d`  
		Last Modified: Wed, 24 Jun 2026 01:30:26 GMT  
		Size: 11.9 MB (11902600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedf0c05b5094f8a4ad3c9e61248b4d55bcc9b97bdab0fc8eac75aeee4475522`  
		Last Modified: Wed, 24 Jun 2026 01:30:26 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145097da7083d8b77225883b374905f06e04418d2bde81b1f3444428652cc303`  
		Last Modified: Wed, 24 Jun 2026 01:30:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7526504ade7bc8095eaab3ffdb347b3425686bf44d0a3d23fee628dbadbd9a2b`  
		Last Modified: Wed, 24 Jun 2026 01:30:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e990bc4863f186c7ec232e905939996566f947ca3bcd634f67eb4974a0764c8f`  
		Last Modified: Wed, 24 Jun 2026 01:30:27 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b02f7d50d0130ad90ba89c3e0655152db3d129df962d8e0d724a5169d77f73f`  
		Last Modified: Tue, 30 Jun 2026 19:08:10 GMT  
		Size: 1.3 MB (1328833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f359998f426689e773dffcf78a6ebb7cbce7b2741fe997f24de2c896adabf5c2`  
		Last Modified: Tue, 30 Jun 2026 19:08:10 GMT  
		Size: 443.6 KB (443587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:241d1a55ac3b7b01ec0456e10a8ff6a4986a70b2e151966ea25a4c13c1526f83`  
		Last Modified: Tue, 30 Jun 2026 19:08:10 GMT  
		Size: 2.6 MB (2603510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e75fbd335b28280eb8f77d03ae4a99e309bbe0a8b983c53739cf25beaa479`  
		Last Modified: Tue, 30 Jun 2026 19:08:10 GMT  
		Size: 1.7 KB (1657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d0b045853037ef3daf1c5aaf89693aefd697c22b2d13c82c6d509e0a78f01e`  
		Last Modified: Tue, 30 Jun 2026 19:08:11 GMT  
		Size: 823.3 KB (823346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061ad5a53fabf2705dae953c7e832d37cc04cec53abbe7e91d0b3c7e65c3dca4`  
		Last Modified: Tue, 30 Jun 2026 19:08:12 GMT  
		Size: 23.1 MB (23116031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:6876da8e915e23fa2ff3004922c0adc54bc9044c7e473b0eeaf8b5cb5178c268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 KB (39515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465e4501eaeb8ec4d0d9aa1c4030168dced5e671df66ef5ad41270ebe850f1e7`

```dockerfile
```

-	Layers:
	-	`sha256:62a3b646387939c5990e0fc80706314cd947f0802be8719427944b66b3ba7646`  
		Last Modified: Tue, 30 Jun 2026 19:08:10 GMT  
		Size: 39.5 KB (39515 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:966825db76e3f9abd147d71825803ee7e831ebeaea8ada6f2b7f8db9d2fe14fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.5 MB (163522504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e5c52528645d328eaab43f01f0c2520763dedf2a91fd05e7c01ff94cf5cb08`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:24:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:25:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:25:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:25:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:25:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:25:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:25:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:25:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:25:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Jun 2026 01:25:13 GMT
ENV PHP_VERSION=8.3.31
# Wed, 24 Jun 2026 01:25:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 24 Jun 2026 01:25:13 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 24 Jun 2026 01:35:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:35:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:38:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:38:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:38:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:38:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:38:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:38:23 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:38:24 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 24 Jun 2026 01:38:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Jun 2026 01:38:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jun 2026 01:38:24 GMT
CMD ["php-fpm"]
# Tue, 30 Jun 2026 19:10:12 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 30 Jun 2026 19:10:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 19:10:39 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:10:39 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:10:39 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:10:39 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:10:39 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:10:39 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 19:10:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:10:40 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:10:40 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 19:10:50 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:10:50 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 19:10:50 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:81c84b0273952340067af970e1fe77a42ea83b4ed1a53319e258d5f1077848f0`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 26.2 MB (26211051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526200a0cd979e2ecad3128c3b45eb0a83aefc6e3ecfe02a7d865315efa77f84`  
		Last Modified: Wed, 24 Jun 2026 01:28:28 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb5d6f746a98bbce2b6ba0731a4d86e5cf36f904772846a3855fd85b3fd39fd`  
		Last Modified: Wed, 24 Jun 2026 01:28:31 GMT  
		Size: 86.3 MB (86256113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb70fdbc2a007bdfe6e725c531982e3be857c39c21d03a8654aaafbc6d20948`  
		Last Modified: Wed, 24 Jun 2026 01:28:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4d697ed043dca28cde3dc3dcd33cb689fe44bddd9748cd1deac9e7d5e98b03`  
		Last Modified: Wed, 24 Jun 2026 01:38:34 GMT  
		Size: 12.7 MB (12749043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d670296079c8434271b4c4abfe406ee1158ebbaa3b2c68ac649666bf189910b`  
		Last Modified: Wed, 24 Jun 2026 01:38:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840d921c14927ed9c9bae5158a14629265be99bd1cab51e5d9ed9752c5ae4254`  
		Last Modified: Wed, 24 Jun 2026 01:38:34 GMT  
		Size: 10.1 MB (10086205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80645ae34365e1fb1788f396f65186ef74f9c1fe641cb5d79133ec5630df54f`  
		Last Modified: Wed, 24 Jun 2026 01:38:33 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb560ace9292784ffaa4c8d1afe5beae8f598ff25adbad0e9511ebf7767cf6ed`  
		Last Modified: Wed, 24 Jun 2026 01:38:35 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a061aaa7b768239c0add4419fb1bbdc4a9987c1cf19a5577c20838e5bbb8332`  
		Last Modified: Wed, 24 Jun 2026 01:38:34 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b8900de38f825d4e6801bccb2d97c2064deec76db224bb8d3e85d53daa6844`  
		Last Modified: Wed, 24 Jun 2026 01:38:35 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8c24f2677223e8ba7793d9d52621142b1535d8cc99332447dba9bd26fdbcaf`  
		Last Modified: Tue, 30 Jun 2026 19:10:57 GMT  
		Size: 1.3 MB (1266127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f954381924309e7cba8f88650f7ea2e772f383206bc1f84e79d4182b85b3599d`  
		Last Modified: Tue, 30 Jun 2026 19:10:57 GMT  
		Size: 398.7 KB (398746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492d774fd1d98933bcffedba73f4a081328febba1a0de1a07df9b373bca6198b`  
		Last Modified: Tue, 30 Jun 2026 19:10:57 GMT  
		Size: 2.6 MB (2603507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a2ebd7dd10a1744bffc225ea8d4e87a023ac65815beeb1690e91fb6f0a4a59`  
		Last Modified: Tue, 30 Jun 2026 19:10:57 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757edf395f3fa3a62629d2c12f46e14dd7cd649d4624a18ce7c08b5b004c5aa6`  
		Last Modified: Tue, 30 Jun 2026 19:10:58 GMT  
		Size: 823.3 KB (823340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9e54dd50cab323c59b5752dcba56471637abca4e4182bc6d8ebee4973dabf2`  
		Last Modified: Tue, 30 Jun 2026 19:10:59 GMT  
		Size: 23.1 MB (23113545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:e75533a5731d62dfc68c2dd9cd09e96af5683d00973ef800a7cd4e88043a2a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ede850f3ed71c36fb319ac762c3bdb547b620c64a111ba3653a5214b33797e2`

```dockerfile
```

-	Layers:
	-	`sha256:09a78cf29355945f4baf30531893341d93ff7787db1b3110c643430d5cc4ae02`  
		Last Modified: Tue, 30 Jun 2026 19:10:56 GMT  
		Size: 39.6 KB (39649 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:116a0a330fad49f16cf6b40ac6e3eb1501a186fa3641872904180a2b36f21671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 MB (193233958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4bca8b522e38852d9e3b065acfb9a70b5d385f7558817c28f8417483d5abb86`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:23:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:23:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:23:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:23:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:23:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:23:37 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:23:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:23:37 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:23:37 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Jun 2026 01:23:37 GMT
ENV PHP_VERSION=8.3.31
# Wed, 24 Jun 2026 01:23:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 24 Jun 2026 01:23:37 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 24 Jun 2026 01:27:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:27:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:31:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:31:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:31:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:31:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:31:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:31:11 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:31:11 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 24 Jun 2026 01:31:11 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Jun 2026 01:31:11 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jun 2026 01:31:11 GMT
CMD ["php-fpm"]
# Tue, 30 Jun 2026 19:07:43 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 30 Jun 2026 19:07:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 19:08:07 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:08:07 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:08:07 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:08:07 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:08:07 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:08:07 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 19:08:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:08:07 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:08:07 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 19:08:16 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:08:16 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 19:08:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb9a66730e215ff882cd891e3090c2afb7e7671492a78b9e61bfa3540e94e19`  
		Last Modified: Wed, 24 Jun 2026 01:27:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c2c1baa313821f1b4cc6affe03c9f928c43fc60709f46d5e0bd2f894a5696ed`  
		Last Modified: Wed, 24 Jun 2026 01:27:08 GMT  
		Size: 110.2 MB (110169516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92b396066262939b103f71dbd0bcc62014832bf812c49721c0ec2fe6ce28202`  
		Last Modified: Wed, 24 Jun 2026 01:27:04 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0229c81e899f5cbd43eb929f385146e2ae25ab559705408bb2cf9d6533eed23b`  
		Last Modified: Wed, 24 Jun 2026 01:31:22 GMT  
		Size: 12.8 MB (12751041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b362823c00af4885e1fa4f8b08a5bb093b936b787bca4dc6da9e1d1d99b0b3cb`  
		Last Modified: Wed, 24 Jun 2026 01:31:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41de94435556e0d1c2a49fd13cb47519a846d58ab7db140f5184c9337372a15`  
		Last Modified: Wed, 24 Jun 2026 01:31:22 GMT  
		Size: 11.9 MB (11925538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc143ac3a31bcb39a11468da95823525c97dcea1927837677d834947a7b96d3`  
		Last Modified: Wed, 24 Jun 2026 01:31:21 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7881d63e16971d607513ae10408315828e121a032867d1aaae10f7a84570cde2`  
		Last Modified: Wed, 24 Jun 2026 01:31:22 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4f62880708a441814cbaff7ebff84c95a2c87e948b2c24855b97e6f907a007`  
		Last Modified: Wed, 24 Jun 2026 01:31:23 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d835933cad28ac9e92586d2dcda7a43579d45436ae58216620d046535aecbdc`  
		Last Modified: Wed, 24 Jun 2026 01:31:24 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1305ac25c693a4be4a95f09ab0d38b3d30b5a0cd2f54b9efe576351132038456`  
		Last Modified: Tue, 30 Jun 2026 19:08:22 GMT  
		Size: 1.2 MB (1242572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d58afec193e9f3fcf152e6c7828b78c00099eabf4e85b83a0aeff4104fa4e7`  
		Last Modified: Tue, 30 Jun 2026 19:08:22 GMT  
		Size: 439.4 KB (439445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41e6dc86afa7dcab3f7c09e49580c9a3341ee63a06433c893ce875d69f8e874c`  
		Last Modified: Tue, 30 Jun 2026 19:08:22 GMT  
		Size: 2.6 MB (2603506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48cf4cb1517bbef54c0e53f641e1b8aeb9bbeb61d14dd8808125621cf40bba1`  
		Last Modified: Tue, 30 Jun 2026 19:08:22 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc5c99bd807e0dbba515b9124ebb5e777ee3d9b1da494e6f225294267d992ff`  
		Last Modified: Tue, 30 Jun 2026 19:08:23 GMT  
		Size: 823.3 KB (823341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7c8b87db595455f453d790aa9051bbec9930e8b0dd77d307967f27a1a096a1`  
		Last Modified: Tue, 30 Jun 2026 19:08:24 GMT  
		Size: 23.1 MB (23115634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:9d2df2dae7af2f313d72c01581579b3fb59afbf1aa5ba444eaa9cf3f8cc45d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 KB (39690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ef28c75190e1f00a91d459a349a1c719070193c9770763200a50a12b099add`

```dockerfile
```

-	Layers:
	-	`sha256:cdece0ecb088b273ee793dbf3d1d39a353655013882d5fac361bb1b0b3fc874f`  
		Last Modified: Tue, 30 Jun 2026 19:08:22 GMT  
		Size: 39.7 KB (39690 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm` - linux; 386

```console
$ docker pull postfixadmin@sha256:f906c7d30e67a169a952d07ddb503d4c53c401e4c8cbb48546328f96ff667623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.6 MB (200607862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab6d6e048cbf38d6712dc38021a33ddee79c6f937a8ba7ce9a1acc0fedb5bf6`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:18:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:18:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:18:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:18:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:18:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:18:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:18:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:18:27 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Jun 2026 01:18:27 GMT
ENV PHP_VERSION=8.3.31
# Wed, 24 Jun 2026 01:18:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 24 Jun 2026 01:18:27 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 24 Jun 2026 01:25:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:25:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:27:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:27:58 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:27:58 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:27:59 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:27:59 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:27:59 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:27:59 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 24 Jun 2026 01:27:59 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Jun 2026 01:27:59 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jun 2026 01:27:59 GMT
CMD ["php-fpm"]
# Tue, 30 Jun 2026 19:09:36 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 30 Jun 2026 19:09:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 19:09:58 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:09:58 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:09:58 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:09:58 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:09:58 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:09:59 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 19:09:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:09:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:09:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 19:10:07 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:10:07 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 19:10:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:984d3baa100eb8c4d7c83b7c23b4748e508aa6ed5903297f02be90a681f52d41`  
		Last Modified: Wed, 24 Jun 2026 00:28:38 GMT  
		Size: 31.3 MB (31301210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc8cde703685594d9489ebec753dc9b1ee7afc89869a06cdd6f144eb5f4f163`  
		Last Modified: Wed, 24 Jun 2026 01:21:52 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bff0ee2082085d79e705259859cd76ab77c9e20c4e8996175dd932b36fc6bfd`  
		Last Modified: Wed, 24 Jun 2026 01:21:56 GMT  
		Size: 116.1 MB (116142380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c3577a1c58e9e415b10c6dd7b794dd9070a161853efcfd724b95a27b1261d9`  
		Last Modified: Wed, 24 Jun 2026 01:21:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174c5ed787d06100c7ec37ddfaaf778ef3fa970137a0d440a31bac93f27d4cad`  
		Last Modified: Wed, 24 Jun 2026 01:28:09 GMT  
		Size: 12.8 MB (12750367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df612f68c4b0f3cb3f1438ecbab86d422b612d6888ddf5ead16ad2bffe2fb7f1`  
		Last Modified: Wed, 24 Jun 2026 01:28:08 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe4d0c085e49d0d69d49b2079f028cb349751e5b5cac0ba4a430509bf059202`  
		Last Modified: Wed, 24 Jun 2026 01:28:09 GMT  
		Size: 12.1 MB (12109914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f8e6afd6ef50275c8e93e0a14d9adf8910ddbf9d015713b493227f99512684`  
		Last Modified: Wed, 24 Jun 2026 01:28:08 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30f670b77b7fc5ce5508236b85429be5a9d32c7d657c5ef2d2e852bdb86f68a`  
		Last Modified: Wed, 24 Jun 2026 01:28:09 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa49662aa66d8f1f016c1b550a96afa955bf6021015aaa9bd22819bc27a1dab6`  
		Last Modified: Wed, 24 Jun 2026 01:28:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2da0468377449efe36a2089b9a7114dfdb1d6643fdb1d64862873eaeb0d837d`  
		Last Modified: Wed, 24 Jun 2026 01:28:11 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f4eb598817a68a4b02b3c4516b748ba44748e73744fed780ca886eb32c8966`  
		Last Modified: Tue, 30 Jun 2026 19:10:14 GMT  
		Size: 1.3 MB (1287757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bf044f64f54d93697b2f22ad2a1d6e282f0bff3e9c0f495d53a162339e1205`  
		Last Modified: Tue, 30 Jun 2026 19:10:14 GMT  
		Size: 459.3 KB (459344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0576abb1b5e762e1b684279a1e983124d728072bda1c4eaa2cd552dd501c9601`  
		Last Modified: Tue, 30 Jun 2026 19:10:14 GMT  
		Size: 2.6 MB (2603506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d9e8e250d7dad36669b1e7c7b0a035118249558de7e3e432dbc911ddaf4c1b`  
		Last Modified: Tue, 30 Jun 2026 19:10:14 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3052f72e817bade628fcdc2d9a77877e8b27e6ac8a8d89f07e0f533e56704d`  
		Last Modified: Tue, 30 Jun 2026 19:10:15 GMT  
		Size: 823.3 KB (823347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51aa4a08eafb2354be69ccc1b742aa41b70b9da161d65b78473f16c1b1253c3a`  
		Last Modified: Tue, 30 Jun 2026 19:10:16 GMT  
		Size: 23.1 MB (23115207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:cfb07f856aba161413ce0dbd5b21986d829f8233b2ff8bd59b1ad589aba161a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 KB (39469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30b61202faa138a956cb053ef348b59208381d6366b9e8073b41349ce451655`

```dockerfile
```

-	Layers:
	-	`sha256:0f013b81c9996e63c6e393f998456f4443bd220bd19a7b59f6327d35f281c2c3`  
		Last Modified: Tue, 30 Jun 2026 19:10:13 GMT  
		Size: 39.5 KB (39469 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:d4d5b7e66d1aaaade7c99527a9baaea6c7c4143b6d08f4cf884e02104ba69aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196675471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a087a82ce9b002effde540e59eef2359cf8f04dc9e49e67a6583501df166941`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:47:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:48:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:48:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:48:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:48:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:48:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_VERSION=8.3.31
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 24 Jun 2026 01:48:32 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 24 Jun 2026 02:27:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 02:27:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:34:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 02:34:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:34:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 02:34:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 02:34:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 02:34:46 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 02:34:46 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 24 Jun 2026 02:34:46 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Jun 2026 02:34:46 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jun 2026 02:34:46 GMT
CMD ["php-fpm"]
# Tue, 30 Jun 2026 19:06:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 30 Jun 2026 19:06:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 19:07:36 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:07:36 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:07:36 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:07:36 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:07:36 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:07:40 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 19:07:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:07:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:07:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 19:08:04 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:08:04 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 19:08:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:639e1c13483ea279c94219be2736856262d8dd2efeff3e6d309f11a66aba21fb`  
		Last Modified: Wed, 24 Jun 2026 00:30:29 GMT  
		Size: 33.6 MB (33606388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64e77efe72bf9ab01112d6628b561df155e58c8abb9a5c50ca8c3c2d3054015`  
		Last Modified: Wed, 24 Jun 2026 01:53:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a885bf66539705f27716480915d14f847c62afd59e7c77b0d7a2ec11fcf9f8`  
		Last Modified: Wed, 24 Jun 2026 01:53:59 GMT  
		Size: 109.6 MB (109598576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6270c259f3728f03e6c19bf8bc89dd6cfe4f6a02bdbe4c4a66ac81d4e83afc0f`  
		Last Modified: Wed, 24 Jun 2026 01:53:55 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e993bd805353a37aff8f6793ef5b7c519eb45d67f9a5eb3aa16f7b7edb008146`  
		Last Modified: Wed, 24 Jun 2026 02:31:07 GMT  
		Size: 12.8 MB (12750414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47eee37f7cc7b4a29cb70ad1a0dd48dc4e30b688b5015cf3448281b45ee99f1a`  
		Last Modified: Wed, 24 Jun 2026 02:31:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e95eea082b0973fafd1d8e8c1cc98fd04a9be005a39954dc4d76d5dc03e561bd`  
		Last Modified: Wed, 24 Jun 2026 02:35:08 GMT  
		Size: 12.4 MB (12440312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b1fcb52c414cbc6d206c76a672f76100c964f277195d528508c6137781c086`  
		Last Modified: Wed, 24 Jun 2026 02:35:07 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b9c52388301003f7c11e201f23b41d720274c6b0e7cbd3231d03226a95709c`  
		Last Modified: Wed, 24 Jun 2026 02:35:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a81ead3cea4df8a3230f97669e60f6684c22caa3c4245b9d10854b8f8b8a42`  
		Last Modified: Wed, 24 Jun 2026 02:35:07 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c1ec6a87cbfd9e02a7a67615b0a073e9f7e127f18ace280a17143d5e0474a6`  
		Last Modified: Wed, 24 Jun 2026 02:35:09 GMT  
		Size: 9.3 KB (9252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7bab4a7b320d110aa8f69a9a70cd60af2196879ba34b7ef9712b39216feb47`  
		Last Modified: Tue, 30 Jun 2026 19:08:17 GMT  
		Size: 1.2 MB (1244861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c400f4b3b81a4e51bed8f5257fce6d4685147d6ca615f0579a1c9b11e3e81c1`  
		Last Modified: Tue, 30 Jun 2026 19:08:17 GMT  
		Size: 478.3 KB (478257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3230b8036d5f7c0c4853482bd1d2e8bf02849b748a31462d94ed4c29ccd39f1`  
		Last Modified: Tue, 30 Jun 2026 19:08:17 GMT  
		Size: 2.6 MB (2603511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56edbfcb546ad33c49dfcac8680fff19df5ecc94c351775af1fc5b81864a121b`  
		Last Modified: Tue, 30 Jun 2026 19:08:17 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36f6436b2746cfb0c62540f95906523ce409ba633384fb89bed501649853f2a0`  
		Last Modified: Tue, 30 Jun 2026 19:08:18 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02dfa05ae5a1e80be65a3eb3c8d67db6b2c96027d19168387488affd014ff59`  
		Last Modified: Tue, 30 Jun 2026 19:08:19 GMT  
		Size: 23.1 MB (23114983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:297fabbb5d611da74ddef299f3613371da2f437bec0e91bb710e48deb1c30e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f2011b4e27533b973ea8e5bdfebbbd321b515ef6a64a7722fbd691944d196e`

```dockerfile
```

-	Layers:
	-	`sha256:df4c63042ecbbd479f223658973bf46a79241a3d24ae9baa07868234dd3a3586`  
		Last Modified: Tue, 30 Jun 2026 19:08:17 GMT  
		Size: 39.6 KB (39575 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm` - linux; riscv64

```console
$ docker pull postfixadmin@sha256:a944baf2edeaef1a5470bb5e050152fb0666408d97614cc14653ff11a0b42de3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.3 MB (227341009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5fa461536642803f4330f9f64b6b16755ed4afcb69a58c48c1ee4931dcff31`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1782172800'
# Thu, 25 Jun 2026 03:10:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 25 Jun 2026 03:12:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 25 Jun 2026 03:12:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 25 Jun 2026 03:12:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Jun 2026 03:12:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Jun 2026 03:12:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Jun 2026 03:12:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Jun 2026 03:12:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Jun 2026 03:12:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Jun 2026 03:12:45 GMT
ENV PHP_VERSION=8.3.31
# Thu, 25 Jun 2026 03:12:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Thu, 25 Jun 2026 03:12:45 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Thu, 25 Jun 2026 10:44:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 25 Jun 2026 10:44:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 13:21:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Jun 2026 13:21:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Jun 2026 13:21:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Jun 2026 13:21:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Jun 2026 13:21:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Jun 2026 13:21:13 GMT
WORKDIR /var/www/html
# Thu, 25 Jun 2026 13:21:14 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Jun 2026 13:21:14 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Jun 2026 13:21:14 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Jun 2026 13:21:14 GMT
CMD ["php-fpm"]
# Sun, 28 Jun 2026 15:40:24 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Sun, 28 Jun 2026 15:40:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sun, 28 Jun 2026 15:44:32 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Sun, 28 Jun 2026 15:44:32 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Sun, 28 Jun 2026 15:44:32 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Sun, 28 Jun 2026 15:44:32 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Sun, 28 Jun 2026 15:44:32 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 22:58:22 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 22:58:22 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 22:58:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 22:58:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 22:59:41 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 22:59:41 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 22:59:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:58bface994ba631e609596a2ca5032d9d75de27f1b6476034b581e226205adab`  
		Last Modified: Wed, 24 Jun 2026 03:41:42 GMT  
		Size: 28.3 MB (28282378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5857a11081278c6794a11415cb81a403d5e56a1e98d5a05a474e4751b6bbbbab`  
		Last Modified: Thu, 25 Jun 2026 04:15:49 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f64aa12de76796ba620c1f61dfbf00595d86b22e83c70e23ab80e22f6f224c`  
		Last Modified: Thu, 25 Jun 2026 04:16:17 GMT  
		Size: 146.6 MB (146585183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75d48c7e93a7ac2ea8e95b78d618385a5865f4b0674a6016d1f7a6e51225d7c`  
		Last Modified: Thu, 25 Jun 2026 04:15:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f7087cd967ab0e0fd89621acd6fc6eb00edae45fb37ecad59331a58ee30f51`  
		Last Modified: Thu, 25 Jun 2026 11:36:57 GMT  
		Size: 12.8 MB (12758000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9abe71e45d83ec747e4194c364a76493be5db187cf00d0a8d61ef20095febf9`  
		Last Modified: Thu, 25 Jun 2026 11:36:53 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbeb8a122ce1c4621431ef8d08b55f32567fe6f5b0d97bc07d0ef8529d5728f8`  
		Last Modified: Thu, 25 Jun 2026 13:24:08 GMT  
		Size: 11.5 MB (11467608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c40289b7226abc8e405f8c33a78255c08d0602485125ec4ab294b4ae98bc66e`  
		Last Modified: Thu, 25 Jun 2026 13:24:06 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1be73edae3d5d9c3a92d10d5daf1f883ae16fef176ff85a68f5b287eb5d0691`  
		Last Modified: Thu, 25 Jun 2026 13:24:06 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28da24ad6367e0332f313c5faa2f2177bd349567a5d29f6e2d7588ebd0476d45`  
		Last Modified: Thu, 25 Jun 2026 13:24:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a7de4065080a1df4af3a0b9589c7de95783e4a02cae5484879d74c1496ab6b`  
		Last Modified: Thu, 25 Jun 2026 13:24:08 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b760d5e79adf071d24d761aad566f9f15bb292d3f32410b928ea9c4de3a8a3f`  
		Last Modified: Tue, 30 Jun 2026 23:00:49 GMT  
		Size: 1.2 MB (1242215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4227b4e1587c0646c3a1e1e2b3a2910ffd7211c3f96d5f67dbeaa15170ae1ce1`  
		Last Modified: Tue, 30 Jun 2026 23:00:50 GMT  
		Size: 432.7 KB (432690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5a40276d196547810b24196c042c0be255d5adb0ff1d6fec4d02e7d7a9f1da`  
		Last Modified: Tue, 30 Jun 2026 23:00:49 GMT  
		Size: 2.6 MB (2603516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d206bdcd39a55a075c8f91bab72e91bc3298034ae93f4b5a397c9ab9341ec16b`  
		Last Modified: Tue, 30 Jun 2026 23:00:49 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe97315f0e1b74c4fc4931143300ea0d920df27054730b246754b1e037adc02`  
		Last Modified: Tue, 30 Jun 2026 23:00:51 GMT  
		Size: 823.3 KB (823347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:889e71da25baee3168380b495c908d990371cc75adf027eefcef13b9eee962b7`  
		Last Modified: Tue, 30 Jun 2026 23:00:55 GMT  
		Size: 23.1 MB (23131222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:ef295b122caa78ccbeedc1952b66672c7dcbacbca3ded14b9906b48118bac8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5869e2b156bbe9f1f6db1e03ecb3ae285755531d8409287a0b36c72e3ecc3975`

```dockerfile
```

-	Layers:
	-	`sha256:630c5932d147b718d72feab545fff82bef2a156fe8a06868c5518456851d5349`  
		Last Modified: Tue, 30 Jun 2026 23:00:49 GMT  
		Size: 39.6 KB (39575 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm` - linux; s390x

```console
$ docker pull postfixadmin@sha256:7bd602176902e99724e266644ec1267d3aced8a9e75067d5f88a8c9b426bae4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.2 MB (175237814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ee2fb696f8003aec7b0cf303743b719ac590fc41427fd89c0142a108ee4494`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:19:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 24 Jun 2026 01:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 24 Jun 2026 01:19:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 24 Jun 2026 01:19:53 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_VERSION=8.3.31
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.31.tar.xz.asc
# Wed, 24 Jun 2026 01:19:53 GMT
ENV PHP_SHA256=66410cee07f4b2baeb0843140bb2a2b52ef930b5cf9b3d6e6d158b33aae8fa37
# Wed, 24 Jun 2026 01:43:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 24 Jun 2026 01:43:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:47:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 24 Jun 2026 01:47:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 01:47:13 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 24 Jun 2026 01:47:13 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 24 Jun 2026 01:47:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 24 Jun 2026 01:47:13 GMT
WORKDIR /var/www/html
# Wed, 24 Jun 2026 01:47:13 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 24 Jun 2026 01:47:13 GMT
STOPSIGNAL SIGQUIT
# Wed, 24 Jun 2026 01:47:13 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 24 Jun 2026 01:47:13 GMT
CMD ["php-fpm"]
# Tue, 30 Jun 2026 19:06:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 30 Jun 2026 19:06:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 30 Jun 2026 19:07:15 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:07:15 GMT
ARG POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:07:15 GMT
ARG POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:07:15 GMT
ENV POSTFIXADMIN_VERSION=4.0.4
# Tue, 30 Jun 2026 19:07:15 GMT
ENV POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
# Tue, 30 Jun 2026 19:07:16 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Tue, 30 Jun 2026 19:07:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:07:16 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 30 Jun 2026 19:07:16 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 30 Jun 2026 19:07:25 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.4 POSTFIXADMIN_SHA512=cce293e92e03f06a20ddbe09a9faec251af3f166f38565429d791feaf832096344a62656bab2a60bbd360545c1a0bd3ed05e11f4a4e46f04858e84639c5391dd
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Tue, 30 Jun 2026 19:07:25 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 30 Jun 2026 19:07:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b6a0af2ceb4b698210b8776157288a3fb06e46aaf75d641139449fcc50ce430d`  
		Last Modified: Wed, 24 Jun 2026 00:28:43 GMT  
		Size: 29.9 MB (29851381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00bb5043cbaffad0e2447070b4a5f2b29ea8f92190db347856d7a7b2afa8db0a`  
		Last Modified: Wed, 24 Jun 2026 01:23:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba630d3700db23d64e3bf4975aae41a0cef309b5e0da02aa4e11522332f82a6`  
		Last Modified: Wed, 24 Jun 2026 01:23:52 GMT  
		Size: 92.6 MB (92572737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8d638a07841acb9fde6207fdb8aef39118b24dcc076004311a2f5332cfffa76`  
		Last Modified: Wed, 24 Jun 2026 01:23:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3919e09fe346a48711d521c653887a2d70853b0e46cbc05aa591e8932793a220`  
		Last Modified: Wed, 24 Jun 2026 01:47:30 GMT  
		Size: 12.7 MB (12749701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef70284cff541245e3a875fa106eec027436659600c1bcb422920dccb629c48d`  
		Last Modified: Wed, 24 Jun 2026 01:47:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15abb190df9f6bd194bf9e0e9da9a119cf7586690c6f2f6574ad992c27dbab3`  
		Last Modified: Wed, 24 Jun 2026 01:47:30 GMT  
		Size: 11.8 MB (11773020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4261c9e62313bb7bf6900479d5f95ab1fa19d41c119af3c490f8baca98eb7093`  
		Last Modified: Wed, 24 Jun 2026 01:47:30 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b006e9a8f1ea5b9a8e8114a732d8267b25e8613aed700de594e1bbe4a1b95e4d`  
		Last Modified: Wed, 24 Jun 2026 01:47:31 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c385b4a35707e803b07baf009f4f434b6ceb23858a31c1e8386fbe604c99acf`  
		Last Modified: Wed, 24 Jun 2026 01:47:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05b71145b8aa43841f50cb4cf600561c8e9b6fb6e64656e338ed1be96c0ee96`  
		Last Modified: Wed, 24 Jun 2026 01:47:32 GMT  
		Size: 9.3 KB (9257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003d546480e90c81b5c26bc9ad967b6fe280ec5b798c79259bab27629e52e9e3`  
		Last Modified: Tue, 30 Jun 2026 19:07:35 GMT  
		Size: 1.3 MB (1284180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83061e020434db5e39e7b5fef36355e2f21a7be0136c21ddaa8c7c9c2255928e`  
		Last Modified: Tue, 30 Jun 2026 19:07:35 GMT  
		Size: 451.0 KB (451024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e92c612299a1cd017bbdefe564eea8f82bcb04ef053649bd788a4c0e5df0988`  
		Last Modified: Tue, 30 Jun 2026 19:07:35 GMT  
		Size: 2.6 MB (2603507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6fe0c88ee743620c20fc6a6cc9a949b93bb1e8c2df695a86996ab6d93fb757`  
		Last Modified: Tue, 30 Jun 2026 19:07:35 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e287811ecb493a4f18396eade3963fcc6a88386e34ee13c1e045beac9ec955a9`  
		Last Modified: Tue, 30 Jun 2026 19:07:36 GMT  
		Size: 823.3 KB (823345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71fa3d3f96a04750e46303fe71f0f8e552beac1ece80aa7a79d5e5d31e50967`  
		Last Modified: Tue, 30 Jun 2026 19:07:37 GMT  
		Size: 23.1 MB (23114085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:646ed733bf2a3d32d5daaa7331ff6246c26d975c652dab192826f8c985258521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 KB (39508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fe9a27605b1a2d0dc9930fcc10b032a7b1cdd5e84606cc0e3511983014d7806`

```dockerfile
```

-	Layers:
	-	`sha256:aa859f7eb9730d0f15f13bba5327862170fc931234b18028b91acc261d9735b9`  
		Last Modified: Tue, 30 Jun 2026 19:07:35 GMT  
		Size: 39.5 KB (39508 bytes)  
		MIME: application/vnd.in-toto+json
