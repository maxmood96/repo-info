## `postfixadmin:3-fpm`

```console
$ docker pull postfixadmin@sha256:6ba70ea2fb15a3c4a98060cd50228a5db75a7fb257aa8092d5d39e92f9dd35f9
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

### `postfixadmin:3-fpm` - linux; amd64

```console
$ docker pull postfixadmin@sha256:c5e67c22c44a69f7ab7700187fe13e628e11e347c08de755a5db51b49e75c872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (177009804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5873bd4a92d7d1a1fe15b167f978bf4f72d576f0145e6efee85b4554030c0396`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6e2092f231d3f3e15d1686c3e1a0a4837072743b8a0cf2a22d23e63d6bf073a`  
		Last Modified: Tue, 21 Oct 2025 01:32:23 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b5d41a111bef2c5ea4161f1297a03af70a39b1bc16505c4225ffdd91045823`  
		Last Modified: Tue, 21 Oct 2025 01:32:32 GMT  
		Size: 104.3 MB (104329000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288c0d5c05a193e5a02e867f673e36228040d77b967211f76200f9b8f7359c12`  
		Last Modified: Tue, 21 Oct 2025 01:32:23 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6296a61ab28cb5acf029011ea2fc727ecf978f314ba2b651a0dfec6fa6e4462`  
		Last Modified: Tue, 21 Oct 2025 01:35:17 GMT  
		Size: 12.7 MB (12690596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309df4824ff8dbc00472f8c0121762aa91328423710879e0c1a5407634153e0c`  
		Last Modified: Tue, 21 Oct 2025 01:35:16 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1480ee299812a95f368284e7ea004784d4d4e4e24cdaaaba6ec23010d3dec15`  
		Last Modified: Tue, 21 Oct 2025 01:35:16 GMT  
		Size: 27.8 MB (27832285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38f317904194f92fe7f280623b737304e67ff79f5b2ce0832a4f1defb3e964a`  
		Last Modified: Tue, 21 Oct 2025 01:35:14 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:597c821d66d480cee6defc62afc846a841c93fc9a290ff2c6f1760ba4f4e0d85`  
		Last Modified: Tue, 21 Oct 2025 01:35:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63de90f73b361318a195a58fd88b777767461b357924c21e6b37bfa24b2cee40`  
		Last Modified: Tue, 21 Oct 2025 01:35:14 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf242d0a8e05d85afdd96d9169fec1ac580fb2af70c69544dc21a02396f67b1`  
		Last Modified: Tue, 21 Oct 2025 01:35:14 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147de133fb006a8cec299da9db58e3ad0809743f9cee4448eedfc86a008e672`  
		Last Modified: Tue, 21 Oct 2025 04:45:23 GMT  
		Size: 1.1 MB (1069396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32950387223393eb24faa0da0543987d0e08c69d98fd66d25ee3c4b305dd073c`  
		Last Modified: Tue, 21 Oct 2025 04:45:23 GMT  
		Size: 973.9 KB (973884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2ab04eca1bfdcb5ce977cbbccdb3d96c14bc3547007e5d85a7035ed50e3433`  
		Last Modified: Tue, 21 Oct 2025 04:45:23 GMT  
		Size: 1.9 MB (1871576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3174e1a9f637aa980e9e511f6f155f5eeddc74493ea42cd28eb430240d75d127`  
		Last Modified: Tue, 21 Oct 2025 04:45:23 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:c6096ca305b540552d1079950a57fde4b7a7539e13fc53f029c6b0d31623ce85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 KB (27338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e706d06dad20eaa21d300fcf9a53f20875f498a024621eb6150dd91a1b66ab4c`

```dockerfile
```

-	Layers:
	-	`sha256:281a053a25f5b4ad7985f155c01a360970217185b4c9295c6ca2d6409b6cba39`  
		Last Modified: Tue, 21 Oct 2025 11:10:51 GMT  
		Size: 27.3 KB (27338 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; arm variant v5

```console
$ docker pull postfixadmin@sha256:7fb8a30e1f531ab9c8ad04308b999b5464155805b5134dfb0923e43f3fa6fd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.6 MB (150577400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd495d00028a65d0a3fa39aef575d8046fd11ae9b579e9ec16a25cebad03ec5`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f982c9691d15a93fba0c1226ca85169d870439f0b6119d1ec61ec73d2a7dc8c3`  
		Last Modified: Tue, 21 Oct 2025 00:19:59 GMT  
		Size: 25.8 MB (25757495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44fb9cd576ea98721b54db5d96bd4c511d36d2f6ecc751ff798765a304ec972a`  
		Last Modified: Tue, 21 Oct 2025 01:25:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c750cc3ba1684ed361352ac98d1e4abaa2faca5a1fdd859a0c3d408b16cb8d9`  
		Last Modified: Tue, 21 Oct 2025 03:56:41 GMT  
		Size: 82.0 MB (81979291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7c829d09fc76d4eeded7e5a43ad90506553c84f0c83445b33226ccc84ea17a`  
		Last Modified: Tue, 21 Oct 2025 01:25:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cbc3a0af70f3652134e28c0b9c25a2a137ca303e60e14c3e844e00fe60b1b3`  
		Last Modified: Tue, 21 Oct 2025 01:49:30 GMT  
		Size: 12.7 MB (12688629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48327712030dd5b3b799d41356b913f0f2daad4ace75897688e7113cbe3b414`  
		Last Modified: Tue, 21 Oct 2025 01:49:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5556a2104e2da2ceef26e79c5c8be4e072c9dcd50352759e8616be528a7ce69`  
		Last Modified: Tue, 21 Oct 2025 01:49:31 GMT  
		Size: 26.3 MB (26311864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea934200974b574bb62baff1b544e63307c4ac4133bdf5db589a4a16d8598bf`  
		Last Modified: Tue, 21 Oct 2025 01:49:29 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c544b04600f748e4ab470f6454960d051f35453fe6875db9f7c3de047520dad4`  
		Last Modified: Tue, 21 Oct 2025 01:49:29 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b4b56710b71ecd0a43aba37f2a3d3dbfe9f5aa38b36a6fe562e21686e33067`  
		Last Modified: Tue, 21 Oct 2025 01:49:29 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57574c1a5a100e7c27d375bc99d976bd631993f4f4dfc35ad2b2594ecfe3ab2e`  
		Last Modified: Tue, 21 Oct 2025 01:49:29 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfdc5dd48cb173e821ae41cf428f0348b3a4f7e231d98e1fc4092a73d5a6ebb`  
		Last Modified: Tue, 21 Oct 2025 03:54:16 GMT  
		Size: 1.0 MB (1042367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbfdc2499a0c760a9117936ff016d316f74e601da17db44146d228a999221d5`  
		Last Modified: Tue, 21 Oct 2025 03:54:16 GMT  
		Size: 911.4 KB (911425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13d62176a94423aa349c0ea896a253e13b805501175043fc7e8c662059a15ac3`  
		Last Modified: Tue, 21 Oct 2025 03:54:16 GMT  
		Size: 1.9 MB (1871573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fbabe8b6d626816c54ac9a681e0b829c2c74f5a3a0467ac654f2219fa46c4fa`  
		Last Modified: Tue, 21 Oct 2025 03:54:16 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:c9f40125e9c00da89ab6f43aace2a1038ec2c84791d19eb57b0a3d0ce0558ff6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:820db01cdd38f003f13aa1525ca3ea021d4241b712d36d6614378a90919005a6`

```dockerfile
```

-	Layers:
	-	`sha256:9a454e66379ca216ca22e29bdccd33aa6ded5bc4d3ed5099accbe7d4da3cbce5`  
		Last Modified: Tue, 21 Oct 2025 08:12:37 GMT  
		Size: 27.4 KB (27439 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:ac3e937d7f7abed9969839f9622387df1ede03d76ea52ebcc411743c15d5d083
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141962407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1870129454dcd383c84eaaa738ffe7942c296867d402965965e2d2c75e7c831d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db362f2007f0c6ea734ddc2b6850d585de180d75bc0d1516aaa5efeaaf16c1c`  
		Last Modified: Tue, 21 Oct 2025 01:36:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6383a0b599d5b67491ea41d900df797d9a6a96481c1709b4ea7aa19d7f3d66`  
		Last Modified: Tue, 21 Oct 2025 01:36:23 GMT  
		Size: 76.1 MB (76147152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686e4d2c0afb9c9b15a86ae084a27380f01b3f9b7143f47d5262e965b6269d90`  
		Last Modified: Tue, 21 Oct 2025 01:36:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810821f0490304a83b194453166b41d319e9fdc3a7500d52f4aeb5305505b836`  
		Last Modified: Tue, 21 Oct 2025 01:51:52 GMT  
		Size: 12.7 MB (12688553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:794117016e6647991818456a54628527ab172b5de3064737cdfaa6390e298bf3`  
		Last Modified: Tue, 21 Oct 2025 01:51:51 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5d9d38355a2de1f5199bb9787452660f47598f05661956fad3ef0a71034ff3`  
		Last Modified: Tue, 21 Oct 2025 01:51:53 GMT  
		Size: 25.4 MB (25411749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7560b26d36c3644c59a04cc5518e6d2286e21db8442aec2ad64be159b8a388`  
		Last Modified: Tue, 21 Oct 2025 01:51:51 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a33149d51edd59d34555ad043c61662d4760ee11992c3aba6af1b93670aa36f`  
		Last Modified: Tue, 21 Oct 2025 01:51:51 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31f49ea292cd9596b49f37f8023c38dad5a8816115d88f88dc2949dba440ca6`  
		Last Modified: Tue, 21 Oct 2025 01:51:51 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986ed991ab99279d98fe2d8ab4e745992697500635ee55e7366e294d7d805fe4`  
		Last Modified: Tue, 21 Oct 2025 01:51:51 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26702d07aa1de6071ce130f1076007359cfe9ae26ec853ddde6bcbe2ab4aeb17`  
		Last Modified: Tue, 21 Oct 2025 04:08:48 GMT  
		Size: 1.0 MB (1035403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19edf67dd6be8c911aa09f9b495ad8e51d646bca0cb247c8cd5c0ec0955902d4`  
		Last Modified: Tue, 21 Oct 2025 04:08:50 GMT  
		Size: 859.2 KB (859190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c817fff08f289d8923378170cb1556b3096d4d1acda8e2227245f0f324425458`  
		Last Modified: Tue, 21 Oct 2025 04:08:50 GMT  
		Size: 1.9 MB (1871576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757b29c724015e6035d9218d554080f060e6a62afb74367d4d2ba703ceeed4bf`  
		Last Modified: Tue, 21 Oct 2025 04:08:50 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:4a9a3bd02fd4e82e16d9c0352a35f0742c474a486cc5de5a3db938b96426f17c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c59ed7aa20fbd3e82ad112b5096d2b6c106a5da7fff7128c502174aeaf7533`

```dockerfile
```

-	Layers:
	-	`sha256:909580b91d1784b84ef2d622aedfdeeef9f9e796a74ae22065fd200a2ba427cd`  
		Last Modified: Tue, 21 Oct 2025 08:12:39 GMT  
		Size: 27.4 KB (27439 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:0716e070c25d00e0b13e188b462bb53b2269d87bd4aaf1dd10fdbea38c3af665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.6 MB (170634055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696da062e633eb9379a2b30a73d0d906eee5ccaa1c51dd89ca0ca1fd686d1c98`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4736ec1e4c25a0ce44a2ace993730c4c38a48aefa2355daa7943f797d958d851`  
		Last Modified: Tue, 21 Oct 2025 02:10:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87815f77ddbbe745a613c3832988b09933f73f655005310b47a9295067afd83`  
		Last Modified: Tue, 21 Oct 2025 02:32:06 GMT  
		Size: 98.2 MB (98164200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752148909e57de5c110ab9de267d8c17df12ef90ff960d21631be1f3cce80430`  
		Last Modified: Tue, 21 Oct 2025 02:10:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bde930e22724e6010400ed3bb23a07ee802c97fb725f93b250334975257c91`  
		Last Modified: Tue, 21 Oct 2025 01:37:48 GMT  
		Size: 12.7 MB (12690325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a704d54dbee6e4415b50e201731418fea0a2150d13ff64d0a1039a774b0a5418`  
		Last Modified: Tue, 21 Oct 2025 01:37:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b76a81c4d83e91a2b9bc8b26e8e8b1a511c097d8a140e11e49f03d695da27d`  
		Last Modified: Tue, 21 Oct 2025 01:37:49 GMT  
		Size: 27.8 MB (27827561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ed330c6562173947de610b7a58f83707261571505b9b7299a76c97d0ef38b2`  
		Last Modified: Tue, 21 Oct 2025 01:37:47 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53899d2b739da9680096bc178fdc2656a626e9a129ed9dc1a5bcb4405cd90a4a`  
		Last Modified: Tue, 21 Oct 2025 01:37:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219febf2889e362a506688c3e401af944a7a88304e85f1ea46b88284d77d0637`  
		Last Modified: Tue, 21 Oct 2025 01:37:47 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c2c5b20660861c5c82d7187fa3774818bb60103edf6e00229f4c2b4828d5f28`  
		Last Modified: Tue, 21 Oct 2025 01:37:47 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b96aac4b59771862c8c0884d62048dcd4768fc659567d201b9bd52e39165c6da`  
		Last Modified: Tue, 21 Oct 2025 02:32:52 GMT  
		Size: 999.4 KB (999390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad97463c184f891e77dae32a143b5c3ba35466ee4d37c8485a95ff0ac6c64bf`  
		Last Modified: Tue, 21 Oct 2025 02:32:52 GMT  
		Size: 964.1 KB (964063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21047493462b032222a1f6d687a8ea973d478d45b3bbe6a6786a2dc43a2feb1`  
		Last Modified: Tue, 21 Oct 2025 02:32:53 GMT  
		Size: 1.9 MB (1871575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d653389930ea65798eaf61704a6a018eeab898c6cdcd4caea5a2822da6f85598`  
		Last Modified: Tue, 21 Oct 2025 02:32:53 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:8c374e69f9c31f9a195397dbaf20fe9a360b5e1ac5fc386dd3f8bfe803fdd724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39340645ed87980db330d600a0497cd5db3891bbbd743f8b768c9e69c3ead652`

```dockerfile
```

-	Layers:
	-	`sha256:f48f56f5c528d4f7557f23b79e040ab3d8725639e0dc82f5ceed4e60990b2c69`  
		Last Modified: Tue, 21 Oct 2025 11:10:58 GMT  
		Size: 27.5 KB (27463 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; 386

```console
$ docker pull postfixadmin@sha256:ab57aa55780b1f7628eebd7ac58fa38faa56f64f68086bccac38b3b97bab2aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175686896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eaec9e2c3a9a36615fef15bb1aa0f7db834fd71afa825060d0928e1e73e1208`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528b646879e5fa320639e0ebe59e000a4b64744644edeb44af5e6caeaa76674`  
		Last Modified: Tue, 21 Oct 2025 01:23:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200d03599c677f31c6e8448f915341815cdad6f03807d62b168b50a199ac2040`  
		Last Modified: Tue, 21 Oct 2025 01:23:35 GMT  
		Size: 101.5 MB (101514847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad9e9afc8203fadf64bf289963c69bb63b1ecc29e1decbde01b1397d94584a3`  
		Last Modified: Tue, 21 Oct 2025 01:23:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c0325a9604242bb05cc7e744ad1b3590245f113f256ff0fc53c137c413e45d`  
		Last Modified: Tue, 21 Oct 2025 01:35:55 GMT  
		Size: 12.7 MB (12689726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0086b7a910c5df4be74f55a0877e7fc9766a88160e11e1cbffc0efeae5224da2`  
		Last Modified: Tue, 21 Oct 2025 01:35:55 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bd08c61b6eeec06cf6114ceb910de67a55b532bb8873c57bc59b5870abf2b9`  
		Last Modified: Tue, 21 Oct 2025 01:35:59 GMT  
		Size: 28.3 MB (28340386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429b3a148fd5ab4ce7c694934b1ac23f989e11adad27991170102b0a4665c9a4`  
		Last Modified: Tue, 21 Oct 2025 01:35:55 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6ab53abc7f5a40b77aef100a2bb47e8d5232302f50a38b03d21b3c2e86176d`  
		Last Modified: Tue, 21 Oct 2025 01:35:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b37c0ba1d566dcfd31c1e15625612d2dd2149dc118fc87e0c6aab9e1040bc99`  
		Last Modified: Tue, 21 Oct 2025 01:35:55 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a10e25a3a527f8d510be6e3af6dd3dfeaff5a86194285529fbc2828314d083`  
		Last Modified: Tue, 21 Oct 2025 01:35:56 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa7d5b26e5558dd4ed7056f39a4f0702e7cf7c4441e0ad2ab230424cc499a5b`  
		Last Modified: Tue, 21 Oct 2025 02:32:57 GMT  
		Size: 1.1 MB (1054282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe0d0e4ed3842fbb77607863bfb552e995db24e8cf74e3de20dffe45024f183`  
		Last Modified: Tue, 21 Oct 2025 02:32:57 GMT  
		Size: 991.7 KB (991668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b099f7bc80e174acf350f3f8eb2ea4a2183d358112fa648f60d70a78d27122`  
		Last Modified: Tue, 21 Oct 2025 02:32:57 GMT  
		Size: 1.9 MB (1871574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b48580aec0d26b68fd8bf619fbc68edb1eaf930d5b215621438dac1814f590`  
		Last Modified: Tue, 21 Oct 2025 02:32:57 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:46ab30c5826038bc9e60eec2e33a6f0e81af3a2e994a9386aa9ff30c34e1de08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 KB (27301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50cdf0fb19519e62005448acc898b7c7bcaa0cfff146c9f9231e2d9c5ed7cf6c`

```dockerfile
```

-	Layers:
	-	`sha256:5b16b0370e3caab52c655d2010335b16ccab75ce3364ac87ef77816a26158cbc`  
		Last Modified: Tue, 21 Oct 2025 11:11:00 GMT  
		Size: 27.3 KB (27301 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; mips64le

```console
$ docker pull postfixadmin@sha256:65128f0b5bab0b9f804a656db7c782278dc57e9a3c5ca062bb44a500242fcc92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152570832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a05d920339e747944ee3554fc7a218c16b8863dc4745817737d456c7cde2ab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1759104000'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:73d0a1261a90ced7c792643cb457a2c9f7bbeca1bcb84939b4029c5a1f01f26c`  
		Last Modified: Mon, 29 Sep 2025 23:34:06 GMT  
		Size: 28.5 MB (28513676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03232016453cd060197e2a81f928170eb114761525dd3c00d9c3384ae2ea93a1`  
		Last Modified: Tue, 30 Sep 2025 01:01:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328cd0006dcf6f780bfb278c18a1cd05d5749f4ae1dc56b6871eda9ce8337a0f`  
		Last Modified: Tue, 30 Sep 2025 01:01:10 GMT  
		Size: 80.7 MB (80669954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b051af170b89147ad2709eb996909dd4f1c5c675586ecff406438604a808c3f`  
		Last Modified: Tue, 30 Sep 2025 01:01:06 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdadad0b3ba529a8b9ef55fac867f8bb045559ba584f174c9834f0caa4021d7f`  
		Last Modified: Tue, 30 Sep 2025 03:30:03 GMT  
		Size: 12.7 MB (12688171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89674e979ee08939162b0605cbd16174fec64b02e42efbbfc93dbeb452effc21`  
		Last Modified: Tue, 30 Sep 2025 03:30:02 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a437a68492ea6ec36a4256e7bfba928e5b61915b352fabc5285f2cc1950638`  
		Last Modified: Tue, 30 Sep 2025 04:04:13 GMT  
		Size: 26.9 MB (26926487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429c036538a6019fd9683b41460efc42d5f1479678acd40c79cb55c41c383e3e`  
		Last Modified: Tue, 30 Sep 2025 04:04:06 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545f63fe2a6d05a2911cf756beea8dd20a79ba2d44fe264f9745f7841c0fed14`  
		Last Modified: Tue, 30 Sep 2025 04:04:07 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508bbdc3082cec6156356091d213fd761d9f2ea81bac6ede9219ce7c823b3bcc`  
		Last Modified: Tue, 30 Sep 2025 04:04:06 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afab336af1617737a9b79c4bf1d76a7bd71e838862ca97c66cc55053d9839dca`  
		Last Modified: Tue, 30 Sep 2025 04:04:07 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff41261f1b6bc571e549ea08de67ac82c9139f431ad5d5262ab2f6aed40e391`  
		Last Modified: Tue, 30 Sep 2025 20:24:11 GMT  
		Size: 950.7 KB (950682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d682783c2192e2a028f136846fb1a6c06bd52dcecd725d7ed23bef37d5a45fbc`  
		Last Modified: Tue, 30 Sep 2025 20:24:11 GMT  
		Size: 935.5 KB (935533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcb8bf91238f6058922c1d39367d1f19e90124dbe967c39a962aed33ed82332`  
		Last Modified: Tue, 30 Sep 2025 20:24:12 GMT  
		Size: 1.9 MB (1871573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967575859ea8d04f7b0670159e6280a3d50751e3113091ea15c37999f2f83d37`  
		Last Modified: Tue, 30 Sep 2025 20:24:12 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:eb7a2a4a1f381485e4c38e38bf50258b5dc97dd3c27d4789bac299d86f9f5e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:877974ec19181d4160d905462e07de1ce042aa196a7cde4bc2255553d3d553eb`

```dockerfile
```

-	Layers:
	-	`sha256:a168a62ee1bda105e73073c70a3567606023b8f4822e5a8e51f449002fe897ef`  
		Last Modified: Wed, 01 Oct 2025 20:12:10 GMT  
		Size: 27.4 KB (27401 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:4e09ddca799636a073f71a6b1fce502daeacd286cb3bc6e9a23cb7a3679e860c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180967806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efb5e3267de55fe33d6af9a9fed453fcff0b66487c1d2d2554b2c9c9e7eb238f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9224126999b17ea18ad3192bf1f731d4bb9aa32a52f09c442a3de3ba3b786f3`  
		Last Modified: Tue, 30 Sep 2025 00:21:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e6783fc03077e22b7c9e12c11882548b0054a2663a8ef49358f7327baf349e`  
		Last Modified: Tue, 30 Sep 2025 00:21:18 GMT  
		Size: 103.3 MB (103328743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33ae54ede2b3ffe909b51995334afb653bfac09e40805963f18c29327385318`  
		Last Modified: Tue, 30 Sep 2025 00:21:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157426c83a0db521326f3bd23ef7d242162b529347edd41255ffc4b5cdfa3882`  
		Last Modified: Tue, 30 Sep 2025 00:59:05 GMT  
		Size: 12.7 MB (12689917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5877f2465c291340a030d37422f088612116baf95ec952368ec65b90509692`  
		Last Modified: Tue, 30 Sep 2025 00:59:04 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d0860d07494cb51b8f66d53eb87d87dbfbed24a2ba4f7da42088552800a2b3`  
		Last Modified: Tue, 30 Sep 2025 01:08:09 GMT  
		Size: 28.9 MB (28902882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7608aca2479e8ecde41014d384698c22d88710b360b78152d4334708a9942624`  
		Last Modified: Tue, 30 Sep 2025 01:08:07 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e3f0f4311d7caecc527e1bfca7ac1d33367aa862ac19c095c353b67762172d`  
		Last Modified: Tue, 30 Sep 2025 01:08:10 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f236d03a5a19a8f09f56a9fd1a9963af0773a4e4a6fa91118aa8e474dd38429`  
		Last Modified: Tue, 30 Sep 2025 01:08:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6a2e0f16b6c228f8059e3330369482ef618546018b6f9e6155feb15ad24637`  
		Last Modified: Tue, 30 Sep 2025 01:08:10 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6865a4cec78f3c8eafed81a6ff38dd263c3de1fa75f903e0cee7033654774881`  
		Last Modified: Tue, 30 Sep 2025 08:51:13 GMT  
		Size: 986.2 KB (986214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18747205e2b30ced91142e4d87fed38ff698a680e513a65b2257a5cb61a24c2a`  
		Last Modified: Tue, 30 Sep 2025 08:51:13 GMT  
		Size: 1.1 MB (1105034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2537521489b29d4dc1fbd20ce7f852c210d685f6179976c2c5549c5a0f4ca9bf`  
		Last Modified: Tue, 30 Sep 2025 08:51:15 GMT  
		Size: 1.9 MB (1871563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d048fc9dec6ad0ed59b026eb730711e2454bc3bb88b0f3e95eef524fb205b544`  
		Last Modified: Tue, 30 Sep 2025 08:51:15 GMT  
		Size: 1.7 KB (1655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:9925dcc948ad2c1fa08cdbf3efb69b3ab4a7638fbae639ccbdbad5a7266e551c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c9cdf10298452b225639f5d3509fe2353ae19c3d4311d27eb2d68ad6924443`

```dockerfile
```

-	Layers:
	-	`sha256:26a9f0523293ccf13cc278078cd460dd10910dead32e1786fac238400fe0c9c1`  
		Last Modified: Wed, 01 Oct 2025 20:12:24 GMT  
		Size: 27.4 KB (27385 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:3-fpm` - linux; s390x

```console
$ docker pull postfixadmin@sha256:7d6512e29968c14a601364d47653102a5a98b0d4674aad2ee52c8bca9db35437
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.2 MB (151221605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef5faf86a29c20aab77cc878e616e444d5e53112387c380ad4e2d438fb06ea2`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 11 Sep 2025 11:18:55 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1759104000'
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Sep 2025 11:18:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_VERSION=8.3.26
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 11 Sep 2025 11:18:55 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Sep 2025 11:18:55 GMT
WORKDIR /var/www/html
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Sep 2025 11:18:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
# Thu, 11 Sep 2025 11:18:55 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libc-client2007e-dev 	libkrb5-dev 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 		docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ARG POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_VERSION=3.3.16
# Thu, 11 Sep 2025 11:18:55 GMT
ENV POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
# Thu, 11 Sep 2025 11:18:55 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.16 POSTFIXADMIN_SHA512=d1b8074c32f7912c187c2c37c5cca158432cb85fc415d9efe86cf11f70ab035117053cc579306e224cb180e70fa3c84a68335f18d62b43abf591e8105a00847d
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Sep 2025 11:18:55 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 11 Sep 2025 11:18:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ee23af7e2c95e7ad71a0f6edf7e138d45ffffb442811e2b9572806a68ee1338e`  
		Last Modified: Mon, 29 Sep 2025 23:34:05 GMT  
		Size: 26.9 MB (26884320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d82124f58a645a9da3f15f3da28d4ca1455d28e5d91846444d1052535447d`  
		Last Modified: Tue, 30 Sep 2025 00:04:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b01b9ac7d1cffa33f9a421d32a8141448890b76a8a421333ce992c42c236f2`  
		Last Modified: Tue, 30 Sep 2025 00:04:05 GMT  
		Size: 80.8 MB (80826420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37f8a2c56e71c89a84dc64f20767ac8e393ae6bf31491b671931026500a94fa`  
		Last Modified: Tue, 30 Sep 2025 00:04:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081f7f3c28c747231d2ec89121bd05941697caf82786481143168a84e8d99f33`  
		Last Modified: Tue, 30 Sep 2025 00:49:31 GMT  
		Size: 12.7 MB (12688987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b113f3e6f349a8c69daef1b35f8b2595beeb3ca812fde01a0b2fa6156cd014`  
		Last Modified: Tue, 30 Sep 2025 00:49:30 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52755a21ae2ecf99b758ae45971a2ca86dd0ee515c5a2768860e7756bc53bf5`  
		Last Modified: Tue, 30 Sep 2025 00:49:33 GMT  
		Size: 26.9 MB (26937676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba6cb8c23b4e73af714fe6f6d9b7093721f31bfbb6b683ffd4b420d9e4873f0`  
		Last Modified: Tue, 30 Sep 2025 00:49:31 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9886f63208cf2ac814703777c1d158b72bf4936777c239fe2cec32cae6e072`  
		Last Modified: Tue, 30 Sep 2025 00:49:32 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49494fa4c0f78c685af3fff87226e662d26e81e8719a7fa0fe49668327a1144c`  
		Last Modified: Tue, 30 Sep 2025 00:49:32 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c241e86fc5be5be1fa712e55fe589383f1b6eb88b7a6f408c357c5818915f870`  
		Last Modified: Tue, 30 Sep 2025 00:49:32 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b204fa50943a5cc63072a3c80a64fc7a46cd45ff58729d340e40049742cd8961`  
		Last Modified: Tue, 30 Sep 2025 08:05:16 GMT  
		Size: 1.0 MB (1034804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a7425e3154fe6f2bb8c5009239750becac315f96a93700eb81dc67d5e5f752`  
		Last Modified: Tue, 30 Sep 2025 08:05:16 GMT  
		Size: 963.1 KB (963078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a62ae75c5c8749b0c6304018cb2334ed465776a5a9f10530b6cd736f507a0e`  
		Last Modified: Tue, 30 Sep 2025 08:05:16 GMT  
		Size: 1.9 MB (1871574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c78c44e6c61c79f1ca72501899d8550ef3adde2bec5a16df2d0b8dfc29f2a1`  
		Last Modified: Tue, 30 Sep 2025 08:05:17 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:3-fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:d5cd45f3bf20ae9b7273573da44938bc3a97c8d9d9fcdac1989fbefa2d19b4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 KB (27332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3da35f1c791bc321dbd33cfcbabcbcb7c4ec121a16c3a707f03c6aa5fdf80018`

```dockerfile
```

-	Layers:
	-	`sha256:95ce92ef593f3c5ea436f7066f5f02fe2ec5753217704a1864e5a01aabbd618c`  
		Last Modified: Wed, 01 Oct 2025 20:12:15 GMT  
		Size: 27.3 KB (27332 bytes)  
		MIME: application/vnd.in-toto+json
