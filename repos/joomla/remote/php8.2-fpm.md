## `joomla:php8.2-fpm`

```console
$ docker pull joomla@sha256:c22b02e4796a96c4fb6d2dd94cd37498165f914def1ad0003c11f77dff2908ec
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

### `joomla:php8.2-fpm` - linux; amd64

```console
$ docker pull joomla@sha256:301393cccefe703008368523fedc1ce7c96063106c120d4dc4cea87372340f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269438996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167fc4fc937ad723ce6575dba275aa36a22ca0cec610424e68f12ac81fb3d4db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.2.29
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6bb69e975bcf65f48201f80e243ad6b7391e7625e817dcf85be69c9937e857b`  
		Last Modified: Mon, 08 Sep 2025 21:52:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa520b8ef6cec8790b04f03f9917efbfe304028aa97c7e667854dda2a8969bc`  
		Last Modified: Mon, 08 Sep 2025 21:52:30 GMT  
		Size: 117.8 MB (117835880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebd8263e55d637898a398f26cbed31070a2bb681d3e9beae3b6e5a29d9f8e03`  
		Last Modified: Mon, 08 Sep 2025 21:52:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b92c19632529f3bd5f1a4eee2dd518f4f91780e541910066f3929020f9f89a`  
		Last Modified: Mon, 08 Sep 2025 21:52:16 GMT  
		Size: 12.3 MB (12309653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb22165fb72b9dd4c68ab6daa6194151632596de580314a8fdc50575619fa77`  
		Last Modified: Mon, 08 Sep 2025 21:52:15 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9f3d54dd8ffc4fd132d2bec558139e390fd50c4049972da026ac6310f53841`  
		Last Modified: Mon, 08 Sep 2025 21:52:15 GMT  
		Size: 11.6 MB (11642740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0908ab06d05277635befb9cf6159c7dfab253bf5c8193f91c7062feb9cfe830b`  
		Last Modified: Mon, 08 Sep 2025 21:52:14 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480f810a17a52f21c3777400a797a7378f7dcd65c863ca8d85b4459a153bf423`  
		Last Modified: Mon, 08 Sep 2025 21:52:14 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe418cb54ea27a32cd045cf0f2df023655cde4a8a1484212d3ace875ee58ca70`  
		Last Modified: Mon, 08 Sep 2025 21:52:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603f2daadd4824bffc594c01fcbdf8e79eda4a7535c6ea57cefd4bb7f65a96aa`  
		Last Modified: Mon, 08 Sep 2025 21:52:14 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef512bc5250df490adb05fb74b6219a68260fb096ff0abe63484fb2b20c900b`  
		Last Modified: Mon, 08 Sep 2025 22:45:05 GMT  
		Size: 27.4 MB (27395275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc002cb2d982392c58628e57a030c63057decca7a10d5f009f4f5429db06c8a5`  
		Last Modified: Mon, 08 Sep 2025 22:45:06 GMT  
		Size: 45.3 MB (45345377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0ba2830533795a1bbb8dd5cbd75182b286de22795078a2026c95fa94f98dd2`  
		Last Modified: Mon, 08 Sep 2025 22:43:21 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30296872170c2290a928ab64f03351c60e6a86d4922ab9667fd8ea4bc74b68e6`  
		Last Modified: Mon, 08 Sep 2025 22:43:22 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2fbb4e741f9848d92449cc79f7989bf6502f15c0715d3292c7d1753b6aeb40`  
		Last Modified: Mon, 08 Sep 2025 22:45:16 GMT  
		Size: 25.1 MB (25118037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a2f530b9747601189cce8b1ecf6efe579652ef805160c3db80e52ccb4947a5`  
		Last Modified: Mon, 08 Sep 2025 22:43:21 GMT  
		Size: 3.7 KB (3658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e1b231da1176df99c2d90b4a9998de66e44f8bb63e2eb75e44874cdac96e8e`  
		Last Modified: Mon, 08 Sep 2025 22:43:21 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:489a78e7310e2f7d303e496ed8a5b63f99c5bef19a3e98c0ac97308e37584ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 KB (46525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d086424d200a995fd5edac4754a6f56612a9194624c3089b831a927adea61203`

```dockerfile
```

-	Layers:
	-	`sha256:40d17af80470b73c3bfcf6163deb72f1d7cfa44b5d01e25fae44877b75238c21`  
		Last Modified: Mon, 08 Sep 2025 22:44:29 GMT  
		Size: 46.5 KB (46525 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-fpm` - linux; arm variant v5

```console
$ docker pull joomla@sha256:fdb505dbdfcda9c92dd15695a9dbd9553e3060bf8c7fcfde7f69fb3a9a3ea7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240557028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eb094ed2da4475d5fc8dcddeaa2457b011ace8457d139528d5c99727b6089a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.2.29
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:498399880872f14c562c46bd2a1ef4cfcf3c2a1453514ff0d0f6b7d89f8010dd`  
		Last Modified: Tue, 12 Aug 2025 22:02:01 GMT  
		Size: 27.9 MB (27941706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b826fc1a1d535eacc028e3d956ad4684d2277457bc010244dfb267e133817510`  
		Last Modified: Wed, 13 Aug 2025 02:04:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5554cad66c2c0be3db0dee9e2828bb1216178113d28498a470e272f7c87a2e`  
		Last Modified: Wed, 13 Aug 2025 04:31:51 GMT  
		Size: 94.9 MB (94871877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bad6001493531fd836717f5de4d6b19cb18c7fe4e2c9d0cbbcb80e66609bd4b`  
		Last Modified: Wed, 13 Aug 2025 02:04:23 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9d2df2483589814f7b18da26d7cf592659b0ca5c8aa3374b1956e5c7968992`  
		Last Modified: Wed, 13 Aug 2025 03:28:09 GMT  
		Size: 12.3 MB (12313629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ec3086eb2063133585d3a2664037d24122e88f88e105e419e9914f1bcc4fca`  
		Last Modified: Wed, 13 Aug 2025 03:28:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ed491c22bdab501a27a205274f03ef9dec97cbdc4ee87a621747a190d2e434`  
		Last Modified: Wed, 13 Aug 2025 03:35:34 GMT  
		Size: 10.5 MB (10459748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a94c3d01053712b77fb1222a5cf5158313f370fdf398b711196b16ec1656d37`  
		Last Modified: Wed, 13 Aug 2025 03:35:32 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d4af23ad054ba5f842f8735a19cab9ce06f9262c8161be9849a12c1e9bc248`  
		Last Modified: Wed, 13 Aug 2025 03:35:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c250c1a90d2a900d54fc8c3dcb3c22685e703c3be78e8df7f4fb9ecb7005a840`  
		Last Modified: Wed, 13 Aug 2025 03:35:32 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ba645b153d7140ec7bad7b6c8a975ccd545241e53461d861150ca2fafd5ea4`  
		Last Modified: Wed, 13 Aug 2025 03:35:32 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5812eba076939a871444642f18ac74cc96347d841fd080fa38340d318e92de`  
		Last Modified: Tue, 19 Aug 2025 23:19:40 GMT  
		Size: 26.8 MB (26820802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6887a5c542ec68d891f54540817712d61d10d87f80534677e8f1360b1ee6a85`  
		Last Modified: Tue, 19 Aug 2025 23:19:44 GMT  
		Size: 43.0 MB (43012689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058041aaf517608d8a4e46f53c3bf7c0beb478c75cc498d68f9117c801802649`  
		Last Modified: Tue, 19 Aug 2025 23:19:37 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee9e083fae4972bd0e5c2e5d24d4c7dbbd1676206e3f3b39ba5a6267b25e67f`  
		Last Modified: Tue, 19 Aug 2025 23:19:37 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c410b911235f709584628f828c50b555dce368e9cf04d68b562b09ef30dfd8`  
		Last Modified: Tue, 19 Aug 2025 23:28:52 GMT  
		Size: 25.1 MB (25118035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e6ebdf91958a6615a9675736c098aa26bfea2373d8a1474b266aeeabaad92b`  
		Last Modified: Tue, 19 Aug 2025 23:28:49 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83455a0b1d977b2a91a7ec7e9a0ff7d2ec1967aa1d2cd689f077ca49220b4524`  
		Last Modified: Tue, 19 Aug 2025 23:28:49 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:00851cb9625be3ab99eb40f28f8d7db0fc82958b34f43faeffe84deb9f249301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 KB (46645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690c5d049218d76486033526efe829b3dc0f13ad109883de3bd2a835d90b7355`

```dockerfile
```

-	Layers:
	-	`sha256:5949abbef0ddef590dae3244f2134c072d7375c984ce8f603dec646a71be8f5f`  
		Last Modified: Wed, 20 Aug 2025 01:46:38 GMT  
		Size: 46.6 KB (46645 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-fpm` - linux; arm variant v7

```console
$ docker pull joomla@sha256:049ed77f3778cafa3f81d65fd1331ebd6175a5b422eb109f41f52ec7ef9b6a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227159702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc0a51f6502d03c79845112e7be14f6443a456d7f15155008037916c6b8aa48`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.2.29
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d480d07cd33d2a61cb24d871a17254661d250ae887a2db15a7e99cb67383a74e`  
		Last Modified: Tue, 12 Aug 2025 20:52:10 GMT  
		Size: 26.2 MB (26207488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f783066fe233d49b725a424d9e4e2edf03ec368e8008a7100235b31d55c72428`  
		Last Modified: Wed, 13 Aug 2025 03:03:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def7928390388cc2020246549215f695478752f6ae67568af1344eee2f6088ce`  
		Last Modified: Wed, 13 Aug 2025 03:03:28 GMT  
		Size: 86.2 MB (86243176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5decd14e90655d8988225e174f3bef3fbd8abee342388203104f64e9516432f7`  
		Last Modified: Wed, 13 Aug 2025 03:03:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48d227f4aa3fc85a4d3742958d320770981ac2aaf25765c480f6587f6b5bc1e`  
		Last Modified: Wed, 13 Aug 2025 09:10:56 GMT  
		Size: 12.3 MB (12313736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db2b6a68b16e2890776e6644e1e104eac958b19f4b910222c818d5adff6ae68`  
		Last Modified: Wed, 13 Aug 2025 04:38:16 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7125d772b62d3ef380f04460256222a27360fbcc39329729ace30e0a65b347`  
		Last Modified: Wed, 13 Aug 2025 04:35:41 GMT  
		Size: 9.9 MB (9852550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e86ee67d08cf8db2a7c4c8d88fadd51367081a43703b033a13210a905218cd`  
		Last Modified: Wed, 13 Aug 2025 04:35:40 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:667c56d45ede702b70f6a94175283d558198f9b65c24206935925606f125d30b`  
		Last Modified: Wed, 13 Aug 2025 04:35:41 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd3ed88d20d49869abc53def918a10039d9d016b722b7b005a05ccd49239499`  
		Last Modified: Wed, 13 Aug 2025 04:35:41 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6119d54e8c173f8ae160a1ba2da5c7a9d5342e1e7c53ba25d73265b6436ea07c`  
		Last Modified: Wed, 13 Aug 2025 04:35:41 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d40fe02075682f4350d41173d4f70169c22813c923c3df8ffc853ba0c1d66b2`  
		Last Modified: Tue, 19 Aug 2025 23:24:42 GMT  
		Size: 26.0 MB (26010467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1996db0034a1090f3bdc8fadd29d7715116207319d1e9837850c85d64cf686b`  
		Last Modified: Tue, 19 Aug 2025 23:24:44 GMT  
		Size: 41.4 MB (41395716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf82c26f211630520843657304661c87b2540b27ba2e1e64a531df78f0a153f`  
		Last Modified: Tue, 19 Aug 2025 23:24:42 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2879b78be24fbbf943639b9a511d9aa71463f47b9b54fa5cd89a5a11f1f540`  
		Last Modified: Tue, 19 Aug 2025 23:24:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3657b28fe0d5f9ebeaca18413e1b2060028a7dfcce5eedb269fd2de281edcdcb`  
		Last Modified: Tue, 19 Aug 2025 23:36:51 GMT  
		Size: 25.1 MB (25118026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de256dfe167963d40aa29c346d1c1477064264d01860e7942cfb854880cc3c50`  
		Last Modified: Tue, 19 Aug 2025 23:36:48 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aee78c44387f42c11a2aabbf0aa013ef8427f6690a14e00acca4c23ae2e0c9`  
		Last Modified: Tue, 19 Aug 2025 23:36:48 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:76c2cb5ebe44ecda825b70c0729583907b74bd0e117e3aa806adf7e9763c5a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 KB (46637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afa40143ca2ceb445841c4725ea7ba3eb73ebd8499510a0693a578a2af86e6f9`

```dockerfile
```

-	Layers:
	-	`sha256:a7dc89084c63205f7a568d0f3217f44e84c931e5f7919b9b0d297a7144b03fc4`  
		Last Modified: Wed, 20 Aug 2025 01:46:42 GMT  
		Size: 46.6 KB (46637 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-fpm` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:2ac5a258c33986df7714fea6df371b8fdc0cd3671998d22723f8b65032fcf936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.9 MB (260892899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cff0a01335d947175c6eafa121cb72781acb76f0462a709bc7f44da3848efc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.2.29
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc03022ec7f33593ecc2a3aeb663cc554de1d9e62087a60919464202ee9a290e`  
		Last Modified: Wed, 13 Aug 2025 03:18:33 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bbeac273051d37a774f98368f1d00d339ab0541a559de53da0b53ac9ed0340`  
		Last Modified: Wed, 13 Aug 2025 04:59:11 GMT  
		Size: 110.2 MB (110160214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a720d4bdd0b0544aeede4fb064271ee7a67ad806bfbd73e41d86f4e6f668e942`  
		Last Modified: Wed, 13 Aug 2025 03:18:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9ee0f0f61d2a7ebee0ca1ab8b1d32f57ff75c8d6388d83924c6ecaa948102e`  
		Last Modified: Wed, 13 Aug 2025 04:51:40 GMT  
		Size: 12.3 MB (12309229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68c6fb5db00fdaffd150fbd4c9d3c168843993d64dbaa579a06204054c406f3`  
		Last Modified: Wed, 13 Aug 2025 04:51:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c68d55fc3fcd4f435cdc13fa24fc9ae2659018a047c78cec5c4c8b00c95f7d`  
		Last Modified: Wed, 13 Aug 2025 04:59:45 GMT  
		Size: 11.7 MB (11684698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c52d58d14bd4d9c5885b91eedb206a9c69d28023ad15598487788f7231dcb9`  
		Last Modified: Wed, 13 Aug 2025 04:59:43 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e29ceffd3d7b71e91a0f37fc4bd3b54f54a336354aa167a3b155448fab69674`  
		Last Modified: Wed, 13 Aug 2025 04:59:43 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ee190503cefa4b8a66393256eb5ce2b759ba00cd5fecc63374941a7889f4ef`  
		Last Modified: Wed, 13 Aug 2025 04:59:43 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f0b77917dcb6a01b489b5134d05ce4a9e92b9ba772b3a376c8f546a195e9fb`  
		Last Modified: Wed, 13 Aug 2025 04:59:43 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1b04a7f893ce9a14d2d0de9bcf66b16b5a90b73cf04cb8073a600d85ff9238`  
		Last Modified: Tue, 19 Aug 2025 23:21:47 GMT  
		Size: 27.2 MB (27210643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4433e89f04a8ce4e01b0fb2c7f123c6180379999521aad92c20a69e7bda64341`  
		Last Modified: Tue, 19 Aug 2025 23:21:57 GMT  
		Size: 44.3 MB (44255489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82825d6887696c008cc508f1d250c9fee8d05f7fac1d22a2451a2791076a43eb`  
		Last Modified: Tue, 19 Aug 2025 23:21:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc357c2a522a0887db544336fb133e5158f86c6e1ab0a9676417b887fe318ad`  
		Last Modified: Tue, 19 Aug 2025 23:21:45 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d74150bac5f9c1eb22254a815ad7d5620de6ec6cc352691310a652b80d5437`  
		Last Modified: Tue, 19 Aug 2025 23:32:06 GMT  
		Size: 25.1 MB (25118040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8742c5e04aec01262d274d53d671c66dfbca878bfe00c3aeccfc947e6cb5b7`  
		Last Modified: Tue, 19 Aug 2025 23:32:00 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499f54b970a8f8e67403401c17efef64548620766a856fc8d87a9f13a888c8c6`  
		Last Modified: Tue, 19 Aug 2025 23:31:59 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:bb5984604ddf148def3636d2daae129d98d1826a2ebc33f61b10cdb950aa6a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 KB (46689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24af0075c54b40a7eca91221abbcd4985cb5f9a8acabd7453cab80ccea44064`

```dockerfile
```

-	Layers:
	-	`sha256:76fe1cf69883d5753c4b6e3cf079857e2947048f727f2755f327f5dd706caea4`  
		Last Modified: Wed, 20 Aug 2025 01:46:45 GMT  
		Size: 46.7 KB (46689 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-fpm` - linux; 386

```console
$ docker pull joomla@sha256:eb156031e26c25a28f6411db6df0b3e6a7bbfda3db68a3132030c8fdea454c7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.2 MB (270172985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72e658f712c598c8b42d1ec522d702c07ee11e3792a466063743ca72e21e68d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.2.29
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bfe6ef9dba48e616cf5a3e24c4f36c8159f8c0d8950662a5a44d5e6a40e06c`  
		Last Modified: Mon, 08 Sep 2025 21:52:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b011002caf0fa09b726473be3f789f3b929145e8410342a7951dc090caf3964`  
		Last Modified: Mon, 08 Sep 2025 21:54:13 GMT  
		Size: 116.1 MB (116136990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b956754e15f949321c021e2e1b5d94471cde981fa286c5b15b921ed91c59e26`  
		Last Modified: Mon, 08 Sep 2025 21:52:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f301a0a6d6ef667384ae8f3852a7bcc044e878b6a99065a684f26bd87d5947`  
		Last Modified: Mon, 08 Sep 2025 21:52:23 GMT  
		Size: 12.3 MB (12308621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7646b63305f695d5002f96d989fa4dbf52d5b6ce9f474ca0eeb40aa0c8108f43`  
		Last Modified: Mon, 08 Sep 2025 21:52:20 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:477b2232650e44052d0f254ddd8b09f7c3c3f4c551a276fd97b05f10ea714549`  
		Last Modified: Mon, 08 Sep 2025 21:52:22 GMT  
		Size: 11.9 MB (11869448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513f63afdc99c6817b4e2a82c32fbd975738c4818d415c660f6010011791e014`  
		Last Modified: Mon, 08 Sep 2025 21:52:19 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b49f91094cb1f6a45587daa32169bddafb68af663c9255de411695ddf77d76`  
		Last Modified: Mon, 08 Sep 2025 21:52:19 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753e69cf24a90deea8a9a5376ed15b29786c8a1e31f26579b871e2aac6213c5c`  
		Last Modified: Mon, 08 Sep 2025 21:52:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e694a917e8147141673f5c4680ba452a70d89e17c9ef364d8687b0782f707a`  
		Last Modified: Mon, 08 Sep 2025 21:52:19 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809a0b7039027c53f5eac9d4c3cb0effbb60c6dece639ba859e468effa777505`  
		Last Modified: Mon, 08 Sep 2025 22:45:09 GMT  
		Size: 27.8 MB (27839558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f27566bb4b073f4c15c04d13a68391b96d45200a9ee467e149a6818f54c90e`  
		Last Modified: Mon, 08 Sep 2025 22:45:08 GMT  
		Size: 45.6 MB (45592022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44c60cf522b985aabf7059cb44201b438a64f1dd1cfae6d92d33f6d9872676e`  
		Last Modified: Mon, 08 Sep 2025 22:45:05 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed7791db00c74cda9201063367d1e77e8ee161086b4f56e836bdee99737ee7e`  
		Last Modified: Mon, 08 Sep 2025 22:44:59 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dbb62675e374240e5c27db795f52a88b04355fcdafa07a7b85b554721c76b1`  
		Last Modified: Mon, 08 Sep 2025 22:45:07 GMT  
		Size: 25.1 MB (25118036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad79eaa58b26eb54b3d1d152947ff011fa5b538c970fe21aba90fc5962f5f68d`  
		Last Modified: Mon, 08 Sep 2025 22:44:58 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8005dd58647eb489d653c61fe934044bf379a77fe8c0a19c744c72b97a9eef`  
		Last Modified: Mon, 08 Sep 2025 22:44:58 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:1211c3aecc570312e2ad1055ffb871c39f3a8334e79321dd2a8fe3dc473b2163
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 KB (46485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09fb869a62b0d608f111a88208b55de08e336ae5b49af13345fbb1b4f2c68bd`

```dockerfile
```

-	Layers:
	-	`sha256:3d9eb06079fcdad80873ea5d64837e34de2cac559d6fd935d07c55360e718e90`  
		Last Modified: Mon, 08 Sep 2025 22:44:40 GMT  
		Size: 46.5 KB (46485 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-fpm` - linux; ppc64le

```console
$ docker pull joomla@sha256:f7dab329a5f7e8bd7b22c2743a9a9e74d56817565b3800f05d40c2c62387e62a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268541630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f565179c38a87ba85f6e6ba55fad16bbf827535ab35077e64506ddeadc492c3c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.2.29
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:52a4daa8724e9e1632306e15fe478aa26ff0ebcb7ba924cb168e9b6738c239d5`  
		Last Modified: Wed, 13 Aug 2025 01:42:36 GMT  
		Size: 33.6 MB (33594213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe95aaa1875d4c50c764ba29c6f95cc470f62d9ac88ad9109e0cd4505d319b5`  
		Last Modified: Wed, 13 Aug 2025 05:31:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0ffef807c2273a22858b85bf52a5cbb82101766a6dfce24ba2f8e3ca25f228`  
		Last Modified: Wed, 13 Aug 2025 08:03:15 GMT  
		Size: 109.6 MB (109595127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e8a64ac10b73fd871320ade0ad956a6b2aeb6e2c3151d32095cad855bbccb`  
		Last Modified: Wed, 13 Aug 2025 05:32:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22142237286a1505a8d535b7774f5ac5bbc6dd6312c3b88d8ef4449c663ea7d6`  
		Last Modified: Wed, 13 Aug 2025 09:15:25 GMT  
		Size: 12.3 MB (12315101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c1c6b4772aed603afb8f82dd3e9ecf80b88b4aeaf4e78cd788a9ba02757ec67`  
		Last Modified: Wed, 13 Aug 2025 08:19:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d234d815abd5af630d8c0c4ded6bda10b1baff3d9fb0e5ce5822fbc3139d2d`  
		Last Modified: Thu, 14 Aug 2025 02:24:30 GMT  
		Size: 12.2 MB (12188318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7e43193f3e8fa8b2e9ad74e9998f64cf591b34f4c75d890decf5d8df3b0cf6`  
		Last Modified: Thu, 14 Aug 2025 02:24:28 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8097f2ab6d7b269379b5bbe441d068fe1dcb3ca02e2322c7527f6f1c145a6b`  
		Last Modified: Thu, 14 Aug 2025 02:24:29 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d42c2dfb205389aee2b90ed57cc9226c53dd7fd360da3645545c0858b2ac30`  
		Last Modified: Thu, 14 Aug 2025 02:24:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a48e29b045bd86058c9ef1120908e1cc13a60f2b4f8c2fe6e50e62643af6b1`  
		Last Modified: Thu, 14 Aug 2025 02:24:28 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b58c4205e166a06d3c2e872718f939946d77726ffb6afd2e07f663dadf56b1c`  
		Last Modified: Tue, 19 Aug 2025 23:32:39 GMT  
		Size: 28.6 MB (28551656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773193f1c1a3d209a00d6a5a21e9060041a77217a18b74e418856731c54ed01d`  
		Last Modified: Tue, 19 Aug 2025 23:32:38 GMT  
		Size: 47.2 MB (47160651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb5088581ce0b8b1e598a97d299c7a7019ac81c2f8334a0a25bd67be7e7deead`  
		Last Modified: Tue, 19 Aug 2025 23:32:35 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03737dab6ef074b8110eb75b3dc73edda503ced91200e0e388bbc70027b48318`  
		Last Modified: Tue, 19 Aug 2025 23:32:35 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512297e08828120bdb5a7bd30975654cad7e127d3c559d6829d711524037b398`  
		Last Modified: Tue, 19 Aug 2025 23:50:39 GMT  
		Size: 25.1 MB (25118030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f9cf1390b64cd7f033a4869609495274f382f257ad4503b49e01cfcb0ba4fd`  
		Last Modified: Tue, 19 Aug 2025 23:50:36 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2704c2ed4c86497fec2f2d99a7058b4b1b51b114d7702bca32f22aec6f08438a`  
		Last Modified: Tue, 19 Aug 2025 23:50:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:86676b278ae8f684cde31a65d6f52ceb584ec6794edb21c2a0054ad359d0f22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 KB (46577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73912c3acafe666a2f9bd7fa3c51b6b6a841d5575abdda663c2d2ef42af3095c`

```dockerfile
```

-	Layers:
	-	`sha256:d22da557a066ee907e4c9dfd1513e8be51bdd58c2d1458fdb759dbe86ed4a354`  
		Last Modified: Wed, 20 Aug 2025 01:46:52 GMT  
		Size: 46.6 KB (46577 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-fpm` - linux; riscv64

```console
$ docker pull joomla@sha256:21b201199c6f19477585adfd54f2217c38f98b6ae614c67cff0ce1cfab2b0493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.6 MB (303645782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b79dabaf61fe42aa1516ef244649d0ebd95c89d29f0997c4bbfd4ea381341e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.2.29
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e74ecc2368ed7bf14f15784d294255a507b61c121584b8889b54497f586460`  
		Last Modified: Wed, 13 Aug 2025 11:14:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ba9332bf4f75d23eae5411f58fe1a55971f98de6873eba08746a8a1042d175`  
		Last Modified: Wed, 13 Aug 2025 11:43:11 GMT  
		Size: 146.6 MB (146577824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05acfa088a6e9eb3845fc5011b31ba6a62983f44944e2347f32361bf21d8f85`  
		Last Modified: Wed, 13 Aug 2025 11:14:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3993d461325aabaa622813d7633f99ee60e3a41724dead8c0750de37df8bbec5`  
		Last Modified: Wed, 13 Aug 2025 22:33:14 GMT  
		Size: 12.3 MB (12321653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cf34cc6defe9db15357e3f52820df7ffa2a9a6d80db8d41e0f863a8738654b`  
		Last Modified: Wed, 13 Aug 2025 22:14:44 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10d0f25358fd6375f3d816eeea92fb382057d67fa0061d8e310205dc7fa1aa9`  
		Last Modified: Thu, 14 Aug 2025 00:14:37 GMT  
		Size: 11.0 MB (11000839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe098345dd8b415336460bf3f08ddd97ceae3ea4184e2cd82250665bae04e4b`  
		Last Modified: Thu, 14 Aug 2025 00:14:37 GMT  
		Size: 2.5 KB (2457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b569f965639d293e81147c07bccc8a2502e8ce01062907ea9ae5fd4638eb804e`  
		Last Modified: Thu, 14 Aug 2025 00:14:38 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c1ff45d558433a46b629e685f8e5a9c249fb008598ea31e03bf2f3e5d01082`  
		Last Modified: Thu, 14 Aug 2025 00:14:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a4996862ca8125cce4d53bd39136d6e48f82312f60f4421db2dbef540b4203`  
		Last Modified: Thu, 14 Aug 2025 00:14:39 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485fc47aacbecd7d3bbb2d2e661d18ebad9395be4aed7ccd6c8cfd21b1f7af54`  
		Last Modified: Fri, 22 Aug 2025 08:34:07 GMT  
		Size: 27.3 MB (27324824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fe4c1f22b2c817ad0e5f5eb1ed0a79f0d1f5660f81507908915e00c739dde3`  
		Last Modified: Fri, 22 Aug 2025 08:34:12 GMT  
		Size: 53.0 MB (53012425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd13328e24050945eb7d68953f2254e5e616e4e5812bf16a36f43eea2963701d`  
		Last Modified: Fri, 22 Aug 2025 08:34:05 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fcc20847aadc43480e2412181ba8af7e16a38d643d354df8a641303c70dc62`  
		Last Modified: Fri, 22 Aug 2025 08:34:05 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62f2a39f28c89d0e90db70fab4c551cb7a6fb5097f6f509b07640b823c2dd4b1`  
		Last Modified: Fri, 22 Aug 2025 08:34:07 GMT  
		Size: 25.1 MB (25118038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b6f23523070bd9c5fdf7216e99b747ece10485478a7af5a6bd10ebf1b49750`  
		Last Modified: Fri, 22 Aug 2025 08:34:05 GMT  
		Size: 3.7 KB (3653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc7d376a97309bd7eda8f4b0473c086d68ffa1a84a3dabc41cd40311ec7d79e`  
		Last Modified: Fri, 22 Aug 2025 08:34:05 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:a229437bc67ed888eb2debf2e79b59d2a87c50dcecd6cdcc2462d32d9e7e9a31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 KB (46577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77aadfdbcf929fdcc417f9b1661250558b79c2f5a0fe02c9eb728319423bc08`

```dockerfile
```

-	Layers:
	-	`sha256:8e1c5417d95b153c37b7d6c89757c61bf727a4b633c0da392446395645163e3a`  
		Last Modified: Fri, 22 Aug 2025 10:44:06 GMT  
		Size: 46.6 KB (46577 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:php8.2-fpm` - linux; s390x

```console
$ docker pull joomla@sha256:ef247c39b1a3442b2f4c92e3ce34dbfa8393907e700af79059cb74bfce51eaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.9 MB (243935039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c954770ad32ca46740a2dc36157eafc88eebcf4c7d97001c324bb59e92194a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 08 Aug 2025 00:02:22 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 Aug 2025 00:02:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_VERSION=8.2.29
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Fri, 08 Aug 2025 00:02:22 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Aug 2025 00:02:22 GMT
WORKDIR /var/www/html
# Fri, 08 Aug 2025 00:02:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 Aug 2025 00:02:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 Aug 2025 00:02:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 Aug 2025 00:02:22 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 22:37:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 		zstd 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libgmp-dev 		libicu-dev 		libfreetype6-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libmagickwand-dev 		libpq-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
VOLUME [/var/www/html]
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_VERSION=5.3.3
# Tue, 19 Aug 2025 22:37:33 GMT
ENV JOOMLA_SHA512=efc0c5249758f1f7d9915992e01aa44203e86126c59c4c3adec8a7342aec132da2f5e10910fd7e2485ab8f58faa981de6be99cfe3c3b3f3c1e79e7d2d0321388
# Tue, 19 Aug 2025 22:37:33 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.3.3/Joomla_5.3.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 19 Aug 2025 22:37:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Aug 2025 22:37:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bfe4d60a27c9392ab729f16b50a763cda36622d744066c3cf029a072133f2907`  
		Last Modified: Tue, 12 Aug 2025 20:59:52 GMT  
		Size: 29.8 MB (29833057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d672c8320b5c626e155e165336b2569c5c22cfbda44788e2e9dd0b175c8a1e`  
		Last Modified: Tue, 12 Aug 2025 23:44:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06790e9e58c7a87421168e1b912411e592f3adbcdce2412a5541e72fa8de3f1`  
		Last Modified: Tue, 12 Aug 2025 23:44:49 GMT  
		Size: 92.6 MB (92562072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019838dc72213baa0c7fefd5773b69a921a755553c45ef473aea40f478c95cb3`  
		Last Modified: Tue, 12 Aug 2025 23:44:45 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90045332a68ba77605ad01c63175f75103608fad5bf21cb273a160522e3e687`  
		Last Modified: Wed, 13 Aug 2025 00:54:51 GMT  
		Size: 12.3 MB (12308231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0688a2e8ba77f7898d85db85ef58a906773a66eb0e482b0e179d2f3dd71c164`  
		Last Modified: Wed, 13 Aug 2025 00:54:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08fd378b26e0c97cd9a3daf1990cdf319c8139a08c3f5c9d5c8678ecd8ffe11`  
		Last Modified: Wed, 13 Aug 2025 07:38:25 GMT  
		Size: 11.5 MB (11531052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c2e80289ed28872e24311311ed45743e8cb8c9803bdf28d6720a267e0b3833`  
		Last Modified: Wed, 13 Aug 2025 02:02:08 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33040a0a3907e85c943f2da1550b797bcaccc69b32a8c2b16b60658340f4fca4`  
		Last Modified: Wed, 13 Aug 2025 02:02:24 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13617fef005392beef2303f8e4c6cb5d3f7c94977df7a79954754de56c825772`  
		Last Modified: Wed, 13 Aug 2025 02:02:07 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5700481d3e80b5a3685e74419259dd3a1aa802abc357c5a45a6325a6ad18131b`  
		Last Modified: Wed, 13 Aug 2025 02:02:11 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5703314f75f303747dac7ff6a9883b842e4f144b765517e99045e2387e032e4a`  
		Last Modified: Tue, 19 Aug 2025 23:27:42 GMT  
		Size: 27.7 MB (27678889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64e048db991425af7377eac824bb2f8890fe3f4e8fd348f3ca95b8ecf0d8e419`  
		Last Modified: Tue, 19 Aug 2025 23:27:43 GMT  
		Size: 44.9 MB (44885189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a52642ffde082ea7e5e20d364ed7056ab6edf528071c7b5bc0cd507de975930`  
		Last Modified: Tue, 19 Aug 2025 23:27:40 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c19dc12f9ac947e5cd78746fc2a01f7ce218396c2831e88a3e4db092671cacf`  
		Last Modified: Tue, 19 Aug 2025 23:27:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b582dba53375f0df5ea1798885f8b508bb2e34f1cb633b9d5f22cd0b1bf18d`  
		Last Modified: Tue, 19 Aug 2025 23:38:38 GMT  
		Size: 25.1 MB (25118022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edca5bd7c0cf281e4967ae2980cd7f2815864544c48256fa4a11ba3873fb581`  
		Last Modified: Tue, 19 Aug 2025 23:38:36 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b10617f08fd8238e5d7cdeca9d936af56b659635f59db7aed058860074040db`  
		Last Modified: Tue, 19 Aug 2025 23:38:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:php8.2-fpm` - unknown; unknown

```console
$ docker pull joomla@sha256:cc32bf6ab088b5d342120551f1ac1fff6c6ac40d54baeafd98a87c59c3f39adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 KB (46517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d38695f2c5a69787509751f4629caae3ecab23ace1297fcc86b14361d19fa1a`

```dockerfile
```

-	Layers:
	-	`sha256:57f07c3b6709f0881518b2607962fa7f2d94f03ac12ca44ea67ec589a95ab4ec`  
		Last Modified: Wed, 20 Aug 2025 01:46:56 GMT  
		Size: 46.5 KB (46517 bytes)  
		MIME: application/vnd.in-toto+json
