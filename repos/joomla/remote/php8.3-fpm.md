## `joomla:php8.3-fpm`

```console
$ docker pull joomla@sha256:52161e2b24bdc21713da98eb5c93ae922a899cbd890feca2ba73bc96415a1b8d
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

### `joomla:php8.3-fpm` - linux; amd64

```console
$ docker pull joomla@sha256:b5f408d92cf0afa2e15686be3df754f4cf7d05d20364d986cfa45b3c0418de11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.7 MB (255671091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775506f95296d41cb0d2b0647f95f6f59282217fb5b67c99a28255460fafaeec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.17
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 04:27:59 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a835f7a42d41baddef8cccc9691d2066b05ea324071f6cf142265b0a9c11f9`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5b95319ddc15769ada221761749d9bac6cf478f1b607081d1c4df587ae074a`  
		Last Modified: Fri, 14 Feb 2025 04:09:15 GMT  
		Size: 104.3 MB (104345517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384ebab55c22169d292567399ac1ccb6154a4b7cf24b98d13b73c543592150c1`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa9a36df35da1ec49278b8cbe66658fb83abec98e7f4c8f6062da4661b70672`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 12.7 MB (12650862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4baa754be4b87920fc4ed230c6c0c0a30be6b90e116aa97965c487dfdfbd0e4`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df0e7a23023d4899b4ab528fc2b2b9d5adacaf963a63ccafb2d466a9b94beed`  
		Last Modified: Fri, 14 Feb 2025 04:09:12 GMT  
		Size: 27.8 MB (27828378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b0f7866a10b0eac27c8fa758a35ea7ee93453fd1fad523542da9e75c4f740cd`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96a58be0a76dce6cd69be1cf8bf5d336147c302cf9d0cd65af2b61c29bda299`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e3f6c4b40f7cfb00a7a4a38559daa24397f523bb9d9ccd0a4443d1bfaa7e19`  
		Last Modified: Fri, 14 Feb 2025 04:09:11 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cade6a0756fd966de2a3723dda1cf8f5bea04d732cbaf642e65cd7981900372`  
		Last Modified: Fri, 14 Feb 2025 05:45:08 GMT  
		Size: 27.3 MB (27277956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c26afd26941c422add1419c582c3d818772be08d2a3fc37f2e3d12147a1850`  
		Last Modified: Fri, 14 Feb 2025 05:45:09 GMT  
		Size: 31.4 MB (31442937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b473208035a84f485376ae8b4520ec09cae6ead1c2ed7d59944071a119cf0c1e`  
		Last Modified: Fri, 14 Feb 2025 05:45:07 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a6b090581353dc6e4441f3ecb1b7ccc18bfc19f92c7138295eb76e849c7ea7`  
		Last Modified: Fri, 14 Feb 2025 05:45:08 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b9b59bc4957a262eedbe149aec7eccc0fce1b9f259fc6325553a7fc800cee8c`  
		Last Modified: Fri, 14 Feb 2025 05:45:10 GMT  
		Size: 23.9 MB (23894811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dd632ca28c0a382fa15a49183d5fe81ea6938bf57a13b7e363b3fda15d50457`  
		Last Modified: Fri, 14 Feb 2025 05:45:08 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74e628bc6e8979b4fa9a79ada0a68aad787399312e64afe17def1136ab3a56b`  
		Last Modified: Fri, 14 Feb 2025 05:45:08 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.3-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:01ab0172920a3da3d3f81cdb9f95e994f7eeecca3b18f9cb55bbd700f4a97f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e59451ae39da86a0386efd86bff8fbb55bc3ff77c10e4ba91cdcdf593b56ccd2`

```dockerfile
```

-	Layers:
	-	`sha256:5036c465fbdbb3c68cb861c4ee2e37586631e6cba280f5043ff74817fd5dac5c`  
		Last Modified: Fri, 14 Feb 2025 05:44:44 GMT  
		Size: 47.7 KB (47707 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.3-fpm` - linux; arm variant v5

```console
$ docker pull joomla@sha256:3e0d3257c4b794180ef813a671bc681c045505e5b9485b29c840bfe0fa774e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225428539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1b0228d1ba21607c0f4f5a1b865697059da5bc8653cc9587be648bac575e474`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.17
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:aa8576c673e5a651f7450bee7603a12ac6168051fdd5b2411678987e180cad6e`  
		Last Modified: Tue, 04 Feb 2025 04:33:02 GMT  
		Size: 25.7 MB (25736549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972786f04f039fb3a4d1b82c728a7c7ea9ffc0e85efd517dc45b571b1f62752d`  
		Last Modified: Tue, 04 Feb 2025 09:33:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e43da89859192986d7ea9c98d997ffc5a0763c751bc8a114b8ac40e7013eb3`  
		Last Modified: Tue, 04 Feb 2025 09:33:31 GMT  
		Size: 82.0 MB (81993010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d164497324e1f248e21428931b6af1422a36e02ee93ec9321130fe7aef51ee`  
		Last Modified: Tue, 04 Feb 2025 09:03:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deaff0929467baf1f53140082511964551912792dba5056e8c5d649e866fd57f`  
		Last Modified: Fri, 14 Feb 2025 05:43:13 GMT  
		Size: 12.6 MB (12649172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2677292000654e0de04dbb2188846b1715449deae7a5875e0b019f702207f4a`  
		Last Modified: Fri, 14 Feb 2025 05:08:55 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e82079250b68d7de3d3520991cb8e996aaf80171427799a956e350b36f3139`  
		Last Modified: Fri, 14 Feb 2025 05:43:14 GMT  
		Size: 26.3 MB (26303355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72fe46befcbba153811df3cbdba887eb4f8aa7ce16dcd036b37f4818d1cccef9`  
		Last Modified: Fri, 14 Feb 2025 05:08:57 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8276bdd144b14027ecb00a31e443b19a7a99f2a463c02a9fd3478c054a42cf`  
		Last Modified: Fri, 14 Feb 2025 05:43:13 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95fe499a81773d82cc6cfd8323e32c6652e61c63ffe7dce0ecb9675de85683a5`  
		Last Modified: Fri, 14 Feb 2025 05:43:14 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f5ec8a0fb718998d4d472e2730e5bcc759104addb05cc5c18b8226bad18ce1`  
		Last Modified: Fri, 14 Feb 2025 05:45:05 GMT  
		Size: 26.7 MB (26705186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2b89952cda63b87036187a65cdd71f768c61813d7bc6fcf0381e4450b644fa`  
		Last Modified: Fri, 14 Feb 2025 05:45:06 GMT  
		Size: 28.1 MB (28128089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f09dba306d72de9499fd2f71ef6f7824f23e03b36cc88351a21c8f5fe2936dbe`  
		Last Modified: Fri, 14 Feb 2025 05:45:03 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21065cc8d4e619900548412c734507ab942cbb4aebe1186f3a81ede60101437f`  
		Last Modified: Fri, 14 Feb 2025 05:45:04 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:108250c4b31206328ebb008ceda34407e6649472b2a501db69a33b04e685b51c`  
		Last Modified: Fri, 14 Feb 2025 05:45:06 GMT  
		Size: 23.9 MB (23894835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23678b6eca197156f5a465e45ad569c9dbaf2c2989add2061365b755027e08f`  
		Last Modified: Fri, 14 Feb 2025 05:08:58 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbed22e3c0873f17a5f63e8a8d28c02dcbedcc0894bee535eb525b756eee1f65`  
		Last Modified: Fri, 14 Feb 2025 05:09:00 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.3-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:7db10e0c434afbe2ed522dc5f1ca1dac6138d30e314afa3e35ccb82ffa7dd970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 KB (47828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:187058bb2276232e79ef49a3e5806babc8de8589aa6e29879a3e0ed553f129be`

```dockerfile
```

-	Layers:
	-	`sha256:cc3a5e24035954ecbd094ec7648c4816971486af613f0579090e9a78ec595e5d`  
		Last Modified: Fri, 14 Feb 2025 05:44:46 GMT  
		Size: 47.8 KB (47828 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.3-fpm` - linux; arm variant v7

```console
$ docker pull joomla@sha256:b1dcf39afe4bca8aa358bedfb96278b30307166f7d8184f5ef1a96c78012d29f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.5 MB (214508204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e1fa152af15706ccdeb34b26dea541e02c66fa48ed5e3953a51fe733ee9ee18`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.17
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8baf7706a2c9f71c9184120af92649e226b5533608aab6cd9ffbc6dc15435ca3`  
		Last Modified: Tue, 04 Feb 2025 05:01:17 GMT  
		Size: 23.9 MB (23914536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf3121bf0a9ad47be9cd9230d76c59964a3c5c2ad428f1f2d5e0ea10c439534`  
		Last Modified: Tue, 04 Feb 2025 16:46:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4e514983dd1fb84c6ee305b52a5a3c4aa50f60f471002066ed6c1fc22642b`  
		Last Modified: Tue, 04 Feb 2025 09:04:24 GMT  
		Size: 76.2 MB (76162605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2400437b25b5d1b02d62a06166a2fb642e727da4868737aedeb7e86797c34448`  
		Last Modified: Tue, 04 Feb 2025 09:04:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e6b98178585bd9b5689333326fb2ad1aa645cb46050af13ddd35dea8a63a16`  
		Last Modified: Fri, 14 Feb 2025 08:42:59 GMT  
		Size: 12.6 MB (12649108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733164d52b112e327bc18dda8a6a6de6f0623b9458bf043ca9666a367b49c6d0`  
		Last Modified: Fri, 14 Feb 2025 08:25:24 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3448a9d16bf2b5eaf49dd0ed001828c5022c28e14a2d6637abff2b799dfae4`  
		Last Modified: Fri, 14 Feb 2025 08:43:01 GMT  
		Size: 25.4 MB (25406670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8994feab71828e660799df6ebb5afbd400b5bf20a9a2ac6f3872639eb75b4361`  
		Last Modified: Fri, 14 Feb 2025 08:25:26 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cabdc92daf493570e1c73c4ff5b36e544c57172471a160c0f3dbf8e1b8b73e`  
		Last Modified: Fri, 14 Feb 2025 08:42:59 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f911a5a823830f2ec9af366586b830ef35d980e4b76d68944bf5b9c559a52a6`  
		Last Modified: Fri, 14 Feb 2025 08:42:59 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a2eb1a5fa9c94ce0e88657c28d57bbe51683a25e2583b65a47edb01cdcfd9e2`  
		Last Modified: Fri, 14 Feb 2025 08:44:46 GMT  
		Size: 25.9 MB (25944497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:432bc8ceb9eb0429a38ed5a74433cb6d1ebd771e5e99a51f16578735a7b667a8`  
		Last Modified: Fri, 14 Feb 2025 08:44:45 GMT  
		Size: 26.5 MB (26517637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df63f6fa12da8e5f5b177b4e14ecae391b2f55c38bccd37c3a0e9e0c8be22dd`  
		Last Modified: Fri, 14 Feb 2025 08:44:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3028882e09df8062aa2221a0ac62fa9050b890a9e44bdcb8cbf82e39be977ad3`  
		Last Modified: Fri, 14 Feb 2025 08:44:44 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a0a1b16384c9bd29e173b22c482c0f1c0710a39b273b1681e22736f46ca0793`  
		Last Modified: Fri, 14 Feb 2025 08:44:46 GMT  
		Size: 23.9 MB (23894826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2808f5fcc09715ec67de06e71f7f5d9affa0dc8ca6abce90db62b9db0559908`  
		Last Modified: Fri, 14 Feb 2025 08:44:44 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9718ea88f30968f125bc4fea6facec9eb29d1d3e0df1cad25a23740f282f75d4`  
		Last Modified: Fri, 14 Feb 2025 08:44:45 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.3-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:81753af3df9b8e5fa833c902e95253b0816f91b05d3e44adabe1d515389aef12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 KB (47827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1413f52e4131e3778ca709f76e927daf0de904f37f8502647db81b726f4f7b9`

```dockerfile
```

-	Layers:
	-	`sha256:1b910b561f312ac8745cb5ea81690136be288e4c88335fa57e163fbb93e780ae`  
		Last Modified: Fri, 14 Feb 2025 08:44:28 GMT  
		Size: 47.8 KB (47827 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.3-fpm` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:5621aae0a90ee8ab39ec0b70bdb1a53e4a34dd7b1210b3d138185b0cdf588149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246632945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6709069e7f7d9544e6562c7c17c58d27dfde36961a48ae35d936f1a3ef7b1e6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.17
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 04:29:51 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e16d737fb0a30c662d9b2adf51f2dff7d89c28971aed9f2463503588644f91d`  
		Last Modified: Tue, 04 Feb 2025 09:01:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c8571b79e8caaac6ec73bed43c061c8744cd39e18a67d9cd17dd79b0d6ea2e1`  
		Last Modified: Tue, 04 Feb 2025 08:59:42 GMT  
		Size: 98.1 MB (98130343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f74dc117b0b71ab00cf12fe8d534cbeab80ebf367380080264b1ddede90d92`  
		Last Modified: Tue, 04 Feb 2025 08:49:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e84a4aa5f6a8ad023b9cf41eef0c612dc0c59b80e89476d98518153fc260956`  
		Last Modified: Fri, 14 Feb 2025 05:43:10 GMT  
		Size: 12.7 MB (12650757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5390744736065c110d9874684170bfe263302bab10fd26d66ddd2a00da59146`  
		Last Modified: Fri, 14 Feb 2025 05:43:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e274b43ab47f8335a3d05777185a1f87f3daff65f4ae3f31323ce3ef25044af9`  
		Last Modified: Fri, 14 Feb 2025 05:43:12 GMT  
		Size: 27.8 MB (27764170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42de6b7fcea796558f95b49a3b27b3ef5d235076afbc4d97da1900e41bee18c2`  
		Last Modified: Fri, 14 Feb 2025 05:43:10 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a791314e52bb0a4b81a450dc905217c88b5f25a8c18190ae7d74be420e465b83`  
		Last Modified: Fri, 14 Feb 2025 05:43:10 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78dc232132df406adbc0903764c2b0b366c840c0f0e9363fd89e7a6630d681c6`  
		Last Modified: Fri, 14 Feb 2025 05:43:10 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973073215d3fdb421138e5aafeb768ab3fd17e8a002389580bb20b013170e28d`  
		Last Modified: Fri, 14 Feb 2025 05:45:04 GMT  
		Size: 27.1 MB (27100196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbaf3a8a01f72d741d9e1b295be6e65c9c99ccd969e9349bfd98ad030cf0858b`  
		Last Modified: Fri, 14 Feb 2025 05:45:05 GMT  
		Size: 29.0 MB (29033420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf5c090fe996a8682f25aea5b8cdb1c3845121232dc6a2b35656cba541da545`  
		Last Modified: Fri, 14 Feb 2025 05:45:02 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b572a56af7f930c6fb0128b2ecef30869f6da274ad7b54fd9dfcd3edb508cd69`  
		Last Modified: Fri, 14 Feb 2025 05:45:03 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b38fb51eee9d01f40597be5fbe71653e5b3d8402589b523cc1f485b2871832`  
		Last Modified: Fri, 14 Feb 2025 05:45:05 GMT  
		Size: 23.9 MB (23894848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1c896becf38679b76f6bcd771fcd2a7d2b7553a9fa9ac887162bb99684115e`  
		Last Modified: Fri, 14 Feb 2025 05:45:03 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741d3d0cbaba9b71d457c2fe219f2fd3531b8364167a4448ee83283f42c1bc9a`  
		Last Modified: Fri, 14 Feb 2025 05:45:03 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.3-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:1af32f5c2fe862924f78e95eda64705d4d6cdab40146559de83d5a6822edfe3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 KB (47864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5952d5bfb61593b22e9d2deb7e5796be3352409cd45b63b64f4684d74e3084`

```dockerfile
```

-	Layers:
	-	`sha256:0ba7f368484abf2692d38cdc8d28c78a42d0a20e09d33be1969cd25575d33052`  
		Last Modified: Fri, 14 Feb 2025 05:44:48 GMT  
		Size: 47.9 KB (47864 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.3-fpm` - linux; 386

```console
$ docker pull joomla@sha256:9bd91140daf9c26aa20c2971d80f21c0982b962feb68d5e57d218cba7fc599e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.0 MB (254029450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e933d71076b73c78de969af03273de53a4374c1d81df3117866f0265fb06ef6c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.17
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 05:32:31 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12872977850b0f276e580892b46396c8ea6a19e5ac26c2c1f22646e1be268ff0`  
		Last Modified: Fri, 14 Feb 2025 04:09:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e33d62dea93b8ebbd742701712d1ead00fc01a5f6ce322e2c1329250185424f`  
		Last Modified: Fri, 14 Feb 2025 04:09:05 GMT  
		Size: 101.5 MB (101513546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa77dcfa2c3fb90c8b1765c294b68f28bfd5f98814a904906b8428e80df796f`  
		Last Modified: Fri, 14 Feb 2025 04:09:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83346b840b46240564bf6fbc38fb3939866e4f984d0d2f48380916159401a431`  
		Last Modified: Fri, 14 Feb 2025 04:09:02 GMT  
		Size: 12.7 MB (12650026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1db055f06b3a2e10c0fbad724fcb5e5c8155032236c58af4a6f5e7f1035c46`  
		Last Modified: Fri, 14 Feb 2025 04:09:01 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0791dbd231f933b67d7e8316958c1ad0163c5e06cb99235f0a9b9aff8883f590`  
		Last Modified: Fri, 14 Feb 2025 04:09:02 GMT  
		Size: 28.3 MB (28336016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c268b81ae5871a95d4f7453d9a038ceee09a68b203d0cd7f96824c863213c4`  
		Last Modified: Fri, 14 Feb 2025 04:09:01 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2917cd230c109a452aa7afb6e103f9a264f33b3765c717114575a7e85dd2e38c`  
		Last Modified: Fri, 14 Feb 2025 04:09:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a6fae92eb9e9dbc707f15e5f92fa51981c2fb806b9afc39ff6a892d0015e76`  
		Last Modified: Fri, 14 Feb 2025 04:09:00 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151bcac1b18815d3967880f30525c854c4a2212af58f0d5d9961bdeacbca694f`  
		Last Modified: Fri, 14 Feb 2025 05:45:05 GMT  
		Size: 27.7 MB (27662397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d896c7905f40aff394aad4c6a78f8c91550d57882611229f5ef17d3fdf1707db`  
		Last Modified: Fri, 14 Feb 2025 05:45:06 GMT  
		Size: 30.8 MB (30766804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8589b4dbbca987751b0c4fbb7d3a2c759dc16f36898186860c83cc3da03e64`  
		Last Modified: Fri, 14 Feb 2025 05:45:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de24089092cf4882c363d4ef6a068d1f38d8554dbf06132b34b93259f0d8eeca`  
		Last Modified: Fri, 14 Feb 2025 05:45:04 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4445dd1bb06dfb2add42c8366e6ff637081e759b0056933aa2829e9c29920d2`  
		Last Modified: Fri, 14 Feb 2025 05:45:06 GMT  
		Size: 23.9 MB (23894871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d86cc41ba40c73188259f301560ab62c40b089be630bb8bf8c24efcbb727478`  
		Last Modified: Fri, 14 Feb 2025 05:45:04 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bf30ccc1eefe8450777ca8f1a4f0c0c2676a59c6a8f0d51a4f2f3f46950e46`  
		Last Modified: Fri, 14 Feb 2025 05:45:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.3-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:712565de914a0cd97a92f82bdb7fa6ef13ae0afcf86a139f8d52b3dcf742fa1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32247c467114d0536f73aa743b5f8d63bc082c0571b5fdfbcb587166a81a470`

```dockerfile
```

-	Layers:
	-	`sha256:22b870ca648e7a8715dd6303c419048dd1c428c651a5c90bcb938ad9464935ea`  
		Last Modified: Fri, 14 Feb 2025 05:44:50 GMT  
		Size: 47.7 KB (47668 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.3-fpm` - linux; mips64le

```console
$ docker pull joomla@sha256:1a3ecdc1601026174613095b7c06bb322dbdc9ec39a44432d4594adb9319ce63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228433076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc9ae4314991234eac98ff7ad1eb40440c701b2ae75c5f13fe62279706b64c5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.16
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:60fe4951c23056512065fcf1948d3167c5aa5d83d4bfd2829494b7d09b4fe661`  
		Last Modified: Tue, 04 Feb 2025 06:00:16 GMT  
		Size: 28.5 MB (28486581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d943b67c93634afa3f4f4b4aa79cd45b624e4044db2d2aacb4f3924c131b94`  
		Last Modified: Tue, 04 Feb 2025 13:54:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56cad68a9722aed1b3c8b4084c18b366b958254fc3e910b0ed406bed05712c5`  
		Last Modified: Tue, 04 Feb 2025 12:11:30 GMT  
		Size: 80.7 MB (80668958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b77cb490565570ef702dfd920d31b7ad1786c141054119dec7b27a69d8cc18c`  
		Last Modified: Tue, 04 Feb 2025 13:54:45 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f414b800e03e2fcacadc5fc9b0c51fe7c12c2c330b051ec2bb0ae47485f32b`  
		Last Modified: Wed, 05 Feb 2025 10:01:09 GMT  
		Size: 12.7 MB (12651550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:955f1c78eae357724167757939f447279a7025f34cc0caf1519538d7e4e5d054`  
		Last Modified: Wed, 05 Feb 2025 13:00:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a082a19b9e1e7109e3ffec5e5d3500cfb1d601980a65d569805f380761ca851`  
		Last Modified: Wed, 05 Feb 2025 13:00:42 GMT  
		Size: 26.9 MB (26915621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd359d22d2ff232e0f1ef84570c88e47b606168318cd8d7cb9bf2587d0b2bb1c`  
		Last Modified: Tue, 04 Feb 2025 12:01:17 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9543b302210d6710346c04ccd228ccbca07534a668771751ffb20fabad620e0c`  
		Last Modified: Tue, 04 Feb 2025 16:02:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7594e382647d8983bef153a30ecc6a6e985fd729c2813f85e5886b750e5ec13e`  
		Last Modified: Wed, 05 Feb 2025 08:44:15 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882ca58a9bfab36d7f146a07937ef5681d6bd1d8d05c6fdb88204c12e04aa127`  
		Last Modified: Wed, 05 Feb 2025 04:24:48 GMT  
		Size: 27.0 MB (27041654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226f04b940994e6b13648fd2f4b1276c2e05fe3d2548b7739790b8d131d90f26`  
		Last Modified: Wed, 05 Feb 2025 04:24:48 GMT  
		Size: 28.8 MB (28755539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179270df2dae7ab07cb6717e82c88f35c82962b9492cd5ac169fc2122edb5cfb`  
		Last Modified: Wed, 05 Feb 2025 04:24:45 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6d712051575d1b9d7f38b515224714d86bc0d1997ce20d558d2a0cbafc0c00`  
		Last Modified: Wed, 05 Feb 2025 04:24:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d754885b8088aeed13db6b435af2f64d8e61fb8a94846b46fd4de450b46178e9`  
		Last Modified: Wed, 05 Feb 2025 04:24:48 GMT  
		Size: 23.9 MB (23894834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122f4c9d78993d202004aaa6d7b351290c6d5a5d8221dbbeda13c6f9cf76ea3d`  
		Last Modified: Wed, 05 Feb 2025 04:24:46 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5044f1be5bd67dd229f4cba13b4f0fbcb935e05cf11b4231338521d508b25744`  
		Last Modified: Wed, 05 Feb 2025 04:24:47 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.3-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:7be54fcac26a265a2f73ca12827cad7d86d6b4e244215da8bc5247c0ff7b6c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 KB (47778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d691d4e196858b0e70fd8d22f7bd745dc8086c8e017a3a88d16c312b3c96d035`

```dockerfile
```

-	Layers:
	-	`sha256:691129f3b0d8e9595e259b2c27f245e599ea4d670705fd722dc80da243a949a2`  
		Last Modified: Fri, 14 Feb 2025 05:44:51 GMT  
		Size: 47.8 KB (47778 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.3-fpm` - linux; ppc64le

```console
$ docker pull joomla@sha256:8e30187a2544c5df65ebfc604392ba793ca5ea9154d875fb7f57194d0ac582ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260885543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9fcdbd674399875b00b170d9345cb63354b534c8184adb29faa31026d1df949`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.17
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c52a49c08f7ab068d0d2a19ef082b810b96dfc903ac76f338fefe25ead7b4590`  
		Last Modified: Tue, 04 Feb 2025 05:00:27 GMT  
		Size: 32.0 MB (32044779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa84e2e7c890e21e6e4725b61a89702b8e63762c9a3ff81b49aa9d99b48ac4b`  
		Last Modified: Tue, 04 Feb 2025 09:33:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcd99fcd86991b417fb95ad64060b06785ff7f6352ce24df8d275dbdd6a315`  
		Last Modified: Tue, 04 Feb 2025 09:24:12 GMT  
		Size: 103.3 MB (103324008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5ca1e7b60d264395b41c4a4787105a41c87e2bd5e9d67895db262fad4873dd`  
		Last Modified: Tue, 04 Feb 2025 23:02:52 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3857772b0c96da7c9040613a926250a833d047c55388687562c3a7d4bade07`  
		Last Modified: Fri, 14 Feb 2025 05:43:14 GMT  
		Size: 12.7 MB (12650389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b441b884047b59d4fd27bf4cd9cf16f27889216b492e231cd2ea7aefb1b1bd7`  
		Last Modified: Fri, 14 Feb 2025 05:43:12 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dfa87f0abe83e32c29ea15e4f19a418a3e76355f47bb03f92e940505f5de0f`  
		Last Modified: Fri, 14 Feb 2025 05:43:16 GMT  
		Size: 28.9 MB (28887389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb7b81fee13d1ee02628064f2954bd8c536b8ad4cd8f1dcd813f9198f807eda`  
		Last Modified: Fri, 14 Feb 2025 05:43:13 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2aab62346be1c6d9980fe0d13b8f7341be8f92b51b6de3e363a9acc4b7d959`  
		Last Modified: Fri, 14 Feb 2025 05:43:13 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8aaabe270a1213cf3832121d82ef465cf4d765a49a13d90f7a7cdb8c74941af`  
		Last Modified: Fri, 14 Feb 2025 05:43:18 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42450782b1abdbe6a40f305b7c30c047444843fc13a3bbd7ebc6a5f5d0307ae`  
		Last Modified: Fri, 14 Feb 2025 05:45:06 GMT  
		Size: 28.5 MB (28460013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae12f11580358e52835a56e1bc84851019bf893fbbbbc19e5667341d93324ad`  
		Last Modified: Fri, 14 Feb 2025 05:45:07 GMT  
		Size: 31.6 MB (31605782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b55b1ae4b1ec7f92713c568c7abd9537f7deba499c0e0fac140219c48eb238e`  
		Last Modified: Fri, 14 Feb 2025 05:45:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae36bd8c8cc24df34bee11e778c6b623b7b121ab598227fa9db177be086d9540`  
		Last Modified: Fri, 14 Feb 2025 05:45:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22923dae1b020dde3edefbe160d7d47339b56349a372f7b3e9d380c3856125`  
		Last Modified: Fri, 14 Feb 2025 05:45:08 GMT  
		Size: 23.9 MB (23894848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369b4feec50b0098e4a82db24ceae041e2e8950d808246d16492f247b411a6fb`  
		Last Modified: Fri, 14 Feb 2025 05:45:05 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f284f9e6e77bc5e9d4be85176289d8347e3e62e27bb0f912123545c8f9bb0b4`  
		Last Modified: Fri, 14 Feb 2025 05:45:05 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.3-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:6fa0d3a77d5fbcd14f31ad64e49f1a918255eab9b8f83f00c6a44155e6592874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 KB (47760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6746787b65d4b0d33b05f319950d74fce30007c88c7820db5535b99a169ee92`

```dockerfile
```

-	Layers:
	-	`sha256:57d37566c427fd4cba5c9e480e32a051226bb371efc810fa92c35515a115d0fe`  
		Last Modified: Fri, 14 Feb 2025 05:44:52 GMT  
		Size: 47.8 KB (47760 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.3-fpm` - linux; s390x

```console
$ docker pull joomla@sha256:09038e5046c5abaabc9ed4ddb38524d8aaa9b2855c73f37cfe8fa14566b60096
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226120100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d68a9d018905191aeb6691291dd61a13f61a189b769f38d33e9b2a72a52602`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.16
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0d866a6d7678ec487418d89df3dec0b490be07ba1650eb7368f0b61ef4082874`  
		Last Modified: Tue, 04 Feb 2025 05:30:31 GMT  
		Size: 26.9 MB (26858628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710647d60578d6ab07738953416fc54c99ef8444eb6c2db9bb6471f6f43c34c9`  
		Last Modified: Tue, 04 Feb 2025 12:11:25 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7f1ee0c242ea1adeb6d2fd642c25c29c0a4bacfafd5ae692c727e81bd5d326`  
		Last Modified: Tue, 04 Feb 2025 09:33:36 GMT  
		Size: 80.8 MB (80817219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8436378c03a7866b6bb31b6bbe8ffa088643c14fecca9032027a6318a5875c47`  
		Last Modified: Tue, 04 Feb 2025 16:01:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1d54343fdf4189be98bca62d5af4bba69360a111a84090af72c0ba9396bd84`  
		Last Modified: Wed, 05 Feb 2025 08:15:18 GMT  
		Size: 12.7 MB (12652581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3ddf30ec4a44bab4aef6e34e4cb700ded326a0e84510c17be2bd428baae3d5`  
		Last Modified: Tue, 04 Feb 2025 23:03:11 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f860f6051485bceade5172875be371c77cc5f238037378a506f69aa5a754e7`  
		Last Modified: Wed, 05 Feb 2025 08:15:18 GMT  
		Size: 26.9 MB (26921925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05189f452a1f81f87353268d939602ecec5aae28ab59b7404665f7a3e7240617`  
		Last Modified: Wed, 05 Feb 2025 08:15:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7818f8df4bca466c625f91cd16c3f8ac75a298f3f6cd2bfed2f2daa93cf54`  
		Last Modified: Wed, 05 Feb 2025 08:15:17 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34deef4e13cd87f26cb7444f1d8c4f26c604fd5a1a8e0ccb1319f67c0c814cc9`  
		Last Modified: Wed, 05 Feb 2025 08:15:17 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327a63f8d3ab6b87d4447d3a3cc658b2b5b3497858d6a6f8bcece6610e450c95`  
		Last Modified: Tue, 04 Feb 2025 13:10:53 GMT  
		Size: 26.8 MB (26814626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42e8bde01eb015def1cfa49a5cf449ecb7c22bb70dbe06d1813e5c1b5df9194`  
		Last Modified: Tue, 04 Feb 2025 13:10:53 GMT  
		Size: 28.1 MB (28142005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fbf2373bc589e5f4ce37424af879e95d7f1e02fbb0a8e17c989ed7c5300533`  
		Last Modified: Tue, 04 Feb 2025 13:10:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd24b62fec41b22a05c4a11dcdb71e9c54e7d63384ae6278a8e18265848eb7e5`  
		Last Modified: Tue, 04 Feb 2025 13:10:52 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f73343923d2ce875230fe135ab8f5c3f39053cd53e38d44858828a6248bb3ef`  
		Last Modified: Tue, 04 Feb 2025 13:10:53 GMT  
		Size: 23.9 MB (23894797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:120594891ed102ba86118849efafa8b338bb505d2bf3669a0b1f08c8bbdef37a`  
		Last Modified: Tue, 04 Feb 2025 13:10:53 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7972e0b4e687fdff3699965b4a8309ea39aeaa5bc8a2eb38c7adade66b3d9a`  
		Last Modified: Tue, 04 Feb 2025 13:10:54 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.3-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:138087ff27441332d5add80460d7ec06ec1cd7cec3f5847a47d6e60e65b484e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 KB (47700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c267c13eb6ed7136b5ed571d09b13163104d4f1653e343e5eef518cd7c3f47a2`

```dockerfile
```

-	Layers:
	-	`sha256:fea0851e9108081b6ce89f8ec9cd238446e9f3d4ff10b4fbfacc857af06d1515`  
		Last Modified: Fri, 14 Feb 2025 05:44:54 GMT  
		Size: 47.7 KB (47700 bytes)  
		MIME: application/vnd.in-toto+json
