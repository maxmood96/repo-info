## `php:8-zts-trixie`

```console
$ docker pull php@sha256:2885b57550b5c8abe25fe2e29421ec48e2cf953d0967a24bb8795040d32df556
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

### `php:8-zts-trixie` - linux; amd64

```console
$ docker pull php@sha256:199ea8c9f1e838b1abfbeeab1b3da67d713f4d56eb5d2128e5ceb1c28c5233f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189058673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea2a552716ce7077638566b59f3dae51f12ac7f7df8a787afae7f04f3bd9fb8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:23:32 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:23:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:23:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:23:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:23:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:23:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:23:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:23:48 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:23:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:23:48 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:23:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:23:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:26:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:26:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:26:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:26:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:26:23 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb347f6f73144503730fb7d2211ebed326a40f7df8e62326bc826f6dcf65616`  
		Last Modified: Mon, 16 Mar 2026 22:26:42 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2362742e4e165b0e078cdc4985420c70f3e4c8fc08350f9bdcdea810bf156c3f`  
		Last Modified: Mon, 16 Mar 2026 22:26:45 GMT  
		Size: 117.8 MB (117843477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3c4b84c05c1c14fe5a68ab154da108b54cc2e63794f42a98a9068f6889243a`  
		Last Modified: Mon, 16 Mar 2026 22:26:42 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3907e9b16c8daf307cea603e086a261d6326951c10ce36c39a6b9aae09c6d16f`  
		Last Modified: Mon, 16 Mar 2026 22:26:43 GMT  
		Size: 14.5 MB (14496688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5bf02fd74897190d71342e05bea621da9bb23602de1465dfc3c96c959d5251b`  
		Last Modified: Mon, 16 Mar 2026 22:26:43 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c398f297cdc8cf15a3412206e0d06e4a12357681ff73134ecee42672bcbb0d`  
		Last Modified: Mon, 16 Mar 2026 22:26:44 GMT  
		Size: 26.9 MB (26939380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a9adc43a715b377248a606c26f0ef50e9368b55ab18f2e67141c648e013ddb`  
		Last Modified: Mon, 16 Mar 2026 22:26:44 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c325de8030da5542ed0a566f73b71b83c7cc252bdaf84a0ecb778a2124873c`  
		Last Modified: Mon, 16 Mar 2026 22:26:44 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:8002d8b477254ef78956a699339e6a5a72f2f9bb619b5c43f3ca17269031661c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6724288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1129abb716058cfd83d09f73d016bd118b7259405eb43c290eab0d73f898bb04`

```dockerfile
```

-	Layers:
	-	`sha256:e4dd0da706cdcb3c65aa36fc4383bce5fa4ffac896df8eb2e49b4337b7407847`  
		Last Modified: Mon, 16 Mar 2026 22:26:42 GMT  
		Size: 6.7 MB (6683243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b335f5785dc67fae256d2f2cd89225c272040f3b0a339d939cace09bbd1b0b2`  
		Last Modified: Mon, 16 Mar 2026 22:26:42 GMT  
		Size: 41.0 KB (41045 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-trixie` - linux; arm variant v5

```console
$ docker pull php@sha256:ebd6b5915ef1439643f3be35365a5193d98edb7852f48197535bffbd92f0a2fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160735564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ef3f54516d6f4d5cdc8031899a1e5cc7ee346a667129a58ff0a5ed1851e986`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:22:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:22:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:22:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:22:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:22:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:22:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:22:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:22:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:22:01 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:22:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:22:01 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:22:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:22:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:25:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:25:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:25:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:25:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:25:30 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7b3f5f35f4c635055161c097c28e11cc3ae9984bb09405fe52ffad0e62c991`  
		Last Modified: Mon, 16 Mar 2026 22:25:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfb1492b794e0b40d1d9243fbd3885687b34b6dae58c105f6e6783a5eb01ca5`  
		Last Modified: Mon, 16 Mar 2026 22:25:51 GMT  
		Size: 94.9 MB (94884061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c50ed8ab3d9aeaecd328ae15919deabade9d5e8b55b5036f5833c27524072a1`  
		Last Modified: Mon, 16 Mar 2026 22:25:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d222e07547a3f924870ad909164977437e442a38afb0726eb97198ac2e552e0e`  
		Last Modified: Mon, 16 Mar 2026 22:25:49 GMT  
		Size: 14.5 MB (14494442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625d578fee3e57b4996a6aa3aaae7853ddfbb3cfaee2645fe2a63434bf6d3d6a`  
		Last Modified: Mon, 16 Mar 2026 22:25:50 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53cca2dde57bf6bf90cd5c939070447306d54e13467bb60053842654880ab33e`  
		Last Modified: Mon, 16 Mar 2026 22:25:51 GMT  
		Size: 23.4 MB (23409784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419550f57ba745155ab551820f09a23688d72634fc27f2f243c63129c2a6e461`  
		Last Modified: Mon, 16 Mar 2026 22:25:51 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b1c71a2b1ea85732d2f8bd9b76ab2443d6d36e4b9109ed3e2d0cb42cde9359`  
		Last Modified: Mon, 16 Mar 2026 22:25:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:1e07ba2c3d424d15e99f880197f59ebb37c1c8f61722c347a9c503509f094b3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6524304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dffb1659e0d47f98b49996a1b8b302dc1574fdc4a0a20ee317fcf6e28f3a9bf`

```dockerfile
```

-	Layers:
	-	`sha256:75b5943b3361654f05bd0f8a6e564da060dbec8c50dd36c05344dd5eaf68a49a`  
		Last Modified: Mon, 16 Mar 2026 22:25:49 GMT  
		Size: 6.5 MB (6483089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1579816b02cd646edb2ffc6cebf4619cd6d77ddf2f49fb31d96fe09b5a3f311d`  
		Last Modified: Mon, 16 Mar 2026 22:25:49 GMT  
		Size: 41.2 KB (41215 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-trixie` - linux; arm variant v7

```console
$ docker pull php@sha256:f11042658ba1f60a3cdaf2695ad1137cf0f8365562231031890800aa29f9d1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.0 MB (148960456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:865897336b91d73eabd337d48f548a9849e93209f97b392be2b02bea4bf38c13`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:23:37 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:23:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:23:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:23:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:23:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:23:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:23:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:23:55 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:23:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:23:55 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:24:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:24:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:30:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:30:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:30:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:30:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:30:20 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b1d5ec4866513f27eac3abc50f375ae947518e76aa41eb53c9bc3a19c59e63`  
		Last Modified: Mon, 16 Mar 2026 22:27:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174faaece6f968aa7b20a40f9aaac0c1f6fea792f301ed268770938de4f19fce`  
		Last Modified: Mon, 16 Mar 2026 22:27:22 GMT  
		Size: 86.2 MB (86246563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deab5f25d49b780786f07eecc25b3f5829d8370589bf08e782c3c7c7d99aad0f`  
		Last Modified: Mon, 16 Mar 2026 22:27:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83db00fd9c2963f46645479ff63bb802dfde74d986600904cdbed18e3bd25d3`  
		Last Modified: Mon, 16 Mar 2026 22:27:21 GMT  
		Size: 14.5 MB (14494563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff405d3024363d85cad2baa6d84ec7ea3cb9b514e31eb799c3154408d9197de`  
		Last Modified: Mon, 16 Mar 2026 22:27:21 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f309ccb3d34ce0c9b0c645e45b4d5ef5c603fd117acf7523eccac29583a427`  
		Last Modified: Mon, 16 Mar 2026 22:30:31 GMT  
		Size: 22.0 MB (22006197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d8937abc3f6689ffb6341a5ba649a81ce05724e72fe7188cf60bd1a5e87775`  
		Last Modified: Mon, 16 Mar 2026 22:30:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53518aeb67c0485531e075aae229e755e253fcc46d5f45b42133b04588085a5`  
		Last Modified: Mon, 16 Mar 2026 22:30:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:93cc1c8d455be6c974485e7385f5b1fd5d1f636c6b034889ad82727badb32a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6528269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b3ef36e00a100162e6abebe1762e2c430874114026a3fcf33b64ccf41e0314`

```dockerfile
```

-	Layers:
	-	`sha256:6bfab2f5fbe1f95a135f6aa5337037635da5921d218ed83e223e2f15832cc221`  
		Last Modified: Mon, 16 Mar 2026 22:30:31 GMT  
		Size: 6.5 MB (6487055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f19cc0adb5d00b15b9f520293a492252433769f240b55bc8a51ddc5dbb836d4`  
		Last Modified: Mon, 16 Mar 2026 22:30:30 GMT  
		Size: 41.2 KB (41214 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-trixie` - linux; arm64 variant v8

```console
$ docker pull php@sha256:1136fc15be387c4ab8807e4b2d52422230fd3a5c6e890e7d655640ce385dca34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.1 MB (181097090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280f3bcbfe7b4d9c0192c14d53659a44b3627f916f09329c00a88c7d3dc08a10`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:23:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:23:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:23:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:23:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:23:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:23:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:23:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:23:33 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:23:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:23:33 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:23:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:23:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:27:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:27:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:27:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:27:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:27:01 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a23ea2134be3c1bffb6ccf4040ff6b66d8592ea3ef13ef0fa75470ae99e0c1`  
		Last Modified: Mon, 16 Mar 2026 22:26:51 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb8a1bceabb45ea0dc2c409158e7d4bc5e4ffc9a1e1169a4aa24235d2ae959d`  
		Last Modified: Mon, 16 Mar 2026 22:27:24 GMT  
		Size: 110.2 MB (110164629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:282df8da3d20e3af62c4d9fda761614079c90dc5d748eeacf09bf95c60773caf`  
		Last Modified: Mon, 16 Mar 2026 22:26:52 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555c0e5c58485323eb4ccb976427667abe04e76d14c222ec82e8bc3eccd29090`  
		Last Modified: Mon, 16 Mar 2026 22:27:22 GMT  
		Size: 14.5 MB (14496274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4653e3cd4f44681f42dadbffaa77a99e935e4899a3e553500428b21fcbe79a6`  
		Last Modified: Mon, 16 Mar 2026 22:27:21 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ad2364b7bd35ffe0def3580f053a6b3d0d1e5632463b0a487b8cc06c3e2252`  
		Last Modified: Mon, 16 Mar 2026 22:27:23 GMT  
		Size: 26.3 MB (26294142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c3b937aa8ee0fe33eb397bbeb9520d9e2e3b3c27507a4c8d9a72cf59f45bfc`  
		Last Modified: Mon, 16 Mar 2026 22:27:22 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f95d9edb191f68fffe9a70ab95b90fb19a764c372d91424952035204698b9c3`  
		Last Modified: Mon, 16 Mar 2026 22:27:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:5ad69192e49075f308822cb16a87b9012a9f4d5b102ffa0fc197edf315a0b6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6821841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb0a10234e7bcb6b12eba82eca8718e9f66fc5618314d17f334022adf7031de`

```dockerfile
```

-	Layers:
	-	`sha256:a4f5c4229a39cbbb5e6d9307fa0e272de09adfc856321438c05041b79950a837`  
		Last Modified: Mon, 16 Mar 2026 22:27:21 GMT  
		Size: 6.8 MB (6780570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f727aac3f80846d922f3002c6693a5325ed7e704d5d0774827ebcfb40df323d4`  
		Last Modified: Mon, 16 Mar 2026 22:27:21 GMT  
		Size: 41.3 KB (41271 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-trixie` - linux; 386

```console
$ docker pull php@sha256:77be6a1cf5cc59ca1e06044e29cba525b739a93b124f47d5b1f81281c1c6d4be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.5 MB (189462785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae2ff969bf224790b27c70b9ff99138685154959fc4d788da94e533076be51d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:19:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:19:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:19:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:19:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:19:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:19:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:19:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:19:46 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:19:46 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:19:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:19:46 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:19:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:19:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:23:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:23:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:23:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:23:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:23:00 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d322b5a8ebd986a5fb4013a87b7d5daee85b6d8969d2803f2e0f64cb741fe44`  
		Last Modified: Mon, 16 Mar 2026 22:23:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186eac8df6dbf6b93265f2e04fb9a193eff19f9badc9a98de8b976ea3b508d0c`  
		Last Modified: Mon, 16 Mar 2026 22:23:23 GMT  
		Size: 116.1 MB (116144379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ed0ac2076d3ae3bca41924154bfb8da68f0ec93908ab976e16c2d162c295b`  
		Last Modified: Mon, 16 Mar 2026 22:23:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3264c3855015578c27e7a738999f0f9638420f0fc02208e1036e472dc6ef97c`  
		Last Modified: Mon, 16 Mar 2026 22:23:21 GMT  
		Size: 14.5 MB (14495769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e86830e6d9319c713429237ca66d2343e1fdd49a8c6f833911ab3a013954b31`  
		Last Modified: Mon, 16 Mar 2026 22:23:21 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0411c0a04e2ba603f56f6d7e5cd5f39e0e4aeb832939c71bfde72508f097a222`  
		Last Modified: Mon, 16 Mar 2026 22:23:22 GMT  
		Size: 27.5 MB (27527874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea75611644b0b8f49b70de6484873fe9dbe7446f11afa1a8259e28bdc0ebf67`  
		Last Modified: Mon, 16 Mar 2026 22:23:22 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ebaceb1f94880449937349a51c2746d042f6907f43f1dc6f3f16dc447cc54c`  
		Last Modified: Mon, 16 Mar 2026 22:23:22 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:162b199b4e92d7c533e321ac331bb6b8bba0141650b1c1c16e9458e26814dbfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6698102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d37e4a829ce3edad12076ea0ded9fb651d2de55258bd34ddf132f24fb35ed5`

```dockerfile
```

-	Layers:
	-	`sha256:c2e3407c22e42c57cb7cd0300601a146343fa62fcdaaa6193d9a764428550c32`  
		Last Modified: Mon, 16 Mar 2026 22:23:20 GMT  
		Size: 6.7 MB (6657121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c5ae10ef1a014c0e2772672619cd1b804a4679911ab480f1747fba287507cc`  
		Last Modified: Mon, 16 Mar 2026 22:23:20 GMT  
		Size: 41.0 KB (40981 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-trixie` - linux; ppc64le

```console
$ docker pull php@sha256:56429c82775c01439abe38bbb83b85af07ad1727dcc96fffca7899aaca0abc18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184766023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480d8854a632f1bea275df9af40f5f24d692b09cd93c66be3d2a2d68497334dc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Thu, 12 Mar 2026 23:28:30 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Mar 2026 23:29:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Mar 2026 23:29:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 12 Mar 2026 23:29:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:29:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:29:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:29:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:29:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:29:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:29:06 GMT
ENV PHP_VERSION=8.5.4
# Thu, 12 Mar 2026 23:29:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Thu, 12 Mar 2026 23:29:06 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Thu, 12 Mar 2026 23:29:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:29:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:40:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:40:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:40:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:40:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:40:12 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3775d5ddfc085666c347a617d5e829f26310c4192ca085c2d6858133f39bb6c`  
		Last Modified: Thu, 12 Mar 2026 23:34:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec48d97db5ea952f4576b2f9d01739464e680954cd8131033b1130e99184b70`  
		Last Modified: Thu, 12 Mar 2026 23:34:53 GMT  
		Size: 109.6 MB (109598721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22b0b943276144e2999641cbe60a6b81da9ba29447be9c399b166708aed41be`  
		Last Modified: Thu, 12 Mar 2026 23:34:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9984969e26f58b142decd4b27c4240d1fe4c7cf984d0c98f0e430ba20743d98`  
		Last Modified: Thu, 12 Mar 2026 23:34:50 GMT  
		Size: 14.5 MB (14495851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333005a6ea67ea08319cc70784daf6086675cdf8ed0a1c87e1f8ea318340dfa6`  
		Last Modified: Thu, 12 Mar 2026 23:34:50 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f19d701c23488be33405add353e626e8c89571d00fa8190bb2f700765ce24e0`  
		Last Modified: Thu, 12 Mar 2026 23:40:37 GMT  
		Size: 27.1 MB (27067590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c8e2a6487cab88417048b5c1b623854c02a44754860ea552b8ae3ab0fc53dd`  
		Last Modified: Thu, 12 Mar 2026 23:40:36 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e0f2afdc6bfa96c9a9abf0e8b86ba81f59e636240ef2b0854fef55c3749290`  
		Last Modified: Thu, 12 Mar 2026 23:40:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:10a06b2a1d719214d1ae53e41002d8677a2b24863f952d951f74aeef73a100f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6723047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870e541c179cf4295691387b8d989494550131d9ba35b4b5c283c5a65753b4e3`

```dockerfile
```

-	Layers:
	-	`sha256:90bd208c9bb8f49c0b143b9b68dd8c07ec57e3c8486db000a9ed3cbfada0a46e`  
		Last Modified: Thu, 12 Mar 2026 23:40:36 GMT  
		Size: 6.7 MB (6682879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7476a8380d5d80b27b1da0b72928806dc913e3fe7ef131bc2bc87cf62b0969f4`  
		Last Modified: Thu, 12 Mar 2026 23:40:36 GMT  
		Size: 40.2 KB (40168 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-trixie` - linux; riscv64

```console
$ docker pull php@sha256:63218ec92f009dd4d2e0da6c3f09b75d2aec4fbda6b2a4535c40e04058e7bcf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.4 MB (214358917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646341cba0e49dd85488c7c79dcff0a52d99a1a7cdbcedeb736c04fb77df9d3d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 08:37:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 25 Feb 2026 08:39:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 25 Feb 2026 08:39:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 25 Feb 2026 08:39:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 Feb 2026 08:39:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 25 Feb 2026 08:39:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Feb 2026 08:39:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 Feb 2026 08:39:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 Feb 2026 08:39:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 25 Feb 2026 08:39:18 GMT
ENV PHP_VERSION=8.5.4
# Wed, 25 Feb 2026 08:39:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Wed, 25 Feb 2026 08:39:18 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Thu, 12 Mar 2026 23:54:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:54:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 03:55:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Mar 2026 03:55:16 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 03:55:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Mar 2026 03:55:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Mar 2026 03:55:17 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae6df9269bfd4174a44849bb7987f7a59ec3c5430213257f79ad656b80f4e2d`  
		Last Modified: Wed, 25 Feb 2026 09:42:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e38127a1d5098bc45d1ab51573d3cb4b81e383d9777a8e0449378000b440c3dc`  
		Last Modified: Wed, 25 Feb 2026 09:43:30 GMT  
		Size: 146.6 MB (146584285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a1ad2ba1292d9c3abe04163ae27f6acc0fa6ab45f94cf6f5f5eebe7c6a93122`  
		Last Modified: Wed, 25 Feb 2026 09:42:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59311cb395266713e7adea71f15b6f1baa5b1e9fcc54fc3261067e445ea69df`  
		Last Modified: Fri, 13 Mar 2026 00:54:42 GMT  
		Size: 14.5 MB (14511137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31268b754d1270fa9874a007a5ba8a822a705442121dce0f5f373c83d40b5c2`  
		Last Modified: Fri, 13 Mar 2026 00:54:37 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:399b7d52c5167837539c9da273b95e47fe8a5d4e79cd8417101c0129b5bfcced`  
		Last Modified: Fri, 13 Mar 2026 03:58:40 GMT  
		Size: 25.0 MB (24983433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02e9bb8432030a26219153b7e2ee946f76666576d8866745207eadb3ffcb0cd`  
		Last Modified: Fri, 13 Mar 2026 03:58:35 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a48b4b9884b396c65bdfa29a2805b28fa025fc1ce918f07359d1f6de8db0032`  
		Last Modified: Fri, 13 Mar 2026 03:58:35 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:bebd5babfde71636b5923074c5bcdf17e600b63af783e0a946f3831d36f4fe0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6796091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100c1c2138f50d9c29ed76beee838020927a591b1139d5856dbdf968baf074b1`

```dockerfile
```

-	Layers:
	-	`sha256:b756f766844dddb3a0b0baa3adb83e06dfdea15f4211ede4a2d252dc9de740c7`  
		Last Modified: Fri, 13 Mar 2026 03:58:36 GMT  
		Size: 6.8 MB (6754968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fff0305de6d0489c0b75fad2cfb7b64e0e7c1ba4d59ecb2a64bdb9198dde5c8c`  
		Last Modified: Fri, 13 Mar 2026 03:58:35 GMT  
		Size: 41.1 KB (41123 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-zts-trixie` - linux; s390x

```console
$ docker pull php@sha256:f7dbc80197cb4ba5ff5a6eef037a586d79ec9065798d51bcfa00739ced70976a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162669516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7720ea2991f89da68606b444072786ab6f0dc4ab8e906ba6567e388fe129c558`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 16 Mar 2026 22:21:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 16 Mar 2026 22:21:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 16 Mar 2026 22:21:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Mar 2026 22:21:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Mar 2026 22:21:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:21:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Mar 2026 22:21:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Mar 2026 22:21:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Mon, 16 Mar 2026 22:21:22 GMT
ENV PHP_VERSION=8.5.4
# Mon, 16 Mar 2026 22:21:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.4.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.4.tar.xz.asc
# Mon, 16 Mar 2026 22:21:22 GMT
ENV PHP_SHA256=c1569f1f543f6b025c583cdc0e730e5c5833c603618613f1aa8e75d1524b8c91
# Mon, 16 Mar 2026 22:26:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 16 Mar 2026 22:26:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:29:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--enable-embed 				--enable-zts 		--disable-zend-signals 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Mar 2026 22:29:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Mar 2026 22:29:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Mar 2026 22:29:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Mar 2026 22:29:42 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d682313c93d842a502f0533c210c3b2caaa363a69eb85e77dce91f657ce62452`  
		Last Modified: Mon, 16 Mar 2026 22:25:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba782a5efcb081606644cebd64910d2d841abde0bc755a0767f1b2a2c85fe97`  
		Last Modified: Mon, 16 Mar 2026 22:25:39 GMT  
		Size: 92.6 MB (92572766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbf0aec76462c7cbcced8ce549ff5e309ef36712ece21fefa2a9107b22ea5ea`  
		Last Modified: Mon, 16 Mar 2026 22:25:37 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82534940e40f62925478e1e6c162120c7c51d28779756d1ae17a9455ae49d21e`  
		Last Modified: Mon, 16 Mar 2026 22:30:03 GMT  
		Size: 14.5 MB (14495202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223bdfaadfc0d87e4a4403991ba818b72a0f4a0afbc4e8a1c447472149abcaf9`  
		Last Modified: Mon, 16 Mar 2026 22:30:03 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f86bc39f56dde8f7e72e86e8161014d8f2f2120933200d37515046b8c82cfe`  
		Last Modified: Mon, 16 Mar 2026 22:30:04 GMT  
		Size: 25.8 MB (25762653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1c5f5b9f54f5a378cae7c97e9e3d373588fd339e6b1f855e9e3d0b51617839`  
		Last Modified: Mon, 16 Mar 2026 22:30:03 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc588a3d18e05487e61a305062cf84e77e01d54ebe24407b8dde572a5c155b42`  
		Last Modified: Mon, 16 Mar 2026 22:30:04 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-zts-trixie` - unknown; unknown

```console
$ docker pull php@sha256:e1032c33245a55346af99bb178a335cddabfd88f628d7d34f8e11ba99dbc565d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6541554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6562b3f8b3992b9e7a7448b0af06bf907cb686cf18cfc4e06dd3cd158256e01`

```dockerfile
```

-	Layers:
	-	`sha256:ef27f13abbda17c70c1e492da2b754bebb35966a6a1231b90ca158bc48302d6b`  
		Last Modified: Mon, 16 Mar 2026 22:30:03 GMT  
		Size: 6.5 MB (6500516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5053aeee108d9f90657b8939ce791010b2a4e6132f3331c757ce0c7e12953393`  
		Last Modified: Mon, 16 Mar 2026 22:30:03 GMT  
		Size: 41.0 KB (41038 bytes)  
		MIME: application/vnd.in-toto+json
