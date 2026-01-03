## `postfixadmin:fpm`

```console
$ docker pull postfixadmin@sha256:16aa6991ebc7473903a13484aa61936690d6c64dab5eb30cd7fcd72e5f65fc07
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
$ docker pull postfixadmin@sha256:8f34a83d187fd23707e02a9b29c7292aeee05c12baccff769a3200d00dc57def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200810996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23732863b3f41fa6a96ab4370b410b3cfdb2953843b8d721e877a1fbb736f160`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:27:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:27:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:27:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:27:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:27:40 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:27:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:27:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:30:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:30:23 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:30:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:30:24 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:30:24 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:30:24 GMT
CMD ["php-fpm"]
# Fri, 02 Jan 2026 22:48:10 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 02 Jan 2026 22:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Jan 2026 22:48:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 22:48:34 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Fri, 02 Jan 2026 22:48:34 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 02 Jan 2026 22:48:34 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Fri, 02 Jan 2026 22:48:34 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 02 Jan 2026 22:48:35 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 02 Jan 2026 22:48:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jan 2026 22:48:35 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 02 Jan 2026 22:48:35 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 02 Jan 2026 22:48:43 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 22:48:43 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 02 Jan 2026 22:48:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:202811c68f67e44bebb8cbcab5368426f755e61daafc226e0a11505731a32610`  
		Last Modified: Mon, 29 Dec 2025 23:30:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24273ba12d1af0810d7820c7c75ca2b3fe832cb221b71e49e6c26c8138dc23e0`  
		Last Modified: Mon, 29 Dec 2025 23:31:02 GMT  
		Size: 117.8 MB (117838542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d35c8551543daa57c82c78738cce70808d7814d181a064fb5a6e35cfae3f4e`  
		Last Modified: Mon, 29 Dec 2025 23:30:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0c35ab5e15ef59f75876f694971c7463b29b5439f72fd75d99b7bf75bdbb20`  
		Last Modified: Mon, 29 Dec 2025 23:30:56 GMT  
		Size: 12.7 MB (12749880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ca494a431dd2878f8739fdb5e76c388a0722b00a6391cb5e36e301ff30df2`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287427e4d8f82a4a368376d90e27813a59b8f1f04f20fc9e3f94f8a5ac5b8d92`  
		Last Modified: Mon, 29 Dec 2025 23:30:54 GMT  
		Size: 11.9 MB (11897962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34ad282648acf930cde22d3abf9cc4ab8aa1e17235fbf4c93b10b667c9e302b`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f29fae1d861375d38b732c702d2361e1fac4c61e26c709a55bf974f14d12d2`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc2f98800abb9ff3433c4cb8758f3e376655b54cddcfa08febd96507f60ca1d`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2222a5f3710ed1173899dad10c5c5b165fed76153a242c880e607e4cf592940d`  
		Last Modified: Mon, 29 Dec 2025 23:30:53 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278d6c92ce45aaa9471a0ccdccb7ab428d27a45dd7092ce95e2f1e54a4bd2f69`  
		Last Modified: Fri, 02 Jan 2026 22:48:57 GMT  
		Size: 1.3 MB (1328598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6103d84d67744fb66601ab4370f5c60af5038bf34bd421021c4cd73644a3ca`  
		Last Modified: Fri, 02 Jan 2026 22:48:57 GMT  
		Size: 442.9 KB (442857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:429c5a51580fbeb34a1dad137b06dcbae399ab9d0284a2fc50b6aefafdf06706`  
		Last Modified: Fri, 02 Jan 2026 22:48:57 GMT  
		Size: 2.6 MB (2602185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8122f0da79d50e25be7201561b21d5dd3792f78c619aa45a98f21865e83208c8`  
		Last Modified: Fri, 02 Jan 2026 22:48:57 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba29ca1994113288153dd17cf714be4e4e85c118be7117a207fab47616229547`  
		Last Modified: Fri, 02 Jan 2026 22:48:57 GMT  
		Size: 776.4 KB (776364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e4564e890e016d950cc25a32a857787d26153bcdac6d1662eb5a0e7f4b62c1`  
		Last Modified: Fri, 02 Jan 2026 22:48:59 GMT  
		Size: 23.4 MB (23383316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:d7a1dc3f8b10c522e5d4a3e8268cffb5a29a5f47e9fdd22a013aec16d31de992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 KB (39515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87eb51d5ed5934478c685a346047e019778bdcd61d5229169a9820880bf944e1`

```dockerfile
```

-	Layers:
	-	`sha256:2088ecce7fc7caf34dd20d87e29d4cb997ae364e9306c9ce5fed780f2d9ad1f1`  
		Last Modified: Sat, 03 Jan 2026 00:11:38 GMT  
		Size: 39.5 KB (39515 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:e29c3b202a7433045c4e4bf5655a6ab2ce82d9bddcb3e716944752c004bfe3fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163720771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dca026c4db43e0eac36cddb631a9a4b2a8999da494262e042a0e150b1a62f37`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:29:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:29:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:29:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:29:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:29:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:29:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:29:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:29:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:29:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:29:47 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:29:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:29:47 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:37:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:37:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:40:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:40:12 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:40:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:40:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:40:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:40:12 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:40:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:40:12 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:40:12 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:40:12 GMT
CMD ["php-fpm"]
# Fri, 02 Jan 2026 22:48:03 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 02 Jan 2026 22:48:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Jan 2026 22:48:30 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 22:48:30 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Fri, 02 Jan 2026 22:48:30 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 02 Jan 2026 22:48:30 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Fri, 02 Jan 2026 22:48:30 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 02 Jan 2026 22:48:30 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 02 Jan 2026 22:48:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jan 2026 22:48:30 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 02 Jan 2026 22:48:30 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 02 Jan 2026 22:48:40 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 22:48:40 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 02 Jan 2026 22:48:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60d257465ef706cfa22a190814fccc60eefcd37b46498f5571945aadeb3076f`  
		Last Modified: Mon, 29 Dec 2025 23:32:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56bdcf35d3961ce06862f400055da0b883def51d93268be39294e33a84d05b0`  
		Last Modified: Mon, 29 Dec 2025 23:33:18 GMT  
		Size: 86.2 MB (86245474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e36243135caedbd8694c70fdcbf31f2c9654dfd5ffbde24d9e3de97b0eea65a`  
		Last Modified: Mon, 29 Dec 2025 23:33:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b7732921aa86052d37cb7af328a474d7df466bd250c77416ad3ea6b47dfcf7`  
		Last Modified: Mon, 29 Dec 2025 23:40:31 GMT  
		Size: 12.7 MB (12747410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b12c1783da84249c156e8a2ff53e005c749148e32ad1146c48c034045a9774`  
		Last Modified: Mon, 29 Dec 2025 23:40:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80625b72aad62ebc26920eb1b4f90fc20c2bfabd8dda4d249f77f36bcb860941`  
		Last Modified: Mon, 29 Dec 2025 23:40:31 GMT  
		Size: 10.1 MB (10079338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20157e1887a5b19397f2cb782c7e353658b23b3dc0a4ce65379b4627d24deff2`  
		Last Modified: Mon, 29 Dec 2025 23:40:30 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1bff9c4191ca6aedf1da264ca4ca55db1ec5d145232d77f38829b81eeaae452`  
		Last Modified: Mon, 29 Dec 2025 23:40:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1c174892eb8ae557b49c747a705898afe9b77f9e7edaef3cd634a51dfdfddc`  
		Last Modified: Mon, 29 Dec 2025 23:40:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7df143d7e95602ec4a6c9be8f602ce86330874b2d302c8a629f478c32cfc`  
		Last Modified: Mon, 29 Dec 2025 23:40:30 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c08431cf1223d645f176acb9f0c5c32a8d7b5a3ce4bc9e3f9fd92cc73ec7a88`  
		Last Modified: Fri, 02 Jan 2026 22:48:54 GMT  
		Size: 1.3 MB (1265936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b6afa96fe3a18a8cab29c9ca9ca1236c186391359452fac8eff2846f9ce79f`  
		Last Modified: Fri, 02 Jan 2026 22:48:54 GMT  
		Size: 398.1 KB (398115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ea6851e6befcc47ab0d805307a45be159925e94bf4491a023956bb0b81a4bdd`  
		Last Modified: Fri, 02 Jan 2026 22:48:56 GMT  
		Size: 2.6 MB (2602185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b50d8b24493794d640493e607d8b3893479a571e17ed3b6bbf82d6e054d1fe`  
		Last Modified: Fri, 02 Jan 2026 22:48:54 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:275fca57f6055fddd35cf3b33fbd7139f4a9a47989423e79d15afb62f6ebb5b3`  
		Last Modified: Fri, 02 Jan 2026 22:48:54 GMT  
		Size: 776.4 KB (776359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5ffa50e756c91688a72675953512a804010f7141b3e2b3c216d114b72f1f8e`  
		Last Modified: Fri, 02 Jan 2026 22:48:56 GMT  
		Size: 23.4 MB (23381199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:8ede6acc67ffd97fee41e2f04512d95d45f76b0d730441271a907bfed3bf2fae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c65101d8d608d994465b88d21d708bc1f1d10995d473fd2c932d9ff5bb42a92`

```dockerfile
```

-	Layers:
	-	`sha256:6737d99c15baa17fd9b90456dcc022ca9f6e35c6d56790903eadf5fdaf14ea74`  
		Last Modified: Sat, 03 Jan 2026 00:12:34 GMT  
		Size: 39.6 KB (39648 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:448314d7aec659e139e24b1b15b6e501a394b6d24700999f80e4103ba4491043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 MB (193433523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9e5ed9fbfd7e45b91044109e7682a41fb79a46a7f18c41ef76af040658c452e`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:27:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:28:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:28:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:28:08 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:28:08 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:28:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:28:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:32:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:32:01 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:32:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:32:02 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:32:02 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:32:02 GMT
CMD ["php-fpm"]
# Fri, 02 Jan 2026 22:49:49 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 02 Jan 2026 22:49:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Jan 2026 22:50:12 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 22:50:12 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Fri, 02 Jan 2026 22:50:12 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 02 Jan 2026 22:50:12 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Fri, 02 Jan 2026 22:50:12 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 02 Jan 2026 22:50:12 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 02 Jan 2026 22:50:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jan 2026 22:50:13 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 02 Jan 2026 22:50:13 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 02 Jan 2026 22:50:22 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 22:50:22 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 02 Jan 2026 22:50:22 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6f857c375092a498e45aa7e4eafede989661dab3df985f8991a4ec8708f4f7`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50be2b43a73faa2ac649448727767a1a8b893c5944a0cf84ead770caba14a28`  
		Last Modified: Mon, 29 Dec 2025 23:32:42 GMT  
		Size: 110.2 MB (110162775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f2ce11fa03a0aa05db30d42e8f83ec994ed53ee47288f65308f077c2fe83f`  
		Last Modified: Mon, 29 Dec 2025 23:31:43 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ec25fe35ec5081a533a586a0699c25483e293b81af559d48fb2c2c73a949ee`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 12.7 MB (12749425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b600cf4286483f95b3815be58c0d61c02de463ba0dd5fec5cd4ceaa97cf53d`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d6e73ddc39ef42a8ecb65f58e8a3f6051336f63897f8c53643e0f6a93d9025`  
		Last Modified: Mon, 29 Dec 2025 23:32:33 GMT  
		Size: 11.9 MB (11925365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad922c5b18ddb1921f9a712389844117402404cc8efe4f58479a3f5648aadbbe`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f7c886390f32ea4216e380e105aa4d795302d8b140ee5844f12bb66f360273`  
		Last Modified: Mon, 29 Dec 2025 23:32:32 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51943d2c724f5ee7fb7b30c30d2c4da72ff114d29ede9253b9a361d558d85255`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f1b42487df6bb0a9e4fe65b9428ce018a5441e4ed3b17b898bef965e59396ee`  
		Last Modified: Mon, 29 Dec 2025 23:32:31 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b2f52e7c03911da68080316854272603b08f7295d72f56d2d6c2c04e70f24f`  
		Last Modified: Fri, 02 Jan 2026 22:50:35 GMT  
		Size: 1.2 MB (1242452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09793589dcffa7b020d0d8c0f68c3bedaeac8356ea358c80461452bbf8207dab`  
		Last Modified: Fri, 02 Jan 2026 22:50:35 GMT  
		Size: 438.6 KB (438565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffb423f7d1e154252f3f2522c539767eefc9c5ca6955a4c69581d2a41fd1541`  
		Last Modified: Fri, 02 Jan 2026 22:50:35 GMT  
		Size: 2.6 MB (2602185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43651923b65e0a4ee78d0769bff239994f7bef775fdeca86fd27fe063598ffe`  
		Last Modified: Fri, 02 Jan 2026 22:50:35 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb2940611eb09de802ea6ee7102168e19c4e64d9eaa5d091fb63fecf0e94e07`  
		Last Modified: Fri, 02 Jan 2026 22:50:35 GMT  
		Size: 776.4 KB (776364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:927e90ecbb2f8325c0b3dd9a72eb153a2383581964e8ada75f6f65c6588bdf0e`  
		Last Modified: Fri, 02 Jan 2026 22:50:38 GMT  
		Size: 23.4 MB (23383002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:b4738c8f6d5e7981fd5ac106b8da388d60da50afc9ec785b6720688d26f2660f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.7 KB (39690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13658512310577370168f6afe413a63ef91e44dcf458147c3a878374643b8e8`

```dockerfile
```

-	Layers:
	-	`sha256:7ea330b800b944e92d5911ba2d233e74dbcbf29ea37291d4e15d8db906fb71d3`  
		Last Modified: Sat, 03 Jan 2026 00:12:37 GMT  
		Size: 39.7 KB (39690 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm` - linux; 386

```console
$ docker pull postfixadmin@sha256:94ea75b1c7a84e68567bf2874552bbe14e5c5cd88ce019582290c0063ee4f71c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.8 MB (200807563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b8f3bdb139d2110f38908624ca2818aa0ed3a2b6c5d374ab10d86c26e1d223`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:17:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:17:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:17:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:17:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:17:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:17:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:17:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:17:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:17:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:17:35 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:17:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:17:35 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:25:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:25:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:27:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:27:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:27:50 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:27:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:27:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:27:51 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:27:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:27:51 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:27:51 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:27:51 GMT
CMD ["php-fpm"]
# Fri, 02 Jan 2026 22:48:57 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 02 Jan 2026 22:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Jan 2026 22:49:20 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 22:49:20 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Fri, 02 Jan 2026 22:49:20 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 02 Jan 2026 22:49:20 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Fri, 02 Jan 2026 22:49:20 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 02 Jan 2026 22:49:21 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 02 Jan 2026 22:49:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jan 2026 22:49:21 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 02 Jan 2026 22:49:21 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 02 Jan 2026 22:49:29 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 22:49:29 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 02 Jan 2026 22:49:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91116053ef5225d9d07ba3c903ddd3bdb2a52efd59b05ad5963fefac66a69948`  
		Last Modified: Mon, 29 Dec 2025 23:21:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7968b8a90ec8512c2573b684938ddfe9b775f1774063835063917691d89e0955`  
		Last Modified: Mon, 29 Dec 2025 23:21:16 GMT  
		Size: 116.1 MB (116138447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add46806ee20b4ca07312288c52d57d3dc097b468b85ed58b5b6b1f1e91a5c3d`  
		Last Modified: Mon, 29 Dec 2025 23:21:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34be806f546626f032ec588c35d59b4d972f1140df5f9f023dd11ff4ca464a30`  
		Last Modified: Mon, 29 Dec 2025 23:28:10 GMT  
		Size: 12.7 MB (12748783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8077ab6d8372165dbab5c8dd414749568a291f2655575daee0c856920d7c274b`  
		Last Modified: Mon, 29 Dec 2025 23:28:08 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4367ea6665f1302e1eca7b901c22fd5ec3d7a7ed08ee4fea422db3d6b382f595`  
		Last Modified: Mon, 29 Dec 2025 23:28:10 GMT  
		Size: 12.1 MB (12104775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e064c57ac5e331a0ac2e1f5626b64070a4af506a81bce47434b998290be098`  
		Last Modified: Mon, 29 Dec 2025 23:28:08 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e89204effc643bf850d1ccb1de1eea1d083ad909a304c9c3b5cb4da104de3bb`  
		Last Modified: Mon, 29 Dec 2025 23:28:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01b5f70e983467465a8cf6a4a2d778e978d5cb09bd53f0711430b16b1e01d27`  
		Last Modified: Mon, 29 Dec 2025 23:28:08 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c81b36e207d0f0628b284b0ff55a2b4bdb1d71b187ccd16637aa02d3dce733b`  
		Last Modified: Mon, 29 Dec 2025 23:28:08 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c4a7fc4327631c949d68648f9e3950d51676fb51fc7adc0968f546d59e65cd`  
		Last Modified: Fri, 02 Jan 2026 22:49:44 GMT  
		Size: 1.3 MB (1287591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f07775e8e15df3a5e62b3254acb94a90832a3bee5a4223faceffe291d987d1`  
		Last Modified: Fri, 02 Jan 2026 22:49:46 GMT  
		Size: 458.9 KB (458935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5bf204380a74342b03af7e95cd10399b8715d7d213b93fbaf88a7db6cd8fef`  
		Last Modified: Fri, 02 Jan 2026 22:49:45 GMT  
		Size: 2.6 MB (2602187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283d521b9158449f31558c699a85e1651d7d147e240c325cb7e14cd100dbe6f5`  
		Last Modified: Fri, 02 Jan 2026 22:49:44 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f489b6c1cabf74faf6cb44d0508d725b4880c903255e834e6111d9066b66fefb`  
		Last Modified: Fri, 02 Jan 2026 22:49:44 GMT  
		Size: 776.4 KB (776359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162d731d148c7f811ac14468365435f2105c55f9f058443d7f7972f5e7e892b`  
		Last Modified: Fri, 02 Jan 2026 22:49:46 GMT  
		Size: 23.4 MB (23382634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:2220e8ae9601bda779f91a721b8dc32e43dabb0334ed0c7e244ec375d3d57363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 KB (39470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df8653e68d7c0644a8f3cdb40660fe3a7ea0ecd6204ec122e17a0eeabe9f6919`

```dockerfile
```

-	Layers:
	-	`sha256:7d5419972db0c54a1d278bd9020ad2c4f4cf6eb4affb55cca4a1d08d8a7a5590`  
		Last Modified: Sat, 03 Jan 2026 00:12:40 GMT  
		Size: 39.5 KB (39470 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:7b8d3fa51ee1d727e541812bb5e9421acde3bcd40b0935239373f5a26155d0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.9 MB (196879636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065685d43e939200da8892bde2a8aceba5dc6ae726b825531d8a099918561ce4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 16:33:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 30 Dec 2025 16:34:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 30 Dec 2025 16:34:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 16:34:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Dec 2025 16:34:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 30 Dec 2025 16:34:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 16:34:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 16:34:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Dec 2025 16:34:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 30 Dec 2025 16:34:06 GMT
ENV PHP_VERSION=8.3.29
# Tue, 30 Dec 2025 16:34:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 30 Dec 2025 16:34:06 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 30 Dec 2025 16:57:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 16:57:57 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 17:01:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 30 Dec 2025 17:01:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 17:01:38 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 30 Dec 2025 17:01:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 30 Dec 2025 17:01:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 30 Dec 2025 17:01:39 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 17:01:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 30 Dec 2025 17:01:39 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Dec 2025 17:01:39 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 30 Dec 2025 17:01:39 GMT
CMD ["php-fpm"]
# Fri, 02 Jan 2026 23:44:06 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 02 Jan 2026 23:44:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Jan 2026 23:44:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 23:44:44 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Fri, 02 Jan 2026 23:44:44 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 02 Jan 2026 23:44:44 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Fri, 02 Jan 2026 23:44:44 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 02 Jan 2026 23:44:45 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 02 Jan 2026 23:44:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jan 2026 23:44:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 02 Jan 2026 23:44:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 02 Jan 2026 23:45:01 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 23:45:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 02 Jan 2026 23:45:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8f57655a18e58caec8202718b81878a0a323ee7dc860ee03487665b00f17d4`  
		Last Modified: Tue, 30 Dec 2025 16:39:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8947d9b26fd5842181dbfa0476ae87283eb4ee0896468eef4401a617eae0fb`  
		Last Modified: Tue, 30 Dec 2025 16:39:26 GMT  
		Size: 109.6 MB (109598066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0082faf6428f6d353e1b13563b033f41260118184f280753196d05c13071880e`  
		Last Modified: Tue, 30 Dec 2025 16:39:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55cafe52ac205a8b5b22fb04dab26f35670d56cddad804a83099df49a18b66c`  
		Last Modified: Tue, 30 Dec 2025 17:02:12 GMT  
		Size: 12.7 MB (12748979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8849000939f3c369d116172733cc774f8a0253c6b3993558eb0991114a326c8d`  
		Last Modified: Tue, 30 Dec 2025 17:02:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f9672e754be972d9b3d1d5ae6473af76c4e10026acef3a7819af1433a95126`  
		Last Modified: Tue, 30 Dec 2025 17:02:15 GMT  
		Size: 12.4 MB (12437919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8774c6982db9ae04e6fe9185284f1ed1ae3389061a055414444f21f5ea2466ba`  
		Last Modified: Tue, 30 Dec 2025 17:02:11 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b2400f618628039e516ef28f5ddd3bfc331b0e667998a39e9021044c1e65b5`  
		Last Modified: Tue, 30 Dec 2025 17:52:44 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cc958aa592862f7f5caf3d37bcbfd74abf88f60afe8e8cdbaee828f3ba6df0`  
		Last Modified: Tue, 30 Dec 2025 17:02:11 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa03437d3a02070437cd155f47b5d10b14a5374113f8ca925a30edba5142d2a`  
		Last Modified: Tue, 30 Dec 2025 17:02:11 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55955c3651418333f0817a1990b96f71b09119751d19f70be898eac06fb1dd5`  
		Last Modified: Fri, 02 Jan 2026 23:45:22 GMT  
		Size: 1.2 MB (1244890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e57c3ea0094c862aaadd03e6e6d5bab1645f9e107873d18e21f55157eda4f68`  
		Last Modified: Fri, 02 Jan 2026 23:45:22 GMT  
		Size: 476.8 KB (476818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16aaf88d7c17d529f2ac3f7ac0deb49e14758f3174a8d487c5c1281f35c027d1`  
		Last Modified: Fri, 02 Jan 2026 23:45:22 GMT  
		Size: 2.6 MB (2602185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffa7612ca32e82182cca228fae94ba4f6be4440bd55d8231a239f2912c65b59`  
		Last Modified: Fri, 02 Jan 2026 23:45:21 GMT  
		Size: 1.7 KB (1656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3e15052c94540b48bdadef0c34c8fe602da5d3b724d9a846c0a6eb55117f7b`  
		Last Modified: Fri, 02 Jan 2026 23:45:22 GMT  
		Size: 776.4 KB (776365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6047840f642f3a7ce1a9d3744520080a0900a7f5feb710f8a4ea5713c2fb681f`  
		Last Modified: Fri, 02 Jan 2026 23:45:26 GMT  
		Size: 23.4 MB (23382768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:13aac2ac401fcd37f2030604cc1a47342c166e7a7f03708da7cbba8eee9d676a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67a109d905cd105d563944c38e5b1db6ac8d4f76da567281bd040cadaac6331c`

```dockerfile
```

-	Layers:
	-	`sha256:277ca5d15c3187d1bd8dc9aec760b743c1ccb51e1f9190e26871be9c1b6ee6c8`  
		Last Modified: Sat, 03 Jan 2026 00:12:43 GMT  
		Size: 39.6 KB (39575 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm` - linux; riscv64

```console
$ docker pull postfixadmin@sha256:60c39d85fef976fbf93eba6a8572e22656003c30097cca6d0d3f39b2ea5af0c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227534751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c728201595b9e080f9768cded93e2a0f29a7523482d89f8e37a6851084d622`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 08:15:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 30 Dec 2025 08:17:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 30 Dec 2025 08:17:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 30 Dec 2025 08:17:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 30 Dec 2025 08:17:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 30 Dec 2025 08:17:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_VERSION=8.3.29
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Tue, 30 Dec 2025 08:17:35 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Tue, 30 Dec 2025 16:24:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 30 Dec 2025 16:24:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 18:31:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 30 Dec 2025 18:31:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 30 Dec 2025 18:31:54 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 30 Dec 2025 18:31:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 30 Dec 2025 18:31:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 30 Dec 2025 18:31:55 GMT
WORKDIR /var/www/html
# Tue, 30 Dec 2025 18:31:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 30 Dec 2025 18:31:55 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Dec 2025 18:31:55 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 30 Dec 2025 18:31:55 GMT
CMD ["php-fpm"]
# Thu, 01 Jan 2026 23:13:43 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 01 Jan 2026 23:13:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 01 Jan 2026 23:17:47 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 23:17:47 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Thu, 01 Jan 2026 23:17:47 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Thu, 01 Jan 2026 23:17:47 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Thu, 01 Jan 2026 23:17:47 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Thu, 01 Jan 2026 23:17:49 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Thu, 01 Jan 2026 23:17:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 01 Jan 2026 23:17:49 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 01 Jan 2026 23:17:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 01 Jan 2026 23:19:05 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Thu, 01 Jan 2026 23:19:05 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 01 Jan 2026 23:19:05 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a44b1edad4acbdf2eb79bc4ed79ff402d6af38c94857a826c4e8f406f68b8b4`  
		Last Modified: Tue, 30 Dec 2025 09:22:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43a8c50b15f754f42cc587a4d423f958f4de65b8cc8da75adfbac833ca87e54`  
		Last Modified: Tue, 30 Dec 2025 11:32:37 GMT  
		Size: 146.6 MB (146578538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4346525b0d45631b779c99bb99caa2632c2822ec686a160c5f4d23f9cfac4217`  
		Last Modified: Tue, 30 Dec 2025 09:22:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee18ea173c5c5c6c9d55d60606ccc2c666bd742a0bfb4960873bb2e4dbcafa7`  
		Last Modified: Tue, 30 Dec 2025 18:35:04 GMT  
		Size: 12.8 MB (12764103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f1ef83fc744884472718d56538d0b64b61d15bbe8ea1eeb9ad097e8d9fc59f`  
		Last Modified: Tue, 30 Dec 2025 18:34:59 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461a4b551a343a39a0b2a023efe9a67f5f45d7e47ca7c663d78feed3b09230d1`  
		Last Modified: Tue, 30 Dec 2025 18:35:01 GMT  
		Size: 11.5 MB (11467654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebc7eb814238ee4ab75b90938a361cbe8dff404e4a1ab4fb792478727f8aeab`  
		Last Modified: Tue, 30 Dec 2025 18:34:59 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3e66753effcba44cb202465ae6c1b51282949ef5efc010151bb01f28ae35f3`  
		Last Modified: Tue, 30 Dec 2025 18:34:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db2e3596c89a7e2cf845d48a7cc8b915c14e11317097cf671bf40b2a9f7cd85`  
		Last Modified: Tue, 30 Dec 2025 18:34:59 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbfbbe5168ab0c2eb8da9c82a09fdee2d96e7041e7ff63aa3a796dc8023aa5b`  
		Last Modified: Tue, 30 Dec 2025 18:34:59 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f51acdf21f666192f974e8a4b316e550149eef9c07caa077fb89376064908fb`  
		Last Modified: Thu, 01 Jan 2026 23:20:33 GMT  
		Size: 1.2 MB (1242041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bc03f92c8b92533e9c4558b4ad28e7008368e0dbff318813a5c024cca9a39f`  
		Last Modified: Thu, 01 Jan 2026 23:20:33 GMT  
		Size: 431.7 KB (431741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80a2aa80338be84ec41347ccc7da3b8f5f44028235eed74fc55813a640c046e`  
		Last Modified: Thu, 01 Jan 2026 23:20:33 GMT  
		Size: 2.6 MB (2602192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fbbed7c4226ac178cc69db9d85274acb5b900b16a2dc7b05fddda80312737ca`  
		Last Modified: Thu, 01 Jan 2026 23:20:33 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8dea6674669d5d0e56e079a4e2b8af6b7e444fd4f7f201c08639b5be29334c`  
		Last Modified: Thu, 01 Jan 2026 23:20:33 GMT  
		Size: 778.0 KB (777999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fdef994c2839b611eb77b5dc842f001741dffb4c66d2aa665802dee64c761ad`  
		Last Modified: Thu, 01 Jan 2026 23:20:36 GMT  
		Size: 23.4 MB (23382604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:f8c1366de026e70d59a37ba5aef8a30c3ea1e6d2a4ff6e993f89d81f9208f8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 KB (39575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:445da9a9d0cdfcbd12d73e154494087a2b3abd701e61c061cad493ffea57ee7b`

```dockerfile
```

-	Layers:
	-	`sha256:1a74098287b767e8116e5d549bd0662ebca2728dbe823b297fe8d9de874a0d58`  
		Last Modified: Fri, 02 Jan 2026 00:10:43 GMT  
		Size: 39.6 KB (39575 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm` - linux; s390x

```console
$ docker pull postfixadmin@sha256:9ce1748446e89b12f78d1e72e023cf541ea8218f8325225d117f29a0d5c89458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175426701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d668c76eb42fd72b79a340e9cca626b60fbad28fdc20a2ed11579eb773f5af`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Mon, 29 Dec 2025 23:20:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 29 Dec 2025 23:20:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 29 Dec 2025 23:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 29 Dec 2025 23:20:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 29 Dec 2025 23:20:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 29 Dec 2025 23:20:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:20:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 29 Dec 2025 23:20:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 29 Dec 2025 23:20:14 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 29 Dec 2025 23:20:14 GMT
ENV PHP_VERSION=8.3.29
# Mon, 29 Dec 2025 23:20:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.29.tar.xz.asc
# Mon, 29 Dec 2025 23:20:14 GMT
ENV PHP_SHA256=f7950ca034b15a78f5de9f1b22f4d9bad1dd497114d175cb1672a4ca78077af5
# Mon, 29 Dec 2025 23:41:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Mon, 29 Dec 2025 23:41:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:44:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 29 Dec 2025 23:44:53 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 29 Dec 2025 23:44:53 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 29 Dec 2025 23:44:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 29 Dec 2025 23:44:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 29 Dec 2025 23:44:53 GMT
WORKDIR /var/www/html
# Mon, 29 Dec 2025 23:44:53 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 29 Dec 2025 23:44:53 GMT
STOPSIGNAL SIGQUIT
# Mon, 29 Dec 2025 23:44:53 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 29 Dec 2025 23:44:53 GMT
CMD ["php-fpm"]
# Fri, 02 Jan 2026 22:49:48 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 02 Jan 2026 22:49:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		gosu 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 02 Jan 2026 22:50:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libpq-dev 		libsqlite3-dev 	; 	docker-php-ext-install -j "$(nproc)" 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 22:50:08 GMT
ARG POSTFIXADMIN_VERSION=4.0.1
# Fri, 02 Jan 2026 22:50:08 GMT
ARG POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 02 Jan 2026 22:50:08 GMT
ENV POSTFIXADMIN_VERSION=4.0.1
# Fri, 02 Jan 2026 22:50:08 GMT
ENV POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
# Fri, 02 Jan 2026 22:50:08 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/v${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 02 Jan 2026 22:50:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 02 Jan 2026 22:50:08 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 02 Jan 2026 22:50:08 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 02 Jan 2026 22:50:17 GMT
# ARGS: POSTFIXADMIN_VERSION=4.0.1 POSTFIXADMIN_SHA512=88be6834257580c7a52dce33ce552e1868a1b28ba639a3378a66278939640073af4f8893fbfac690e2df5e67db0143c5726aab575bf0e4014b39a03d46916831
RUN set -eux; 	composerDeps=" 		unzip 	"; 	apt-get update; 	apt-get install -y --no-install-recommends $composerDeps; 		export COMPOSER_HOME="$(mktemp -d)"; 	composer install --ignore-platform-req=ext-mysqli --no-dev --no-interaction --working-dir /usr/src/postfixadmin; 	rm -rf "$COMPOSER_HOME"; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $composerDeps; 	apt-get dist-clean # buildkit
# Fri, 02 Jan 2026 22:50:17 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 02 Jan 2026 22:50:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef34cd33906b4e4d8a4e27681bb0df8433a46a78ec86fe6d78d47fd04f4fb78c`  
		Last Modified: Mon, 29 Dec 2025 23:23:51 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5ffddb206f617060b180d3b9744cda1b79b0b7b5fb203e9e3e1d7d9c2a8d45`  
		Last Modified: Mon, 29 Dec 2025 23:23:57 GMT  
		Size: 92.6 MB (92564912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26919535fcd0454eb2f96d2316d6f0f13f070dd1aa1989067eeccd258ff913c`  
		Last Modified: Mon, 29 Dec 2025 23:23:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fc51f0613b5f12e448f4a6321149cd1b8f13f68ab129eea2bdc2f3c6af9c724`  
		Last Modified: Mon, 29 Dec 2025 23:45:15 GMT  
		Size: 12.7 MB (12748155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:836dfc85be05404b313c8cc122621c5024817cfc95334f2b448824302f90082d`  
		Last Modified: Mon, 29 Dec 2025 23:45:13 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e57c8844a9227b9ccf3893e4f17b168d41fcd99f91d2da5970edb0337c46114`  
		Last Modified: Mon, 29 Dec 2025 23:45:14 GMT  
		Size: 11.8 MB (11769705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8092cb0cac57485bc70a7845441427febee042d6af05a840a0df00a2bab5b6e`  
		Last Modified: Mon, 29 Dec 2025 23:45:14 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb0abea18a5ebd4a0d42b33507856b5bdf0deaf7b9ec6dbca4d990854c15a61`  
		Last Modified: Mon, 29 Dec 2025 23:45:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd073168f106ba854f428895a00a9e4b4da87a1ea1470ac09aa17f02d3121761`  
		Last Modified: Mon, 29 Dec 2025 23:45:13 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ba8deb8d8fc0b9678dbc077d3d4f42a306cceba78b72b60ebccfe47841171d`  
		Last Modified: Mon, 29 Dec 2025 23:45:14 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93984b47073e43fc553d30749efc73511827ec52c6d9ad28f402a4ab51beb7d`  
		Last Modified: Fri, 02 Jan 2026 22:50:32 GMT  
		Size: 1.3 MB (1284048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab4db948be3e4e7296c8e5b7830b8afeb9c3bbb79609ed1bdafd51fe51ade58`  
		Last Modified: Fri, 02 Jan 2026 22:50:32 GMT  
		Size: 450.4 KB (450407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dac6fbdc43694ddba19848969cdb321c1d2ed63e9cd5d9b7f40b1cbe8f8fc1`  
		Last Modified: Fri, 02 Jan 2026 22:50:32 GMT  
		Size: 2.6 MB (2602186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbfc10cc8efabda61bdd6a5e89763511fc61f828484a2be51e5c7e5349b271c`  
		Last Modified: Fri, 02 Jan 2026 22:50:32 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52fb63dd0dcd49a27ff4430585d72452d88a9dff53cbf4916e660becf251df8`  
		Last Modified: Fri, 02 Jan 2026 22:50:32 GMT  
		Size: 776.4 KB (776361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6e2c7a620d29c78ef7d03b1023e2f1419399b3f0229d983602771a74823a0a`  
		Last Modified: Fri, 02 Jan 2026 22:50:34 GMT  
		Size: 23.4 MB (23381759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:fcacf5ca16ef756406b012a6f16fa78f2b6a2cf9dafcabafd2cd6a84656f8bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 KB (39508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33225de373443c985ea64a413f996cd7bbea07ff48d73209ab01814df38a2d0b`

```dockerfile
```

-	Layers:
	-	`sha256:5a5c323261f00df7b59ba2c54bb4e08bd1ca2f2e3e5d2dc9b051ffde9bb3eb54`  
		Last Modified: Sat, 03 Jan 2026 00:12:49 GMT  
		Size: 39.5 KB (39508 bytes)  
		MIME: application/vnd.in-toto+json
