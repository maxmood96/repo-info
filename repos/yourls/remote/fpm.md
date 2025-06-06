## `yourls:fpm`

```console
$ docker pull yourls@sha256:faa315f34be40a82085fb7a223d040c827a34e14065700f10cb627a71d5ed852
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

### `yourls:fpm` - linux; amd64

```console
$ docker pull yourls@sha256:cb87f5fdb59e6c28bfadeddf1a751f898260134dba4781e203d196eb7aa4ca76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.0 MB (183012447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea4133a830e947bfff08ca9b7f0678352c2980a791ab7150aefcbb2720c9a09`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9995a2a127afaef82ccacedfcc1ba00520a4fee1015910b9f8d908b6735280b4`  
		Last Modified: Fri, 06 Jun 2025 17:40:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c33cdd2d809d13987cde67f5bb8ef656cd142ea6b7f530b2c3725391c56596e`  
		Last Modified: Fri, 06 Jun 2025 17:59:50 GMT  
		Size: 104.3 MB (104326420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38c981154410e6f6585ff949e88ea70d76916d8fb50e0ddb2baa0639c11b576`  
		Last Modified: Fri, 06 Jun 2025 17:39:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c433b00b1443e0880f2ec6444d1c5eb49702c0fb83811257ec3698013735fc`  
		Last Modified: Fri, 06 Jun 2025 17:59:40 GMT  
		Size: 13.7 MB (13728773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab215b95663e87d8417031c78b4911da1327f664c245242744e52cdadc5371d`  
		Last Modified: Fri, 06 Jun 2025 17:40:19 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a8dd75d8b5178ba38b16e4f46385269eb19182a742c19b20b04b127926399c`  
		Last Modified: Fri, 06 Jun 2025 17:59:40 GMT  
		Size: 30.3 MB (30284034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e5327f5e84b7671f311f8a6b91b55cfcadfd6f03326b8f2e751bf41a96881a`  
		Last Modified: Fri, 06 Jun 2025 17:59:38 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dffffba5b2c19e3b2c0503d453738c14934cf33018cc534a0913593aec5fe4`  
		Last Modified: Fri, 06 Jun 2025 17:59:38 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf181289527361f1672a3841ea69bef541545016c2fb8f89b4b6419ba38a228`  
		Last Modified: Fri, 06 Jun 2025 17:59:38 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0aaa8314b68050626f52f48f6b8aa45187095181a1cb69b6e6eccc459c328d`  
		Last Modified: Fri, 06 Jun 2025 18:01:11 GMT  
		Size: 663.3 KB (663325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422cc300cb9a328719f1896bc69a443a87efc5b53678fec18d9f678836c06237`  
		Last Modified: Fri, 06 Jun 2025 18:01:12 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b258009723d7d3285fa8837afec360ad29282abd870ca26a138ad8909fc4cf7d`  
		Last Modified: Fri, 06 Jun 2025 18:01:13 GMT  
		Size: 5.8 MB (5767590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca53fe3a84ebd4d8c3f103e37aef74458d26ced6b1a4f9959254b0bc3cae5702`  
		Last Modified: Fri, 06 Jun 2025 18:01:12 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d951c013877a8b99d129c363bc0e33cdae654b7eb1a3062109d4a1ece1926c5c`  
		Last Modified: Fri, 06 Jun 2025 18:01:13 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:5727a2df4e3f08ffea5d417a1219d01cf33451e51bcd35de83639c8a85e08b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c049fee1a67a7ccc5380518bd6f78f9d1a8dcfb263f3ceb5e902150d52b4271`

```dockerfile
```

-	Layers:
	-	`sha256:39f0f011c992a095d04c10f7f6850b61538412b1c9e52d02d2d647b1ca9d7297`  
		Last Modified: Fri, 06 Jun 2025 19:42:56 GMT  
		Size: 26.5 KB (26451 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; arm variant v5

```console
$ docker pull yourls@sha256:dadc89f4402140ea1587831566b981ce3a4b9d24d79401b2a62bef676adfe7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155969469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aff0fdea857f58d6256729abed489278fad1a7e010d7e215a6cebd478b18cee`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a630a0ae6a7caa13c26c641757aedb6f2a685e945563086d454f01db874d5a4e`  
		Last Modified: Tue, 03 Jun 2025 14:06:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c1543f1d03f96cc1c05ba7756b5950bbb8edfd3038bc0902f7bd06c8b3a5a6`  
		Last Modified: Tue, 03 Jun 2025 14:07:15 GMT  
		Size: 82.0 MB (81970289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b1f2e7aca197ce584722af1cb59310256391ea143b4eee91fe64249d0f64ac8`  
		Last Modified: Tue, 03 Jun 2025 14:06:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef36e25949ffd2b1230e0e24f74da29908558fae134626a5cfeb2f39683c3efc`  
		Last Modified: Fri, 06 Jun 2025 19:43:50 GMT  
		Size: 13.7 MB (13726913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e773962fd25adac4aea6451fd4c58bd0da4846356d19167f1c4535b177e189f3`  
		Last Modified: Fri, 06 Jun 2025 17:49:57 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92dc74955633d73e14cdd2ce726c77aa11a82fde113037c5e0f9e41dbc88b6ed`  
		Last Modified: Fri, 06 Jun 2025 17:53:07 GMT  
		Size: 28.6 MB (28557342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a79c1f49b8aca393f6ef217e7faee6f79e0a14324ce687bba35386226e372a1`  
		Last Modified: Fri, 06 Jun 2025 17:52:58 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33fc0dadf8183342e79c54c15cb61f776b3948192eb888a638160d0ba145afbc`  
		Last Modified: Fri, 06 Jun 2025 17:52:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ad81a561185bd9c768f487bcea8aa21ef6b21cbb059481842f71c2c25149a0`  
		Last Modified: Fri, 06 Jun 2025 17:52:59 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9495fa39b2445f4c373c0d134939894568c492a542d3e5c4f73da6e128a6cacb`  
		Last Modified: Fri, 06 Jun 2025 18:27:09 GMT  
		Size: 173.5 KB (173463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619006e6ff0df3cf45c1bae5df0609b26e422ca77b54666b2ac057c868b23b68`  
		Last Modified: Fri, 06 Jun 2025 18:27:09 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93003e5bfc511cb5138709fa5178e5e3ffec0ed660b90eb2d8f523373a818278`  
		Last Modified: Fri, 06 Jun 2025 18:27:10 GMT  
		Size: 5.8 MB (5767590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e1ee9258a374a0b8977e527225e683d62f3b2bcd4525671d91a0b805ca76a9`  
		Last Modified: Fri, 06 Jun 2025 18:27:10 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0965ca335bce479c25532b1be6a1b5af9b6b5dd4b211d077fcdf9db2af92fc6c`  
		Last Modified: Fri, 06 Jun 2025 18:27:11 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:bb626182a90baf2b80e8f9d1ebcf1d0a50f46b39c9a32414f4f5c0163cc048f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aad2f72d84e40ff21801867f45445c4fb6bc9bf479fc72655bff11f9f6b747c`

```dockerfile
```

-	Layers:
	-	`sha256:390a615e67ca98983ea31094a271c3d9d6d4f5a8969ccc5243e582818d0abe91`  
		Last Modified: Fri, 06 Jun 2025 19:43:00 GMT  
		Size: 26.5 KB (26547 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; arm variant v7

```console
$ docker pull yourls@sha256:8da4a15d05243b75d71bf0e404b7a34e9b33991fe9f84576c9484b24daf5c83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147322513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f29e770c58b9e4176494e18e985f2bb4c56c175ef00027247e37b350c6f9f2a`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67b0d6d3f419936777d490c71b48fd196b853be826a3cbe2a99f87ce45962a8`  
		Last Modified: Tue, 03 Jun 2025 13:33:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b3dbe5e2b037219e6a37b411897a539f579592c7d55f751f30cdcfee2dafdd`  
		Last Modified: Tue, 03 Jun 2025 13:33:29 GMT  
		Size: 76.1 MB (76132659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56653e4c243acfc3e7a605794bbf2267c510182bd9d2f39f4bcf6a23263375bd`  
		Last Modified: Tue, 03 Jun 2025 13:33:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4beb472b6f6bd355601f75aff4368d8d9591b7fb987c13e9031b77b1d527cd3b`  
		Last Modified: Tue, 03 Jun 2025 19:07:11 GMT  
		Size: 13.7 MB (13725108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253535f6c244259b6239ebf7d98238a48246d6f147c36fb0aa07a1bac88bc745`  
		Last Modified: Tue, 03 Jun 2025 19:07:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5302c25e3ce6e3576ab961f94e55487178e15268bee9e694e8c8228f677f8f8e`  
		Last Modified: Wed, 04 Jun 2025 20:46:06 GMT  
		Size: 27.6 MB (27588253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b99f57aa75fc6e91cdf72aa8edfd2558d4a554b833b467387953ebca2c4d053`  
		Last Modified: Wed, 04 Jun 2025 20:46:03 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c931ab8bb0ef4ac7a3db625d4c694453cf602f1bccb9a39a64bdd0dbbd9f09e1`  
		Last Modified: Wed, 04 Jun 2025 20:46:03 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb5684d5a4098836bbcf0102f9a59981f7ec97ca24e1984c84da0606ce2d308`  
		Last Modified: Wed, 04 Jun 2025 20:46:02 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec95f99ac6332ba6728e1e1bc400785fcbf509d8e9a1ba0901b11a276996434`  
		Last Modified: Thu, 22 May 2025 12:10:26 GMT  
		Size: 159.0 KB (159015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef17fc5a61d17cd0f3f95ae9a4c965e73ed8bdf28c37e87a220b847f22287a1d`  
		Last Modified: Thu, 22 May 2025 12:10:26 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ccb377b49377926954a8392e31db97dbbbeb29f534f60395ec2318b35edff1`  
		Last Modified: Thu, 22 May 2025 12:10:27 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f318347cb76a11ae815795bc783b8cfb35ad9bbf09b5c9b1e49d2fc7c8813cd5`  
		Last Modified: Thu, 22 May 2025 12:10:26 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76abaadc727db856d624f3784137d20b3914790b5aa9904fa1a4b60dae229621`  
		Last Modified: Thu, 22 May 2025 12:10:27 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:43f79695685b6d334dfc97e25c25b9959edd96cb67dbeec1a73d9bea622dc772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e88ad14497a305fbc2cebeef73f507def7627c143c7a2ab93d186cb32ea62a90`

```dockerfile
```

-	Layers:
	-	`sha256:ecc759481c993f83505b03377f4672a3271efc67b512cfdccc9d10f6f083be31`  
		Last Modified: Fri, 06 Jun 2025 19:43:04 GMT  
		Size: 26.5 KB (26547 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:ef708552140e607c78597cc9294a6eb640a8f448be54677dc6f98110bcec3047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176162847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc31c3732ca1e768210e1d47b0e0c3317e72f558b2e5cbd498ae4f488ea7a7d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2162264c942aa762db417d45ba0a061dc8a07fdceff32a29a2d59afdc5dce9f9`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ae464486e7a7b754207a11225be678aa24148395332f33c785867c1ee4adcd`  
		Last Modified: Tue, 03 Jun 2025 13:30:28 GMT  
		Size: 98.1 MB (98128413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa473689d317e799934b0b99abeaba5a91da4380c0b6148373000ed23bde9ba2`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842847345e9b4932e1fe464d8d894ccfdf7169b798f2999a102c60f8b75ae1d4`  
		Last Modified: Tue, 03 Jun 2025 13:35:14 GMT  
		Size: 13.7 MB (13726692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d562fab2492856a79204ff3463cd59b09b7cc622930f89f9e3938590cf4893b`  
		Last Modified: Tue, 03 Jun 2025 13:35:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00867262a96ba1ea9f52cc0248ad3f151139214e5d78b4ad899af5e0eaf0e9c5`  
		Last Modified: Tue, 03 Jun 2025 13:34:44 GMT  
		Size: 29.9 MB (29881951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd65751c3a81ece3247d0282921d12dd2b328610729c960cd3be34954505f3d`  
		Last Modified: Tue, 03 Jun 2025 13:34:46 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d66b7c77777afdf18efd08dc2d5e7b358634e92293be0da688d152f2c147f1`  
		Last Modified: Tue, 03 Jun 2025 13:34:48 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3b49e798392e277c29db2be11b886ae04fb5e311184a151133e1a1f9fd487`  
		Last Modified: Tue, 03 Jun 2025 13:34:51 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35712dbe25c6d6b213c3b00ffe8a198f91c8e252e4eaa7238a743d94b5010219`  
		Last Modified: Thu, 22 May 2025 09:14:22 GMT  
		Size: 575.9 KB (575940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67290ad7ecb70eaabaf86c7e1842842cea49607b6d86f883a4faf04f045d1111`  
		Last Modified: Thu, 22 May 2025 09:14:21 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05f5cef9991c938e52c30ee551a5c2051e0be06f7e1a1ca899d5b2bde676b22`  
		Last Modified: Thu, 22 May 2025 09:14:22 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99695b0df0a96f34175dc6352d7dd1bbd6cfc6103df9e02208d974bb3bf93293`  
		Last Modified: Thu, 22 May 2025 09:14:21 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e304e49c09f8ba4b8163de6748d860b121c453b5f4cc3b718de81501142ce8`  
		Last Modified: Thu, 22 May 2025 09:14:22 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:ae92d76a9f69c9812aceb06694ad160aeb5b168ab7d9a953765bc017ecfabb08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73984e367bca9eeb192f21ce7f502328c98b3ab77749189cef4a026a192a6422`

```dockerfile
```

-	Layers:
	-	`sha256:d1384aa96ee91d939a311c640c6e2bfb899f6031a4fd0162e3fa8943549739e1`  
		Last Modified: Fri, 06 Jun 2025 19:43:09 GMT  
		Size: 26.6 KB (26579 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; 386

```console
$ docker pull yourls@sha256:4ad5a76053ec77e0655c04e4af8336449bc3b7d71ba01001b329a184e6dc8a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181779133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e058b29b4723e0257ef23df5cb5d54d958011f4feae704311363179c1b27ea`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586cfc240d7c44440f95b7e9239643e5b3b3e01e797f249b1ad9f68bff81b7da`  
		Last Modified: Wed, 04 Jun 2025 13:47:50 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36001a84760dd75464eb6c06e29dcf81b5ee27ba2802a7c51fdb392c33bc0fd9`  
		Last Modified: Wed, 04 Jun 2025 13:47:57 GMT  
		Size: 101.5 MB (101507465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d4e3f77f0f71c2a5d36f6c409299ee15bbd9e7a6a6cd747fb09de300a139cc`  
		Last Modified: Wed, 04 Jun 2025 13:47:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64464e784fe6dc4d93b1646de994f2255e417cf1d57bf06e085ec14a70779f15`  
		Last Modified: Wed, 04 Jun 2025 13:48:01 GMT  
		Size: 13.7 MB (13726110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d5b3489bddec921d974b72251b4ac1b0698f335f4ec22db754fc86b478aad8`  
		Last Modified: Wed, 04 Jun 2025 13:48:02 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79a71162551aa51ecdcd63b57f281b05a1bba17bb549bdd6973a9236ad353cc7`  
		Last Modified: Wed, 04 Jun 2025 13:48:05 GMT  
		Size: 30.9 MB (30867397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20792761053bda608d9e6ddad1180b9aa8b33caee015c94a2434514b5c6a4eaa`  
		Last Modified: Wed, 04 Jun 2025 13:48:06 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dd2cfd2d76dade18c3655865c5a0dab9cf16cc2fd26745bef2ea548f9f9849`  
		Last Modified: Wed, 04 Jun 2025 13:48:08 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bab9f600769f739c83a83f706f380ebf34d8a33d1d315316201b6d8421702c`  
		Last Modified: Wed, 04 Jun 2025 13:48:09 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c7df9b7ec547a0e501a295319ec7976f5234be8e942e206d443641cde6b2e0`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 686.1 KB (686110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9df52a4c09ad40b77fd36aaea0db0d3174ef5853edfe64c34dc32f7105316d`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211b64d1327bde6fd14c9e1a0cb15f2c6ab37cd21c8772b02262dcd63b67a84b`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3758f7c061755ce168d8803dc6503cbf5614b155ef79ba8b9b168d99db96203`  
		Last Modified: Wed, 21 May 2025 23:37:26 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a6203aea737a8abb0f8f1a74fda267f0b2845f8b7c24640ff5803694e9362`  
		Last Modified: Wed, 21 May 2025 23:37:27 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:1bddd3f9709bf8251f2fe8f8a2e1e30e41675fcd9183c94d688a239037745d44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26949a0fddfb45104dd3cbc1a971fdb602c34e477c12daf3233f2d67b51fd88`

```dockerfile
```

-	Layers:
	-	`sha256:e46d14c9f47cbe3f39e09282f506cbbfce421429c684b037e19200ebc5741483`  
		Last Modified: Fri, 06 Jun 2025 19:43:13 GMT  
		Size: 26.4 KB (26415 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; mips64le

```console
$ docker pull yourls@sha256:11e6f03bfc5db8c58025dd8be2551cb917fb88e1c58bbd293289118bcb29da21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158069311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40a6cfb74a61711ab33331f3821836b314747b6b98f7372fcc91714a4d9df13d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4b2d065c1ae51e1de38627f7944c17a1a577f385d527b6bf91b589844d0689`  
		Last Modified: Tue, 03 Jun 2025 14:07:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5af86f1704d74588bed3a81502d5b84aaa58ec860f5145be4f0fd74e864385c`  
		Last Modified: Tue, 03 Jun 2025 14:07:31 GMT  
		Size: 80.7 MB (80670380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5286f15cd07eee9997888e6110e809261f661823a9bcc233812db970c553fb13`  
		Last Modified: Tue, 03 Jun 2025 14:07:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b7193b80ea6b70dcca18896d036acb8d83e8c98d6251421318c32ca8e89c9e`  
		Last Modified: Wed, 04 Jun 2025 07:07:12 GMT  
		Size: 13.7 MB (13724845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199ee207781a2543a183297951766ee2805c26018fb0b9bdcef7242f42283d13`  
		Last Modified: Wed, 04 Jun 2025 07:07:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b67bc23ec30eae2830e849a66423e52e8e6aac78b3fc2f531a30789036dcffb`  
		Last Modified: Thu, 05 Jun 2025 13:42:48 GMT  
		Size: 29.2 MB (29207845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92763c324104fb79565e69f4e33b0a44e10bf4442b2429b7246b80f566899615`  
		Last Modified: Thu, 05 Jun 2025 13:42:42 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ea33fbe742a25e65aaa9d645688363a147b9cdaf5ff6ba0a1a9ae14556217f`  
		Last Modified: Thu, 05 Jun 2025 13:42:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b9419548cd054c78428b17a25802a8ad34d65b4ffb839267b16734cc661412b`  
		Last Modified: Thu, 05 Jun 2025 13:42:45 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2bda51f77a74d1f1c768c722ec2664d66b0b8b045797bad16a0cdd0a1d16d2`  
		Last Modified: Thu, 22 May 2025 14:26:09 GMT  
		Size: 169.8 KB (169822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9e07a182b5f9c8a595f15ebcb8deadff0ddda8b579001dbf0a33ce1a33448f`  
		Last Modified: Thu, 22 May 2025 14:26:09 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cc2c23d73bc86b7bb53f96f2294605c53b3f30193444deeba7f758c05090ea`  
		Last Modified: Thu, 22 May 2025 14:26:10 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb1e1ca98f37699e1619ff8d7d6e34a44b34e46e58255989e0b519eded89f9d`  
		Last Modified: Thu, 22 May 2025 14:26:09 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2a4f5741a354aea9c3fbc52f8c8cf6171c6e70ebad63737406ee0a062520f1`  
		Last Modified: Thu, 22 May 2025 14:26:10 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:ef0309b6fec6960359332e6d088faaecb7cfbf964eb5c103e9443d7801088de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22d6ae674b8829ed3cb82d2f0e2bd3ae2d4e8ed1b48bccab0baceb1a0aad9739`

```dockerfile
```

-	Layers:
	-	`sha256:094db0c392047b8bc6c28bcbeafa6fcb8a050c0b5640ce03ddbbc572d0999bba`  
		Last Modified: Fri, 06 Jun 2025 19:43:18 GMT  
		Size: 26.5 KB (26517 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; ppc64le

```console
$ docker pull yourls@sha256:9af985fa21fde4b3c08eab412c53517619c4b08771bd5e1ce8fffd8a5af1b0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186460930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d01cfd68f4eff8a7968b28339e95760f27bc72c94e1c9b561ba7c6b1d06174da`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.7
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c8f6558609f4eda938f055dbc23ff092be663afb6bb7d22397dead0d155e4`  
		Last Modified: Tue, 03 Jun 2025 14:07:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b95a24f0f53c73df78df26adee8011626da1dd6f4150d1531843c39f2fa7279`  
		Last Modified: Tue, 03 Jun 2025 14:07:40 GMT  
		Size: 103.3 MB (103318542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbbd3cd9d8dd0b29377d19251990f04906ba83ff91eb897513badc4d334a010`  
		Last Modified: Tue, 03 Jun 2025 14:07:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1101d3d522f7624cc7597b7919ae55b7aade67df6347e223106e8e03be32e72`  
		Last Modified: Wed, 04 Jun 2025 07:07:10 GMT  
		Size: 13.7 MB (13726428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83139f4176b1ea384f6fa21d39f2f4bd192c916da1b4e15ea3f023ce10da046`  
		Last Modified: Wed, 04 Jun 2025 07:07:07 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d857ea4e61be5a3faf5cba82c2e860aa5b2ab3332e326722c5740bc6d8238e`  
		Last Modified: Thu, 05 Jun 2025 01:10:43 GMT  
		Size: 31.4 MB (31354216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedb4798c33cbecb8144c56fe6690e7687c28a72c9b96a74a0c5d5e9d1269221`  
		Last Modified: Thu, 05 Jun 2025 01:10:39 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a0e121976b89d08096db226f2a169811952743952e21131b289b74720c32ce`  
		Last Modified: Thu, 05 Jun 2025 01:10:39 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97805b9d4c7a7eecb20296f0350226f922ec9692de654853d25fc08504dd66a7`  
		Last Modified: Thu, 05 Jun 2025 01:10:40 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26736a921868c9e589de79041b99ad92e8192a31b368baf4593998cf83256a47`  
		Last Modified: Thu, 22 May 2025 16:50:36 GMT  
		Size: 210.3 KB (210274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3407110b6123650b0c946348f113ae95211a01c59d82933328d196142453f142`  
		Last Modified: Thu, 22 May 2025 16:50:35 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f502c5b7bd2e4acfe5690fac74d18bad1c0de397ddcfa49265742dd31c1533`  
		Last Modified: Thu, 22 May 2025 16:50:36 GMT  
		Size: 5.8 MB (5767593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7223416fcb574cad11e22ec9753ee2dc6efc7cb50921ffd3ed464574d3163ff`  
		Last Modified: Thu, 22 May 2025 16:50:36 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8bd52b90f26dd2b7995b4399f4919da34c212be9b8a118620890ec139920cf`  
		Last Modified: Thu, 22 May 2025 16:50:37 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:47a06c4e9510a26897154e84941d8bda847e9f681332daf49cc269b6cc8d1da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945b296a4c3a73674e66dc038f06f6e570d7b744d6298b60b55058295856b9a4`

```dockerfile
```

-	Layers:
	-	`sha256:074c27dc2e9b4c8f8a9ce2119f666e8f096fd1d44a686b2d31d7ca8fe46d8d23`  
		Last Modified: Fri, 06 Jun 2025 19:43:22 GMT  
		Size: 26.5 KB (26499 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; s390x

```console
$ docker pull yourls@sha256:42751a06f7a50360c327bb601880275cfe7860566021003cc422c63135a90d58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156941179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f9f37ec59ba0fc05e453e705fdb84829b1a06302574a7090a0b4c85343035a`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 25 Apr 2025 02:48:28 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Apr 2025 02:48:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_VERSION=8.4.8
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.8.tar.xz.asc
# Fri, 25 Apr 2025 02:48:28 GMT
ENV PHP_SHA256=aa6a4d330b47eacd83e351658ba8c47747a1e4356456219cfb6d75e7838da091
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Apr 2025 02:48:28 GMT
WORKDIR /var/www/html
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Apr 2025 02:48:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
# Fri, 25 Apr 2025 02:48:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ARG YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_VERSION=1.10.1
# Fri, 25 Apr 2025 02:48:28 GMT
ENV YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
# Fri, 25 Apr 2025 02:48:28 GMT
# ARGS: YOURLS_VERSION=1.10.1 YOURLS_SHA256=ec21841af21194c8ef06a8eaaea5bf26d329741f9d09e04b32685a2d8ac4027e
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 25 Apr 2025 02:48:28 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Apr 2025 02:48:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65e64042a8c749f17bfb3b660d34f4e07edd06c81899da76f0b866d5592048d`  
		Last Modified: Tue, 03 Jun 2025 14:07:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae504c4e6cef239a74e8e2bc8e65a5adfc4fd86d2ce43efcb6fcf7b948f38c6`  
		Last Modified: Tue, 03 Jun 2025 14:07:59 GMT  
		Size: 80.8 MB (80824650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9845dffb4e53bff01a8cc52346eef48b2a105a195a30ab820e7df1e9682a7a`  
		Last Modified: Tue, 03 Jun 2025 14:07:30 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78b16306317b16185542f8f490a5af4f14d17e2610167a91156f4e35ad04d8d`  
		Last Modified: Fri, 06 Jun 2025 17:38:31 GMT  
		Size: 13.7 MB (13727189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca6f281e4945e81fca63fbdb558071eb2f5d6bb9c648434baf1485dc442327c`  
		Last Modified: Fri, 06 Jun 2025 17:38:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f93c909c42b5c47f45d9efb1b7e350a52a5f50c3de85e1269c20ebe5f97033`  
		Last Modified: Fri, 06 Jun 2025 17:45:11 GMT  
		Size: 29.5 MB (29541995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21014e9347327688053ab130ae16770073b889dd76c223e097451b1984678a30`  
		Last Modified: Fri, 06 Jun 2025 17:45:09 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50817c29c970c777259c8e0bc90a39df0a23ec50e10240cef62afec2c8448193`  
		Last Modified: Fri, 06 Jun 2025 17:45:10 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad09c3fb4efd696ba5a9ddea662a924b2722b0c233f7b57446247101c2bf16b`  
		Last Modified: Fri, 06 Jun 2025 17:45:11 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22af673f1e930af44c91858534cafc3c01522813b86bad89abac399a5169aebe`  
		Last Modified: Fri, 06 Jun 2025 18:52:24 GMT  
		Size: 180.0 KB (179977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d185242d9dc82520c0d0340ce501292b0bbb51cb2f76b346acf1df6980358a`  
		Last Modified: Fri, 06 Jun 2025 18:52:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b5f9eb333228a04a6e39baa387c89811f2a59105d55f88b3d228ab06b158a9`  
		Last Modified: Fri, 06 Jun 2025 18:52:26 GMT  
		Size: 5.8 MB (5767590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94aec7f38f02ec3c49a055fb95b38ba1469f1ed0b0be8a4c6b96799a699e9b14`  
		Last Modified: Fri, 06 Jun 2025 18:52:26 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21e9213eb6a49eaeb6e35a2c8174614ccfaa1f08c0d975f56d7c47d24677d034`  
		Last Modified: Fri, 06 Jun 2025 18:52:26 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:26e85683e76d6fe9ab970ba0312db2a34ffba780cdd734415743d38a5ce84d8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c907adbf34138576611c25d5d5c9e32a25856e6a59f6980fa132e2561e8ccee`

```dockerfile
```

-	Layers:
	-	`sha256:6ced9a32a9265cb7a97264363e2146aa77cd075874e5613d9ea01cb9e6e33e58`  
		Last Modified: Fri, 06 Jun 2025 19:43:26 GMT  
		Size: 26.4 KB (26444 bytes)  
		MIME: application/vnd.in-toto+json
