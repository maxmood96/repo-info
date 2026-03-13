## `matomo:5-fpm`

```console
$ docker pull matomo@sha256:b76f3072277459d4e275f91922d4bc282515bb540337c276987c31275c497c8a
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

### `matomo:5-fpm` - linux; amd64

```console
$ docker pull matomo@sha256:2ffa231aa3349330a1b08fc2a8e206aaa2f5aaea0314e7ec249135b55f5035f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.2 MB (200217422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d279decb1161200f8b93ec3a49374572559cf03235be350d02913e01387e8bd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Thu, 12 Mar 2026 23:28:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Mar 2026 23:28:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Mar 2026 23:28:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 12 Mar 2026 23:28:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:28:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:28:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:28:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:28:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:28:52 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:28:52 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:28:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:28:52 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Thu, 12 Mar 2026 23:32:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:32:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:34:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:34:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:34:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 12 Mar 2026 23:34:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:34:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:34:54 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:34:54 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 12 Mar 2026 23:34:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Mar 2026 23:34:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 12 Mar 2026 23:34:54 GMT
CMD ["php-fpm"]
# Fri, 13 Mar 2026 00:16:06 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 13 Mar 2026 00:16:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 13 Mar 2026 00:16:06 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Mar 2026 00:16:06 GMT
ENV MATOMO_VERSION=5.8.0
# Fri, 13 Mar 2026 00:16:16 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Fri, 13 Mar 2026 00:16:16 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 13 Mar 2026 00:16:17 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Mar 2026 00:16:17 GMT
VOLUME [/var/www/html]
# Fri, 13 Mar 2026 00:16:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Mar 2026 00:16:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcaa8c5e39112f540def008b891480c0c23e24dec2b07c73a4d8d2e4ea983d59`  
		Last Modified: Thu, 12 Mar 2026 23:32:04 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3332389b42697751c122bf7378753387d8e3e3a5870000ca83fa7d467616651e`  
		Last Modified: Thu, 12 Mar 2026 23:32:08 GMT  
		Size: 117.8 MB (117842531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542b76cae2c17c1c54bed66d9414aaea912ca3762ef11d99fc188781f5295212`  
		Last Modified: Thu, 12 Mar 2026 23:32:04 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf6ec10d3a7ae678817e083c958a0c367adfa4348d85669675c3dd9ed2ccd92`  
		Last Modified: Thu, 12 Mar 2026 23:35:05 GMT  
		Size: 13.8 MB (13832327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ee20c15dae3a54891e913e974f6625ef00554e97d5d0c6a4ffee46fdec92a7`  
		Last Modified: Thu, 12 Mar 2026 23:35:04 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5914eb919e67e13a2fac6130de45a7fc59627af6922d71e100eb77790b9d861c`  
		Last Modified: Thu, 12 Mar 2026 23:35:05 GMT  
		Size: 13.7 MB (13686166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dd21b3e9b562ae154203cc9636cbf0a28cb161735a8bb5e73c76eb4248262b`  
		Last Modified: Thu, 12 Mar 2026 23:35:04 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34cbd97e8a4939194c2d22a02eb59c16b0836c1d3f5aa93dc0b1e3cf5d2704a`  
		Last Modified: Thu, 12 Mar 2026 23:35:05 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39573b64c1ab5f5555694a83cfbed24c7964b2af5d09ba2fc0e60a956b1ba183`  
		Last Modified: Thu, 12 Mar 2026 23:35:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e3f1e923b8c3cf95f3f36eeb410beed4bf14fbef401f97efeb400257858df3`  
		Last Modified: Thu, 12 Mar 2026 23:35:06 GMT  
		Size: 9.3 KB (9271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa968a97ed9039c2bb6c97c958285dc8f22a37025a2bb791b8d87ee89c465b99`  
		Last Modified: Fri, 13 Mar 2026 00:16:24 GMT  
		Size: 2.7 MB (2686199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d82712139a4b3755da46bef5b60e12a63e596280f2212c9adda5d290b21674d4`  
		Last Modified: Fri, 13 Mar 2026 00:16:24 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17af97b6d237354d282e8778023927d708f0211ba7b6a97f2f5a0a8a2a90b8dd`  
		Last Modified: Fri, 13 Mar 2026 00:16:24 GMT  
		Size: 22.4 MB (22376874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1aef92c25c0edd1033b942dbe39ef9e68c5d5d90fce148e34c72578a2f7efb`  
		Last Modified: Fri, 13 Mar 2026 00:16:23 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc2e6b4e5bcffee4d5196245c8fe83ffad2e64bb48f26f981fab0d213aa2f28`  
		Last Modified: Fri, 13 Mar 2026 00:16:25 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:1cc38c24646321791e25db0973bc3701afa432551a81b8c1691214d86ae4da4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad9e16285c32cb310e5541e5a2d4fbe99e98a5fa2f5819979604baa38f2e2a5`

```dockerfile
```

-	Layers:
	-	`sha256:80880968fc901406d1969a1e6a5584158d70b81c72521b55b59582c30edd8c74`  
		Last Modified: Fri, 13 Mar 2026 00:16:23 GMT  
		Size: 33.2 KB (33248 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; arm variant v5

```console
$ docker pull matomo@sha256:b2784e1f776e4b2f60bd5e2b07f9646d699ee33bf28a66b22bd53dfb6806b209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.8 MB (173799531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204c9a98bd906c55c452875174a82e1274d4208dca7682cbc91619f45d5576ad`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Thu, 12 Mar 2026 23:44:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Mar 2026 23:44:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Mar 2026 23:44:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 12 Mar 2026 23:44:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:44:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:44:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:44:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:44:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:44:42 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:44:42 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:44:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:44:42 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Thu, 12 Mar 2026 23:44:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:44:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:47:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:47:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:47:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 12 Mar 2026 23:47:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:47:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:47:53 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:47:53 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 12 Mar 2026 23:47:53 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Mar 2026 23:47:53 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 12 Mar 2026 23:47:53 GMT
CMD ["php-fpm"]
# Fri, 13 Mar 2026 00:25:43 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 13 Mar 2026 00:25:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 13 Mar 2026 00:25:43 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Mar 2026 00:25:43 GMT
ENV MATOMO_VERSION=5.8.0
# Fri, 13 Mar 2026 00:26:00 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Fri, 13 Mar 2026 00:26:00 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 13 Mar 2026 00:26:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Mar 2026 00:26:00 GMT
VOLUME [/var/www/html]
# Fri, 13 Mar 2026 00:26:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Mar 2026 00:26:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:627c2b53d9179c1da1e4d228f8c88d9735459f81d38344e0dc68d11c726aaa77`  
		Last Modified: Thu, 12 Mar 2026 23:48:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afb0f02dc9ce063aa93d2529d93a8a2ce0245570cffd98b512c4ed7d4b982b4`  
		Last Modified: Thu, 12 Mar 2026 23:48:13 GMT  
		Size: 94.9 MB (94884017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cdf035a81b004be321b7ae40f049f28a6dfff709c9934e446366e88bb9ffc1`  
		Last Modified: Thu, 12 Mar 2026 23:48:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae54db72e10fb31ed52861ada6bd4fab3f4ab847d3a92724181d4fe64bd40e`  
		Last Modified: Thu, 12 Mar 2026 23:48:11 GMT  
		Size: 13.8 MB (13829709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87465f1368922e43221b82272329b41c9feee97bc457ed20bd64a03b8eab48b`  
		Last Modified: Thu, 12 Mar 2026 23:48:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7760850080e5f73caf3957ec827b19c6d29c0ec30a63154a457fb02c8d367e5`  
		Last Modified: Thu, 12 Mar 2026 23:48:12 GMT  
		Size: 12.2 MB (12238470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eea27590f0442d077eaf747b32e49fa2de14d5fe375c7765d4fc80bca9e7118`  
		Last Modified: Thu, 12 Mar 2026 23:48:13 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bd517e0bc349234c3a188c727338ced4e1689bb9af016924ce72fc1d17d597`  
		Last Modified: Thu, 12 Mar 2026 23:48:13 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a815099f8d82355318becb5c45dcd07ffb6b8d01e6088de2aaf1853b161485b`  
		Last Modified: Thu, 12 Mar 2026 23:48:14 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdac4774fa0f55ffc1faf6d6233c59954397b69a40f7e571d288b95f7994e28`  
		Last Modified: Thu, 12 Mar 2026 23:48:14 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127b064d6a3a96a09a2d60ca65c8429ec6c9aec093066618c6f9bf44b4e1cbf`  
		Last Modified: Fri, 13 Mar 2026 00:26:07 GMT  
		Size: 2.5 MB (2510180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393fc4eb75743faecddcb4648e0dcd00fe5babd3d00016c810d1bab7f8886d36`  
		Last Modified: Fri, 13 Mar 2026 00:26:07 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00c301dffd52eea3053e74486d56f30a24328c7c19cfb0a86a9dc0c293eea2f8`  
		Last Modified: Fri, 13 Mar 2026 00:26:08 GMT  
		Size: 22.4 MB (22374861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398792623e1952bb2d23775886265ab6543c64b58f381653280b85a256875883`  
		Last Modified: Fri, 13 Mar 2026 00:26:07 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3245d02a10544b6ca5aacfe21dcc6d5b853bbe8eeca65e65b5803954ba0e4c3b`  
		Last Modified: Fri, 13 Mar 2026 00:26:08 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:0c9c304f9bfd6f1d78928837694c3fbecbce805ffb274ab52a8d96a4703c287f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a72511123846f6d9ad1c32755d2f8f16a449bbe56a152cf8907a9b92a351eb`

```dockerfile
```

-	Layers:
	-	`sha256:f470a3023782a218626123fb3031de00b2cb44874a981441b44583dae376fecc`  
		Last Modified: Fri, 13 Mar 2026 00:26:07 GMT  
		Size: 33.3 KB (33348 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; arm variant v7

```console
$ docker pull matomo@sha256:f5366dab520dc754bbb312772f97dad679daac4f83a3991e613ce3ac586d70d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162643119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96eccd8579f78274603ae671e6369a65144a3e3620d4c47346341d7216f34d8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Thu, 12 Mar 2026 23:32:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Mar 2026 23:32:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Mar 2026 23:32:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 12 Mar 2026 23:32:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:32:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:32:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:32:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:32:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:32:33 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:32:33 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:32:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:32:33 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Thu, 12 Mar 2026 23:39:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:39:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:42:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:42:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:42:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 12 Mar 2026 23:42:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:42:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:42:31 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:42:32 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 12 Mar 2026 23:42:32 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Mar 2026 23:42:32 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 12 Mar 2026 23:42:32 GMT
CMD ["php-fpm"]
# Fri, 13 Mar 2026 00:27:02 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 13 Mar 2026 00:27:02 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 13 Mar 2026 00:27:02 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Mar 2026 00:27:02 GMT
ENV MATOMO_VERSION=5.8.0
# Fri, 13 Mar 2026 00:27:18 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Fri, 13 Mar 2026 00:27:18 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 13 Mar 2026 00:27:18 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Mar 2026 00:27:18 GMT
VOLUME [/var/www/html]
# Fri, 13 Mar 2026 00:27:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Mar 2026 00:27:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9438e4f0dafffd7df091a30af4ee07d90904ffa98416f296e13ce940c77750`  
		Last Modified: Thu, 12 Mar 2026 23:35:51 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b03bb4285232e22f74d37592fb326192afea629b99e925199768f156ddf6d`  
		Last Modified: Thu, 12 Mar 2026 23:35:53 GMT  
		Size: 86.2 MB (86245692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01b0c6dc4365edda617dc2b87155d1d02005c49b94441f12920db0aded43ae93`  
		Last Modified: Thu, 12 Mar 2026 23:35:51 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081afa73f33aa4012eb4e7a1e2cbcee2c3aa4d797c27d75b2c206eea1ec4860a`  
		Last Modified: Thu, 12 Mar 2026 23:42:42 GMT  
		Size: 13.8 MB (13829836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9ee7cdc7f4c6472474973bd4974e84c7c9d80494fed01a1ee60c2f87a4e820`  
		Last Modified: Thu, 12 Mar 2026 23:42:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5e9a53fa95aa97e5c4eb9548da48b8a6220f70f11e8fe00e98bd486d45e2fe`  
		Last Modified: Thu, 12 Mar 2026 23:42:42 GMT  
		Size: 11.6 MB (11571633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46450cbc1d9cacead89a7dac671ff3835cd5609887ce0b39fe6c7c4b52fa4c6`  
		Last Modified: Thu, 12 Mar 2026 23:42:41 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbb6b9975c11ae7cf3583968c0b26aa3e97b1cd11e86249cfd8d98361d65106`  
		Last Modified: Thu, 12 Mar 2026 23:42:42 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39cc7cd747f31a16f84dd75c91689d8ecee162043060e78e0e3500e0977963d5`  
		Last Modified: Thu, 12 Mar 2026 23:42:42 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fb2a3fe3f457a96a15c3738c603fe074e6cabe3a17b1d3928eaa16b37a2e5b`  
		Last Modified: Thu, 12 Mar 2026 23:42:43 GMT  
		Size: 9.3 KB (9271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb0aba3803b6abcd758473eea7b7db48283d5a43f5730404c74f03f3d5e58ac`  
		Last Modified: Fri, 13 Mar 2026 00:27:25 GMT  
		Size: 2.4 MB (2392599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5592d1bf16ce2f75df2f9f7e2c4d42dfc47235c6ab6ff4065722d7d20e824bb6`  
		Last Modified: Fri, 13 Mar 2026 00:27:24 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988cd1e4984dc5166216a6445aff39c363274198d8f0298d7af6a0abf1e27513`  
		Last Modified: Fri, 13 Mar 2026 00:27:25 GMT  
		Size: 22.4 MB (22374916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c39c51e6dc3cb1cfeeb788ce3a0e17151c41049bc7f9fff43b86b30346c181c3`  
		Last Modified: Fri, 13 Mar 2026 00:27:25 GMT  
		Size: 345.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a6a9b38ab4abfb99885358dfa681bc8a87ca3da20c02d8689dc1febc19b7fa`  
		Last Modified: Fri, 13 Mar 2026 00:27:26 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:4457369902d5e748a2c8008ab182fc29ed388b4c862728ce5edebc6623e00b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b00e51528a54a2c27056ac299a52cbc5b701ba51b29f65fe64f2f1de48f60fd`

```dockerfile
```

-	Layers:
	-	`sha256:179ffa12438a76b05dd1bc60e35e72661d83ec907ccc9121a8a9cf77285dd72a`  
		Last Modified: Fri, 13 Mar 2026 00:27:24 GMT  
		Size: 33.3 KB (33348 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:6177bbdcdfb3f1fa7da90fc4fad7533aa8f9319ea26b62f6b6d837b5c4e6be77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192536912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ceded4d0c0f5f4188410bca03235787443af1069b2fa52cccf969c1ddcfbe9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Thu, 12 Mar 2026 23:35:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Mar 2026 23:35:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Mar 2026 23:35:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 12 Mar 2026 23:35:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:35:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:35:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:35:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:35:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:35:46 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:35:46 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:35:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:35:46 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Thu, 12 Mar 2026 23:35:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:35:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:39:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:39:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:39:02 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 12 Mar 2026 23:39:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:39:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:39:02 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:39:02 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 12 Mar 2026 23:39:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Mar 2026 23:39:02 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 12 Mar 2026 23:39:02 GMT
CMD ["php-fpm"]
# Fri, 13 Mar 2026 00:16:35 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 13 Mar 2026 00:16:35 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 13 Mar 2026 00:16:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Mar 2026 00:16:35 GMT
ENV MATOMO_VERSION=5.8.0
# Fri, 13 Mar 2026 00:16:45 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Fri, 13 Mar 2026 00:16:45 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 13 Mar 2026 00:16:45 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Mar 2026 00:16:45 GMT
VOLUME [/var/www/html]
# Fri, 13 Mar 2026 00:16:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Mar 2026 00:16:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0cfbeb07544e0dbed82da9e9aa1ae927130439ac2f956a0153cfeb58121101`  
		Last Modified: Thu, 12 Mar 2026 23:39:24 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974a05c686c10805f20832c32100064d2a692dc497e938198d6aad9d2e5298b0`  
		Last Modified: Thu, 12 Mar 2026 23:39:27 GMT  
		Size: 110.2 MB (110163174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:847a27db851e3c37c1767442a0ec773bc285137293730be1f961386424c57f14`  
		Last Modified: Thu, 12 Mar 2026 23:39:23 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8f272f0a1f5cb787f6273eb21687e138984565a090f2ae17412ca690e973c8`  
		Last Modified: Thu, 12 Mar 2026 23:39:24 GMT  
		Size: 13.8 MB (13831844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d46c1e92134b472021fb2303f82a22abdbd7e11247205302cf85a71aa97e9b6d`  
		Last Modified: Thu, 12 Mar 2026 23:39:25 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210de84558b82ca62b782d70ed720fafebfbd02dd75cf27b77489b9b59746f8d`  
		Last Modified: Thu, 12 Mar 2026 23:39:25 GMT  
		Size: 13.3 MB (13343442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8f40209f8646dfb0b8042cca6d65bd48440146ebc288e49c0416c019d48183`  
		Last Modified: Thu, 12 Mar 2026 23:39:26 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07f1eef67931cea4b16bf52536c1c3922d1b243cedf7a7c2b5fb50e9680ccf3`  
		Last Modified: Thu, 12 Mar 2026 23:39:27 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef6913cf1ca386439f3c7573d35b78adf1108f7e3e5fe94a82bc2a0a0b99c350`  
		Last Modified: Thu, 12 Mar 2026 23:39:27 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:536b928e3319e745e5477070239db841af33eb818acff89c9cbec46e44e563e0`  
		Last Modified: Thu, 12 Mar 2026 23:39:27 GMT  
		Size: 9.3 KB (9272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239f2e459f0496d6e92a828051308b852e2216712608018b6c2f15e3750d86ab`  
		Last Modified: Fri, 13 Mar 2026 00:16:52 GMT  
		Size: 2.7 MB (2667167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c640733477bfd81c8e5beb257ec78821ec9485ef2b7192ec2651934808af035c`  
		Last Modified: Fri, 13 Mar 2026 00:16:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fc93148eaaf643b1fe6d76dd62dff01ebdea2711c02c5de2305f4da2072739`  
		Last Modified: Fri, 13 Mar 2026 00:16:53 GMT  
		Size: 22.4 MB (22376492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5002bb5cf6eacf5d57a376fe5ec314f7e87029e39070e726b41c2018a7cc93df`  
		Last Modified: Fri, 13 Mar 2026 00:16:52 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81462ae691bbef97523091db4803b21c34d54a27217feca1ee831e8fc97db58`  
		Last Modified: Fri, 13 Mar 2026 00:16:53 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:7892ca34f5d209daf1bf8141860f520f041c378fda3a3869712ffbbb4865e60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 KB (33382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2dc4c65cd0a9e077f1e6998e096be6900fb43aa2074d2aa2eb0b33b2ba2edd`

```dockerfile
```

-	Layers:
	-	`sha256:806534db2f2a0a858f9c2fb7ce8030ae8ab0e7886262a4152ccfbd5070d05038`  
		Last Modified: Fri, 13 Mar 2026 00:16:52 GMT  
		Size: 33.4 KB (33382 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; 386

```console
$ docker pull matomo@sha256:550be95a5927fad21545d8f828fb8d19ead6cefa9ccdcfa5943e955438aa5f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.3 MB (200303941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20fc3b415006700040c84e3bc17e8a2698c12e246562cc434d5c499f9978eff7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Thu, 12 Mar 2026 23:40:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Mar 2026 23:41:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Mar 2026 23:41:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 12 Mar 2026 23:41:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:41:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:41:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:41:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:41:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:41:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:41:12 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:41:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:41:12 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Thu, 12 Mar 2026 23:41:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:41:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:44:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:44:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:44:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 12 Mar 2026 23:44:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:44:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:44:14 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:44:14 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 12 Mar 2026 23:44:14 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Mar 2026 23:44:14 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 12 Mar 2026 23:44:14 GMT
CMD ["php-fpm"]
# Fri, 13 Mar 2026 00:16:34 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 13 Mar 2026 00:16:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 13 Mar 2026 00:16:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Mar 2026 00:16:35 GMT
ENV MATOMO_VERSION=5.8.0
# Fri, 13 Mar 2026 00:16:46 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Fri, 13 Mar 2026 00:16:46 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 13 Mar 2026 00:16:46 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Mar 2026 00:16:46 GMT
VOLUME [/var/www/html]
# Fri, 13 Mar 2026 00:16:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Mar 2026 00:16:46 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a48052a0f706f79ced7f9a3ea5390cf9a040ba35c69e9c52f740dbb4a5386bd`  
		Last Modified: Thu, 12 Mar 2026 23:44:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937a9c39a33ffc4ba8d63add184b6db555b88f67d95b9b042c87a911da8c82ea`  
		Last Modified: Thu, 12 Mar 2026 23:44:37 GMT  
		Size: 116.1 MB (116145161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8482ffcede573568fe16130681f316434651bc1763398c2b45f9cd0aa2b72c7b`  
		Last Modified: Thu, 12 Mar 2026 23:44:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae957216bdbfe26f5229d12dc02a75dfdf5a790e7dba47403d8e7966d10d91c0`  
		Last Modified: Thu, 12 Mar 2026 23:44:35 GMT  
		Size: 13.8 MB (13831155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684950dcd4c0ec420acc76884d7eed017c9ff8e14bd4a082b240035658479ed4`  
		Last Modified: Thu, 12 Mar 2026 23:44:35 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060a6a9ee48fb73566d39b04e281f2d6b0434946c96ea3f0e725c88259ef1dbb`  
		Last Modified: Thu, 12 Mar 2026 23:44:35 GMT  
		Size: 14.0 MB (13980443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f294d83d770155df9abf51ef521b39e4011eb9ad31684606b6dd7c041c1c38ba`  
		Last Modified: Thu, 12 Mar 2026 23:44:36 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6da530d618366a7561901d0b32d6f116b672005b967c60196c77cb3a23d316c`  
		Last Modified: Thu, 12 Mar 2026 23:44:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddec01c26b30abe4c76a480fbbed80f2aed6b34d0b38c5e53c44d3afe58ebe8`  
		Last Modified: Thu, 12 Mar 2026 23:44:37 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdf646f3025e34362f6d23bf6549578ec8ff86d25e4a0c5420db3be84560695`  
		Last Modified: Thu, 12 Mar 2026 23:44:37 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2dfa35eebe8ca2b6815870e03aae84a976befa49e0a9fad444da10377622a64`  
		Last Modified: Fri, 13 Mar 2026 00:16:53 GMT  
		Size: 2.7 MB (2662507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9496392be6dbd792417f84782147e0235aebc75c055bfbce1e7d01754ab59fed`  
		Last Modified: Fri, 13 Mar 2026 00:16:53 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ceec42fd984d6d23620e94d3b8e6dfdfe03bab3e51aba8489b422bc1be8cb7`  
		Last Modified: Fri, 13 Mar 2026 00:16:54 GMT  
		Size: 22.4 MB (22376071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75db4b9a4a9627508b4b10e7fe534020f3e29174a7ef67261082967f477d6a63`  
		Last Modified: Fri, 13 Mar 2026 00:16:53 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ed30d157169ca224bae2aedf5dc970174a65585770be354d880e71a53fdbfe`  
		Last Modified: Fri, 13 Mar 2026 00:16:54 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:1348bee15ecef1d4ee552d0920c63bd28421a2eb96288322aa53af05925b2dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70539ed30cf0e17fb7ee8cf416e0d31bbd4f53854acc25749edc80e1b1f5f6be`

```dockerfile
```

-	Layers:
	-	`sha256:cc8495d35ee5208cdf5abc5c1caa7f70e461f8e49033835ea927c51a6eb8da13`  
		Last Modified: Fri, 13 Mar 2026 00:16:53 GMT  
		Size: 33.2 KB (33212 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; ppc64le

```console
$ docker pull matomo@sha256:df1201ef39b98edac885be7e28d7d69aef4d40973746b11881c02071cc7e7675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.6 MB (196574428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97c8aa0a671e6cc5cdbdea65d33120d262fb5c58bcc809e8a044cd7757e98f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:32:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 24 Feb 2026 19:33:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 24 Feb 2026 19:33:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 24 Feb 2026 19:33:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 24 Feb 2026 19:33:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 24 Feb 2026 19:33:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:33:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 24 Feb 2026 19:33:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 24 Feb 2026 19:33:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 24 Feb 2026 19:33:28 GMT
ENV PHP_VERSION=8.4.18
# Tue, 24 Feb 2026 19:33:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Tue, 24 Feb 2026 19:33:28 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Tue, 24 Feb 2026 19:58:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 24 Feb 2026 19:58:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:07:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 24 Feb 2026 20:07:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 24 Feb 2026 20:07:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 24 Feb 2026 20:07:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 24 Feb 2026 20:07:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 24 Feb 2026 20:07:32 GMT
WORKDIR /var/www/html
# Tue, 24 Feb 2026 20:07:33 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 24 Feb 2026 20:07:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 20:07:33 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 24 Feb 2026 20:07:33 GMT
CMD ["php-fpm"]
# Thu, 05 Mar 2026 00:22:09 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 05 Mar 2026 00:22:09 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Thu, 05 Mar 2026 00:22:10 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 05 Mar 2026 00:22:10 GMT
ENV MATOMO_VERSION=5.8.0
# Thu, 05 Mar 2026 00:22:46 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Thu, 05 Mar 2026 00:22:52 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 05 Mar 2026 00:22:52 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Mar 2026 00:22:52 GMT
VOLUME [/var/www/html]
# Thu, 05 Mar 2026 00:22:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 00:22:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7690cd9f98d511ab47bad6b0f57131948908338ab7adc991d55c865326cac8`  
		Last Modified: Tue, 24 Feb 2026 19:39:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae9f58f13e9d918afe833361b4c7d9fe0b3caf579a1a946767b97fa1d9806bd`  
		Last Modified: Tue, 24 Feb 2026 19:39:22 GMT  
		Size: 109.6 MB (109598488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71f0a668b3964403df849cfd4e69c59e0bab46a4a7ab6507b543c932233ac99`  
		Last Modified: Tue, 24 Feb 2026 19:39:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b155f83b23fc1ecaf48986140b0d916c3272df28ded490eff6a543ef173e9c62`  
		Last Modified: Tue, 24 Feb 2026 20:03:05 GMT  
		Size: 13.8 MB (13821151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6522f8e1c3c7185646e4f40b57b3a987f4a19392cb2be80731e2f1716e178e`  
		Last Modified: Tue, 24 Feb 2026 20:03:04 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533bdf2f86b63bcad8ba9e0e39d6b76beefb4aa11f713b652ef0871ff626b99e`  
		Last Modified: Tue, 24 Feb 2026 20:07:59 GMT  
		Size: 14.2 MB (14212875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dcf7a6b4373c1b627ffea72525e2b8ba2ae815417bf5e61d43af607aac9cf58`  
		Last Modified: Tue, 24 Feb 2026 20:07:59 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22844853d427c07c770f9157adec10387fa126b7bcd07b7e885874eadc5ea9d`  
		Last Modified: Tue, 24 Feb 2026 20:07:59 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d539383a2114c608455cab0ffd7392493c7733af6d5ee8ea9c0efe118946119b`  
		Last Modified: Tue, 24 Feb 2026 20:07:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684e1e3870b04ba2a2128473e876dcf24d5f3a37b4db6a692852a5aaa0726880`  
		Last Modified: Tue, 24 Feb 2026 20:08:00 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3adc3d1d12c3e88313d156390c1df2df0e90a077b87f1c70ba4120f929823e8b`  
		Last Modified: Thu, 05 Mar 2026 00:23:06 GMT  
		Size: 3.0 MB (2950599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46aa585da2d09a81d23cf875e857b1b31ab99cf7c323e97327326c0cfbe1a3b6`  
		Last Modified: Thu, 05 Mar 2026 00:23:06 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e93f9ec90b2d1db6c5f5aabf0b4e43044f7a66a9c5a723dbf6624251fa5c99`  
		Last Modified: Thu, 05 Mar 2026 00:23:06 GMT  
		Size: 22.4 MB (22376412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f880ac4bf96833ab5300f65541d15a0ee38e2a05beae4c7534231628a892d20f`  
		Last Modified: Thu, 05 Mar 2026 00:23:06 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8190f737be1dc39d7acca01ecb991f819230b9f2dddc12d6f26da8ffffe69eb7`  
		Last Modified: Thu, 05 Mar 2026 00:23:00 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:e426c065de8accb8be94ea9ea9c4fac6c12087c05c2c9699c7fa2c39cb4ba5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d64f8b27f0b720e11c75b0e527173b9b2a95c56bfd4500f5275cac20d91b3625`

```dockerfile
```

-	Layers:
	-	`sha256:91a4d1c39c474e78f8e121fe25624b13d434cf7032a9e97ca2bd263d18d802b7`  
		Last Modified: Thu, 05 Mar 2026 00:23:06 GMT  
		Size: 33.3 KB (33296 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; riscv64

```console
$ docker pull matomo@sha256:7f8aa79fc58e03bf67fd6577b0782b5427b33b137037629941eb2e9460a7ed80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.8 MB (226810118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a99e4187f78f572b9f23711daaa63b4fbe6e228ca20471d65e76eaf8ba58f44`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 25 Feb 2026 08:39:18 GMT
ENV PHP_VERSION=8.4.18
# Wed, 25 Feb 2026 08:39:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.18.tar.xz.asc
# Wed, 25 Feb 2026 08:39:18 GMT
ENV PHP_SHA256=957a9b19b4a8e965ee0cc788ca74333bfffaadc206b58611b6cd3cc8b2f40110
# Wed, 25 Feb 2026 12:50:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 25 Feb 2026 12:50:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 25 Feb 2026 15:03:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 25 Feb 2026 15:03:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 25 Feb 2026 15:03:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 25 Feb 2026 15:03:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 25 Feb 2026 15:03:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 Feb 2026 15:03:29 GMT
WORKDIR /var/www/html
# Wed, 25 Feb 2026 15:03:30 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 25 Feb 2026 15:03:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Feb 2026 15:03:30 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 25 Feb 2026 15:03:30 GMT
CMD ["php-fpm"]
# Thu, 05 Mar 2026 05:33:34 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 05 Mar 2026 05:33:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Thu, 05 Mar 2026 05:33:35 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 05 Mar 2026 05:33:35 GMT
ENV MATOMO_VERSION=5.8.0
# Thu, 05 Mar 2026 05:34:57 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Thu, 05 Mar 2026 05:34:57 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 05 Mar 2026 05:34:57 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 05 Mar 2026 05:34:57 GMT
VOLUME [/var/www/html]
# Thu, 05 Mar 2026 05:34:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 05 Mar 2026 05:34:57 GMT
CMD ["php-fpm"]
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
	-	`sha256:8525b9f8a848966d3ec206f82a2654739f1e41fb0b21e8984f0b6f614bb8c5e5`  
		Last Modified: Wed, 25 Feb 2026 13:47:46 GMT  
		Size: 13.8 MB (13829070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed8dcbd305a50a3fbea850808b553c86268d0f94fcc9196cb7b8b3133f051e45`  
		Last Modified: Wed, 25 Feb 2026 13:47:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01547831776f253257c88b05c83a17f9bdccb7783321273caa23c62da3223e41`  
		Last Modified: Wed, 25 Feb 2026 15:06:27 GMT  
		Size: 13.1 MB (13138678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1f348300f7f4424908f160bb23f526f40525b86353a614c8395a2e1c0593f1`  
		Last Modified: Wed, 25 Feb 2026 15:06:24 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98182e7fa73379a5f5461b9087ba8ce961016ea20cc8c1b34d0c7d24d2c57136`  
		Last Modified: Wed, 25 Feb 2026 15:06:24 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a64cd29f70ef52098c03cbfa86b06522e81514cd83e8e33a70b68386bd76794`  
		Last Modified: Wed, 25 Feb 2026 15:06:24 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17f8b4823de057ecb77db55f687e3536bd896828f17986fe176157e615646d29`  
		Last Modified: Wed, 25 Feb 2026 15:06:26 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc64b3ffe47b589e1a1ebb61ce21cc1974d7272529c479379684448c34b34041`  
		Last Modified: Thu, 05 Mar 2026 05:36:15 GMT  
		Size: 2.6 MB (2590575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8035467cf62c0ee26fe7b5db6db2ac04982f97d6653b89c08a8f2b9d9261549`  
		Last Modified: Thu, 05 Mar 2026 05:36:15 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c2c3a7acf012b2043693cafc41fe763a4901dc468b0ff2f431e414e6d31d4`  
		Last Modified: Thu, 05 Mar 2026 05:36:19 GMT  
		Size: 22.4 MB (22376400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7195bf7cccd80deeae36b565fb87b5bbd0ccc7f09c79cb07d932a8fa962979ed`  
		Last Modified: Thu, 05 Mar 2026 05:36:15 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa55214e65e849c4c54ade88b1ca40e3fa74f8966870aa38e8d80223b7b404f5`  
		Last Modified: Thu, 05 Mar 2026 05:36:16 GMT  
		Size: 822.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:b920f7f649a619a9ade83afe98a973d8a46022954c3a9b5997cbd75ef91f6921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d4a2beb3f3cdef896f6438bb224fed7e30c7be76b42c510d59c6cd310171af`

```dockerfile
```

-	Layers:
	-	`sha256:0d3c56811fcb907a37d337655daf976efcbee1aaf609e8390ccfffeaa2388159`  
		Last Modified: Thu, 05 Mar 2026 05:36:14 GMT  
		Size: 33.3 KB (33296 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:5-fpm` - linux; s390x

```console
$ docker pull matomo@sha256:f3d5a4250359cfcf87d64e22a584b1b0848081354d5e4402d2bd3ba6824fc3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174808413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff9f7cf668f917539a74c7df49b52aacc6577be9f1bb3c531c7630e55c1b58a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Thu, 12 Mar 2026 23:25:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 12 Mar 2026 23:25:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Mar 2026 23:25:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 12 Mar 2026 23:25:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:25:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:25:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:25:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:25:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:25:54 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:25:54 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:25:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:25:54 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Thu, 12 Mar 2026 23:43:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 12 Mar 2026 23:43:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:53:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:53:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:53:00 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 12 Mar 2026 23:53:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:53:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:53:01 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:53:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 12 Mar 2026 23:53:01 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Mar 2026 23:53:01 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 12 Mar 2026 23:53:01 GMT
CMD ["php-fpm"]
# Fri, 13 Mar 2026 00:30:27 GMT
ENV PHP_MEMORY_LIMIT=256M
# Fri, 13 Mar 2026 00:30:27 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 13 Mar 2026 00:30:27 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 13 Mar 2026 00:30:27 GMT
ENV MATOMO_VERSION=5.8.0
# Fri, 13 Mar 2026 00:30:37 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Fri, 13 Mar 2026 00:30:37 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Fri, 13 Mar 2026 00:30:37 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 13 Mar 2026 00:30:37 GMT
VOLUME [/var/www/html]
# Fri, 13 Mar 2026 00:30:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 13 Mar 2026 00:30:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608bea8187e5ffa120471f60e9e30f31e918fed5484b52f271b7a54d1a5db916`  
		Last Modified: Thu, 12 Mar 2026 23:31:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddbbd9cd78a3df8f8f93c7eb5ec42029279dbe30f08f1e5f9692789f8f67556`  
		Last Modified: Thu, 12 Mar 2026 23:31:09 GMT  
		Size: 92.6 MB (92572080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc0754b1bc5a336f979da71da16e221438ff759f3570041153e4228ddfc581a`  
		Last Modified: Thu, 12 Mar 2026 23:31:00 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81d36a95efe74d511e37d836fc0139b73a0c803258f394377fea72b888268874`  
		Last Modified: Thu, 12 Mar 2026 23:48:30 GMT  
		Size: 13.8 MB (13830590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392684bfe541cae98ccc3508c97a2afc3e35e821b1a3773e95df83f6f289bcb6`  
		Last Modified: Thu, 12 Mar 2026 23:48:29 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4cf56c3c82d4593cfe1271b53e0ed0ca39e42aff4202fb46fe6af4c87444a0`  
		Last Modified: Thu, 12 Mar 2026 23:53:19 GMT  
		Size: 13.5 MB (13460892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afaca14a74238e5272ae9f3567bab702f29e213cf98dd9b0f2a7ae1e77280c2`  
		Last Modified: Thu, 12 Mar 2026 23:53:19 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac881fc205280821f7f5540b040ff7565c19dcf215f35164f2727f9bff361d9`  
		Last Modified: Thu, 12 Mar 2026 23:53:19 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e831dca7b38e40c5708cbabd1b9ca213752e90fcaf1fc564e2523ec73c80c2eb`  
		Last Modified: Thu, 12 Mar 2026 23:53:19 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7747be65e26a551227f61395b08b320f9e12e163b77ebea780331dc2430dcc`  
		Last Modified: Thu, 12 Mar 2026 23:53:19 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff953f5e58745d5ee6d71dc2afb30fb12738d4ee27f032f9879340ca4eba3308`  
		Last Modified: Fri, 13 Mar 2026 00:30:48 GMT  
		Size: 2.7 MB (2716495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f55502368192b93c9b567d6135b75775c26cc8ca6de3484dfb05cbc5045ac82`  
		Last Modified: Fri, 13 Mar 2026 00:30:48 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a5e6af179352b2560eca4ecc8563b7d4e1eacdcecd7ca8d05de003d24d81aa`  
		Last Modified: Fri, 13 Mar 2026 00:30:48 GMT  
		Size: 22.4 MB (22375491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c086fd43c5d9324db3382b9475a60e04bafea52e452206dbc7f8d5770fba0775`  
		Last Modified: Fri, 13 Mar 2026 00:30:48 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a49a6d3c169e8ad41eb25055b4c5765177e8c7323472cf3e58672e6e640ec6`  
		Last Modified: Fri, 13 Mar 2026 00:30:49 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:5-fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:ab28987daa4305e1e3dc62361216658c4af99dcc180b06a3fb3eac752021d628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6271ecf5a7000d4a1215aced853ff144c67ff91e595c1ab314e693b0b8d8cf77`

```dockerfile
```

-	Layers:
	-	`sha256:c722a5f0dc8e3be9dacd3279dc84067e0fd059a0e07904e05eb5af71128dde88`  
		Last Modified: Fri, 13 Mar 2026 00:30:48 GMT  
		Size: 33.2 KB (33242 bytes)  
		MIME: application/vnd.in-toto+json
