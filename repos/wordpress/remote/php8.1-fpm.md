## `wordpress:php8.1-fpm`

```console
$ docker pull wordpress@sha256:fee03b396f18505bb21cc9cd17292bb2b8676040d0da7319b4ff4237ba7f561b
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

### `wordpress:php8.1-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:471cf16e9dec4e550e2dec86b752c9d781bb9c654ce4fb008131f1f7801c7bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.4 MB (242439409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510e2e70e66e0dc9f774b63d4f9142fd123037b6d9ccd0706a7799c92f06c05c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Feb 2025 20:06:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.1.32
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Feb 2025 20:06:56 GMT
WORKDIR /var/www/html
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Feb 2025 20:06:56 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
VOLUME [/var/www/html]
# Tue, 11 Feb 2025 20:06:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa97865270981d54dba95ceb07e18b485292aacc949fcaa2eb17e8231359277e`  
		Last Modified: Mon, 17 Mar 2025 23:23:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c24329cd6e3d44b6e8bb465a1fd35ea1cf819e8a2e814ad8283b8b34e376ed`  
		Last Modified: Mon, 17 Mar 2025 23:23:07 GMT  
		Size: 104.3 MB (104329346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead64ee0ab7bc6626af1bf27311d3bcbdc656bf80c0401f3d892c585d55295fa`  
		Last Modified: Mon, 17 Mar 2025 23:23:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322cd9a607da1a11da2db6b435e33f4147704e07a445cb61c952753f694eb409`  
		Last Modified: Mon, 17 Mar 2025 23:23:04 GMT  
		Size: 12.0 MB (12003136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f19ba6572979e6f078cbd29137d30226c2cb9539d16b907154b09539506537`  
		Last Modified: Mon, 17 Mar 2025 23:23:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9167a64348d1e07e0edafd6116d011a399c7b4ba515520739cbb63971a03fa8`  
		Last Modified: Mon, 17 Mar 2025 23:23:05 GMT  
		Size: 27.3 MB (27331079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62c4d6a150d29ba7613df2d5004bf5ba5d75c530ef571642f7e4e44b9089de2`  
		Last Modified: Mon, 17 Mar 2025 23:23:05 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a41f9f23a2ba3f4c175460b9d74b4aa6cd1e7f9d55fe025b6aac654568e3fe`  
		Last Modified: Mon, 17 Mar 2025 23:23:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1d0accd38b64ed311747960bf95f177c251ff9f4ac1ab07af2d901937c4dd1`  
		Last Modified: Mon, 17 Mar 2025 23:23:06 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54067bc56d2f2def4679d05db38ed5503c3232a4dc3b6233e4549e91af85a267`  
		Last Modified: Tue, 18 Mar 2025 00:17:20 GMT  
		Size: 26.4 MB (26374512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d130df3dfee84640574d9003a67046774694434a54cf3cf60194caf76193d229`  
		Last Modified: Tue, 18 Mar 2025 00:17:20 GMT  
		Size: 17.4 MB (17420926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc0ff62559eae89e58eb781ece381665933a9a790b407eb3506cc949d76415b`  
		Last Modified: Tue, 18 Mar 2025 00:17:20 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8879f30435131d869b816703f179913da9728e740ff785da3780bd1924201176`  
		Last Modified: Tue, 18 Mar 2025 00:17:20 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1365f1c42d405aee3e76a8a957878a23ce2cf4ee4f9d64d9d56a43859d60dbb0`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 26.8 MB (26758082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac1b35f202585d6ab9b6bbba9e2719d99902cbb8a8a187ed425a4a73203bd17`  
		Last Modified: Tue, 18 Mar 2025 00:17:20 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd52cdc647e5d6299610ae5d4a4fa1ba32cf46b3284f4fd043114d84d2dd9f8e`  
		Last Modified: Tue, 18 Mar 2025 00:17:21 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:91a04df58341814d489eb274602847179b3c9ccd481dff3b9922f413d8508fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7649253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274be1a246e50cff21a81f4d6590b4186579a072a8ea7e34b93d49943fa25b4e`

```dockerfile
```

-	Layers:
	-	`sha256:d0c03998dfdf4af9a6c1520acf4d3e35372c5d2d09d43409a5c4dd9a2a7ccac5`  
		Last Modified: Tue, 18 Mar 2025 00:17:20 GMT  
		Size: 7.6 MB (7601048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea5f2f51b783c813b96387a410a6af93ecaea94a66d4c182496834db6a95da54`  
		Last Modified: Tue, 18 Mar 2025 00:17:19 GMT  
		Size: 48.2 KB (48205 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:b235702256dc05247a0d94d1a8d6e80c993a58b2a73b1dfc4370da52794552b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.3 MB (211338148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0ac7f30c5b1e09767e5b0bb241ec3c9e8ae520744e976bbc685a4b29c7a113`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Feb 2025 20:06:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.1.32
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Feb 2025 20:06:56 GMT
WORKDIR /var/www/html
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Feb 2025 20:06:56 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
VOLUME [/var/www/html]
# Tue, 11 Feb 2025 20:06:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50392f60ef98ab502e7ed416d506883257fe8ed57158995e7e77f0bb4d3317f7`  
		Last Modified: Tue, 18 Mar 2025 01:17:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70faba6dfc75d37d904a2f4e790ed9afc8110c25721f14deb57e142ce509f203`  
		Last Modified: Tue, 18 Mar 2025 01:17:34 GMT  
		Size: 82.0 MB (81993797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daffac9eca4d243722e527ddd815f9abe7f53272e743c7fd4b6c1177b0eb255`  
		Last Modified: Tue, 18 Mar 2025 01:17:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:444e0ca7b436985deaa64630ca637921c8982d5b1e508cfff8cc9b6c52853b08`  
		Last Modified: Tue, 18 Mar 2025 01:17:33 GMT  
		Size: 12.0 MB (12001295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccaf7126532c8eda4e58ad623a294b08a53b77dab77ef5bd366eb9ef5215885`  
		Last Modified: Tue, 18 Mar 2025 01:17:32 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1755328147effdff543e7fecc087afe68de473c5da8d57a836c25e299cbdaf`  
		Last Modified: Tue, 18 Mar 2025 01:20:50 GMT  
		Size: 25.8 MB (25811250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19a8d9e1c49a676b9fe079520d1934bd0496c4dc36d4c8c13d8e5a78749dfe9`  
		Last Modified: Tue, 18 Mar 2025 01:20:49 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc4b696c79316b9ee910a602d6cddf90a09591a633480a69599034540c58e86`  
		Last Modified: Tue, 18 Mar 2025 01:20:49 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e01f2ad118ce50e0360e07e90b403ee6c9382330f5e0cd07a7fd013146bd7b3`  
		Last Modified: Tue, 18 Mar 2025 01:20:49 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7671809d390645f13915efe0ca4cc2bf0b8ea18115922e0df5ca5d5f0a6b96`  
		Last Modified: Tue, 18 Mar 2025 05:10:44 GMT  
		Size: 25.8 MB (25823205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4051087ff97620845dd266a7735e387b91403750dc4390c82f3a907f43a5e687`  
		Last Modified: Tue, 18 Mar 2025 05:10:44 GMT  
		Size: 13.2 MB (13197189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5b429ecffc1ed8e6ec42b3e07cbf9d636baf56d65a7f7c91b2ba91d073ece2`  
		Last Modified: Tue, 18 Mar 2025 05:10:43 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe33e19b7b996ab6050d8c486ea3a9688a01520145e06541408c98509a5fc9ac`  
		Last Modified: Tue, 18 Mar 2025 05:10:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62781b814ed3353b7330ba13f121796a074f6da4ad163d766ca7cfffe044752b`  
		Last Modified: Tue, 18 Mar 2025 05:10:45 GMT  
		Size: 26.8 MB (26758087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f757a8c4995ae434bafdc195ea9159c114c13e3d5ce04796ec0ca3b28752c10d`  
		Last Modified: Tue, 18 Mar 2025 05:10:44 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b38d1e334c41b3f266e35339528cd541f3f62945986a15ea4ac66bfeb1318720`  
		Last Modified: Tue, 18 Mar 2025 05:10:45 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:a34e17eef77276cea37f261f6bb6142269ae3730066a402aea3d9359340d1a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7455506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb7e4c0c511a4c1f7e8b416a82c158d3d927e89bdc57b37b93f2f1b30080774`

```dockerfile
```

-	Layers:
	-	`sha256:6991c859293de13595946641d895e7f08dd10a487ecf5541d0f6e01e9870dd03`  
		Last Modified: Tue, 18 Mar 2025 05:10:43 GMT  
		Size: 7.4 MB (7407181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a315881dbece103871bf107907b50110768212ac29c1af9363f4715c348c3b00`  
		Last Modified: Tue, 18 Mar 2025 05:10:42 GMT  
		Size: 48.3 KB (48325 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:6587244d31e280ca237c95edd9726455c56e68f64f2790e03c58121901967230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 MB (200941118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4a767fff117f7a032973089f067725458a4780b4cecec35dfd2e0010e66088`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1742169600'
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Feb 2025 20:06:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.1.32
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Feb 2025 20:06:56 GMT
WORKDIR /var/www/html
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Feb 2025 20:06:56 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
VOLUME [/var/www/html]
# Tue, 11 Feb 2025 20:06:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
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
	-	`sha256:c64676fb52c11bd3fedee5f2cb485ea3c347bd0aab1b5101d7849554a485afc9`  
		Last Modified: Tue, 18 Mar 2025 09:40:39 GMT  
		Size: 12.0 MB (12001246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8115c6b3b58430b529c9f74ef43211399479797d7a9e22c17e8dad1f8bbd9363`  
		Last Modified: Tue, 18 Mar 2025 09:40:38 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5f8ed33bb72348ef13eb8918c061c099c8d6223880907d7fa448312469fd9e7`  
		Last Modified: Tue, 18 Mar 2025 09:45:57 GMT  
		Size: 25.0 MB (24956473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:033617dadeee7880113f7f2d777cf3905afa77e1664c9d728c2cc552545217a4`  
		Last Modified: Tue, 18 Mar 2025 09:45:56 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d873943e0ca436ddc286d90153c25c7abd4fc6a96c721a11b748ffb3751a2a85`  
		Last Modified: Tue, 18 Mar 2025 09:45:56 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33051730acc2a3f498b908d02232a30423f6d7401b6ad0534c0e50474df3631a`  
		Last Modified: Tue, 18 Mar 2025 09:45:56 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3d8fa6a8ee3f9a7d656f4bd3e889609e8b57588b48bd13990f399c17dcb694`  
		Last Modified: Tue, 18 Mar 2025 14:16:50 GMT  
		Size: 25.2 MB (25161718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e601f158391711aae6833aa8b4525358485f85029425b46e33ddcfa48b7677`  
		Last Modified: Tue, 18 Mar 2025 14:16:50 GMT  
		Size: 12.0 MB (11968023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d2d3f3c27db66f4f43924c05413fb68fc85527220e450885de3410eb52fa6`  
		Last Modified: Tue, 18 Mar 2025 14:16:49 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d636d1d5f1741ba04445de1b1f6be79d5d3956fd933e9bd7b07753c3fd471663`  
		Last Modified: Tue, 18 Mar 2025 14:16:49 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d230694a7cb33c0c8a1dc3caf8218fefe1af9c9b83d4f171b213cd161c6ed2c6`  
		Last Modified: Tue, 18 Mar 2025 14:16:51 GMT  
		Size: 26.8 MB (26758077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa5735ee711ee769131f4299d7fee5dc2ef09e1358765696a2521b88a66ecd1`  
		Last Modified: Tue, 18 Mar 2025 14:16:50 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f071f3e7f1877cce77ca5e0a3d88d01cb6cb544ef8fe6fd706cc753ff4893c36`  
		Last Modified: Tue, 18 Mar 2025 14:16:51 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:b0e0a3e8cb1d308d6c435aad3581884e64514a25f25d99e3bc1898e9bfc22a8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7460172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41072106e1a9997c55635232b7e90f900fbf5f9d79d1db94768da6606ae983bc`

```dockerfile
```

-	Layers:
	-	`sha256:69f9a0ebb078936e699e89346c9e5aac8b0c0758004aa509fcb5e6c864126fd4`  
		Last Modified: Tue, 18 Mar 2025 14:16:49 GMT  
		Size: 7.4 MB (7411847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b3cd7c52f45aebc12fe4338327ae4e4ca6a3a8ba5049a19a66259d22caecfef1`  
		Last Modified: Tue, 18 Mar 2025 14:16:49 GMT  
		Size: 48.3 KB (48325 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:bd435c54e2c096f298903c523b895f1ef321a345166e9bad06efde4383dfe5c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.2 MB (232246254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:273f6441edaf209e4851f1b00f072ab5a4e2921b0385e80e3e8e73531d8176d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Feb 2025 20:06:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.1.32
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Feb 2025 20:06:56 GMT
WORKDIR /var/www/html
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Feb 2025 20:06:56 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
VOLUME [/var/www/html]
# Tue, 11 Feb 2025 20:06:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b845448e3a2fe08e44de9ba393e368edaf553ac2b42b58d46d95c8f2fbec662c`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e86d7f22c74cb3db95f1c6735710834cf0f07e91ac282ce7db0d5d41e01bf71`  
		Last Modified: Tue, 18 Mar 2025 05:41:25 GMT  
		Size: 98.1 MB (98130134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9244afd9af6f27e0dc7bde93588cd95adc9c04ee4cf0ddeac0af32d2ce6f2d9f`  
		Last Modified: Tue, 18 Mar 2025 05:41:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d903f456f52178ae5ce8dc14ca8ef564b28bcea5ea437b8b8384c836f441a6d6`  
		Last Modified: Tue, 18 Mar 2025 07:30:38 GMT  
		Size: 12.0 MB (12002970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf68910144743acf65c541ab6a22ccba7cd8dc2fc984928248ecbcbc4441be53`  
		Last Modified: Tue, 18 Mar 2025 07:30:37 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9194dd416d3d1fa495b50f3266467fa8064d933552d0fbc08e027e7e2724ad8`  
		Last Modified: Tue, 18 Mar 2025 07:34:51 GMT  
		Size: 27.3 MB (27279774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2b8f2462195b0f90143456a95cc444184aa91e25f68144e456aeb7bbf7fdad`  
		Last Modified: Tue, 18 Mar 2025 07:34:50 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cad3ee89d9fde6bb2a666c3fd0cd0b0d7d0c0e5f238defbf3d5f7910984207b`  
		Last Modified: Tue, 18 Mar 2025 07:34:50 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38e799492fb046eefd5ac9dc476a5c867639a991fa5a84048f6462fb9cd25c9`  
		Last Modified: Tue, 18 Mar 2025 07:34:50 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b3abc4ecc0744bd57b5ebcbc29cef7d3199fccb268e64a06350ffc26d895ae`  
		Last Modified: Tue, 18 Mar 2025 12:04:10 GMT  
		Size: 26.3 MB (26287521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db2a2fc45f233fa6158783323c36c63a485092f109723d0cf68c720b254ce99`  
		Last Modified: Tue, 18 Mar 2025 12:04:10 GMT  
		Size: 13.7 MB (13726256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e5f24579238d8ba736a043337edb7a30f6a6f51df854fb5c544e673b47adb0`  
		Last Modified: Tue, 18 Mar 2025 12:04:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07af1457a2c89b583edc81a5ecce0ec46163a0fa364906f132e734efd8f6c4a5`  
		Last Modified: Tue, 18 Mar 2025 12:04:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed14717fb3f56978749b0d6e75cfb2b657f4a851c6502faa9ac187ef3f9d1f91`  
		Last Modified: Tue, 18 Mar 2025 12:04:11 GMT  
		Size: 26.8 MB (26758090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f4d2af202575121e53a72fbe6069a9a1b7a671f25f49d7d6ec249c8f6182f4`  
		Last Modified: Tue, 18 Mar 2025 12:04:10 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f10543c470f80694b9a26ea9552c0f3e96d2da7dd61b985f8982a34a556b3b07`  
		Last Modified: Tue, 18 Mar 2025 12:04:11 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:4007fa3fb36eda43b679da1a50aaaee09dfeda6398649913d99864be917fb1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7678162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a94b90d798a0b07ffd000ffa2b525b7157034872e9244ba4077ceeedd455272`

```dockerfile
```

-	Layers:
	-	`sha256:1416b0309a62272e21c485c410ad57947ab329afda49a667d3574f7de41ae2aa`  
		Last Modified: Tue, 18 Mar 2025 12:04:10 GMT  
		Size: 7.6 MB (7629801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cfc17aeebd04e699ae68666ed7dd409c873ce0ed9d26f383eccc08b1903e708`  
		Last Modified: Tue, 18 Mar 2025 12:04:09 GMT  
		Size: 48.4 KB (48361 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:6ad3e33a037c3ab595537a9c6c34082adc02807179fc2b6aa9486752a8b4628c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237579185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44274182eb047a8416191064cc67b2badf4dc2c0e7bd579da628de45f79356b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Feb 2025 20:06:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.1.32
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Feb 2025 20:06:56 GMT
WORKDIR /var/www/html
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Feb 2025 20:06:56 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
VOLUME [/var/www/html]
# Tue, 11 Feb 2025 20:06:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c06f79fb6bc8bc4b7af314064c1ca03229ebc25b6a5bed087db00ca9145a93`  
		Last Modified: Mon, 17 Mar 2025 23:36:34 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4b7293cd7af1c3125c4c07d13dc91fda89e6d5d6ddec748a9d80b062c9e4d7`  
		Last Modified: Mon, 17 Mar 2025 23:36:37 GMT  
		Size: 101.5 MB (101512618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef416291c48600932917a03cea92fa9f2e652a7c84be7264cabbd2e16d7c8774`  
		Last Modified: Mon, 17 Mar 2025 23:36:34 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:533eb01aeebef350aa80b4596f0e9d76c60db33941f7555376e907dc0fe87dc8`  
		Last Modified: Mon, 17 Mar 2025 23:36:35 GMT  
		Size: 12.0 MB (12002278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9422b72a3b7b4a81573743cfe66edf0797d4c3b996854ba74e15378382569af0`  
		Last Modified: Mon, 17 Mar 2025 23:36:35 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270e2f647aa20774b1acfe79599736a2ba40d6f2823b73c42313abd8a8642cd1`  
		Last Modified: Mon, 17 Mar 2025 23:36:37 GMT  
		Size: 27.8 MB (27840666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3e2d827b70b69d2079964daade8d1340add0e78d65bbac61b06998b7500d609`  
		Last Modified: Mon, 17 Mar 2025 23:36:36 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d8fb5772b29a910bd4eb9ae35c9df1dae39ec143d110746884aa38fba3dc62`  
		Last Modified: Mon, 17 Mar 2025 23:36:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b9a882b7dec198e9e3c08a1ea890309084d433d7ca57b3c124db58a43f5d09`  
		Last Modified: Mon, 17 Mar 2025 23:36:37 GMT  
		Size: 8.9 KB (8884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b47fddc9f5cd8527aa8358a5369c7ee0b60c4dffe5147ba689777168464afe6`  
		Last Modified: Tue, 18 Mar 2025 00:17:53 GMT  
		Size: 26.8 MB (26826214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f83a26b11555a229e2d8b5c84c3c3b906b86c25acefaeb39d25e595e8894463`  
		Last Modified: Tue, 18 Mar 2025 00:17:53 GMT  
		Size: 13.4 MB (13432361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edca03e8b96e2eef0556ab5466a5cbdd9f980b3df7afb5c9e3eb523b5f71a03`  
		Last Modified: Tue, 18 Mar 2025 00:17:52 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b521e007974f3a036171b0edd52980b1365179307533658b03b7016252065150`  
		Last Modified: Tue, 18 Mar 2025 00:17:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca736fdf9946c2aa0ddf7cc4be4fe5ada8beb6ba2e2823eac08cec6b6494a03`  
		Last Modified: Tue, 18 Mar 2025 00:17:54 GMT  
		Size: 26.8 MB (26758055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9f87c627b2cb5e19feaefbe4dae7486d5e72df8553f547e795c0bc71ed3b8b`  
		Last Modified: Tue, 18 Mar 2025 00:17:53 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f25a844478d7241517aa0c85c19f8e45ab1021c7de2dab832d24062f71ed1c4`  
		Last Modified: Tue, 18 Mar 2025 00:17:54 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:40050a915f4256834893f2a1a3d84fda76f50286c21375c4f746c6dcfa46c145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7622464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2668146d0592f52d13e8cefe6f65fa7c41a020604fee7d45504b4334ce8e793b`

```dockerfile
```

-	Layers:
	-	`sha256:b4e3da884890d0a2975b6d14aca07ae31672d233cc9d679ff17169b4942aecca`  
		Last Modified: Tue, 18 Mar 2025 00:17:52 GMT  
		Size: 7.6 MB (7574299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5017fb180966f9a0c5a67943113c9e47706b102f1ba6d47e5413ea097bf3164`  
		Last Modified: Tue, 18 Mar 2025 00:17:51 GMT  
		Size: 48.2 KB (48165 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-fpm` - linux; mips64le

```console
$ docker pull wordpress@sha256:849fb840fe61b84b1288159028366ee13ac086ec37f72df49c83c7abe9dbc280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.4 MB (213417504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b07a16fd3e43c216642ee622bec56d821b5d87f00a8c3be167fc2c97479c4a98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1742169600'
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Feb 2025 20:06:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.1.32
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Feb 2025 20:06:56 GMT
WORKDIR /var/www/html
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Feb 2025 20:06:56 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
VOLUME [/var/www/html]
# Tue, 11 Feb 2025 20:06:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
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
	-	`sha256:73dd5a9b827bf9f4c35d730b51b079c082a624aa95fba8af656a2b44319bf469`  
		Last Modified: Tue, 18 Mar 2025 11:27:14 GMT  
		Size: 12.0 MB (12000903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fa5a5d5d866957f0aa2d335c9585a375f7101e62e428a7281dede9dd18a930`  
		Last Modified: Tue, 18 Mar 2025 11:27:11 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906a989194e6f108b3005009d5ee85c7f526f982152e5222e171138dae63dcd8`  
		Last Modified: Tue, 18 Mar 2025 11:44:14 GMT  
		Size: 26.4 MB (26424266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:840916b74cc70405dcfce848053370bc7356e9a107f96db749796e41f1ef53d5`  
		Last Modified: Tue, 18 Mar 2025 11:44:12 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92cb8958941137b626ef222bd2e149cbfdfc0739fa1458e168fbaaddb13ee93`  
		Last Modified: Tue, 18 Mar 2025 11:44:12 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ef641226b32e562ea02aed2b1d7fe0e3810a0c8f66183163b522d5776aae20`  
		Last Modified: Tue, 18 Mar 2025 11:44:12 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd8eb0d94851c89fb87d2ecedde98bbde9d11b0b89fc1329750f8cc64d89b33`  
		Last Modified: Tue, 18 Mar 2025 22:30:45 GMT  
		Size: 26.2 MB (26152257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587a840ed90cdc10b3a5d66ed5ccee9e3077ff54a11c66415afa589cc3750332`  
		Last Modified: Tue, 18 Mar 2025 22:30:44 GMT  
		Size: 12.9 MB (12904696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228eb8dbb0ea081a97f88c2c42f31c971b3daf07c691bdfd5d33e0c5e9758e30`  
		Last Modified: Tue, 18 Mar 2025 22:30:42 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3490b7b19acacbae8582322e66144679f4fc95fc53ce13e3e81840689b9aee`  
		Last Modified: Tue, 18 Mar 2025 22:30:42 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cef668c665b0c23c9b8f5333c7236e744237de5a2b3d4134cd454117a8f068`  
		Last Modified: Tue, 18 Mar 2025 22:30:46 GMT  
		Size: 26.8 MB (26758099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f294486e2a274892cd339a845856d9d8ad93fad74631c5853c375954efd03ce6`  
		Last Modified: Tue, 18 Mar 2025 22:30:43 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9658a51844b3f8328b0913ca9d61a6eebda0f887d57c7a2ee8016372a2edf807`  
		Last Modified: Tue, 18 Mar 2025 22:30:45 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:2c35a04dd490d7cea304f25952e770773aa84ef04cca74877ef8b3ff0b36ec7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 KB (48060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f800bb43f0f15446c51bb0c9fa506fb6eb16a4f97216096a789e887e436070d2`

```dockerfile
```

-	Layers:
	-	`sha256:64abdcf27a4d78a70c4dadbc02edca2e4e94121abfabfea5bc54234354b9d989`  
		Last Modified: Tue, 18 Mar 2025 22:30:42 GMT  
		Size: 48.1 KB (48060 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:a84129f1f7fa8ee5a5e02d38b93555a132b4a14d1214b0a03b78bcc696f2a10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245555776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79125e745cd7c369b0702fa9f1d71d5a71a1daa5a8b6c9172b03aa498dd358a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1742169600'
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Feb 2025 20:06:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.1.32
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Feb 2025 20:06:56 GMT
WORKDIR /var/www/html
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Feb 2025 20:06:56 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
VOLUME [/var/www/html]
# Tue, 11 Feb 2025 20:06:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:89104bade2bef9a11eda15952361b42943ba7a21a6bc452862cf92faeccc17cf`  
		Last Modified: Mon, 17 Mar 2025 22:20:32 GMT  
		Size: 32.0 MB (32047814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40c9e444f13d4c7a03580cf188ef06ad94ffc13189161777e9ed5cf824f8ea7`  
		Last Modified: Tue, 18 Mar 2025 03:15:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef297c24191733a2fbe29ead5c53224c75c11b7ee0ba80b57b0b3898a33bbbf`  
		Last Modified: Tue, 18 Mar 2025 03:15:07 GMT  
		Size: 103.3 MB (103324904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d707aca2b2791bdef48c24201e181e34f312580cea3313c4c8b8cdfa4a82c4`  
		Last Modified: Tue, 18 Mar 2025 03:15:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a975490b00b2dcf69306cb6c86904fa5921ac25bbd59d08210382547ee8b069`  
		Last Modified: Tue, 18 Mar 2025 03:15:04 GMT  
		Size: 12.0 MB (12002638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49561e2e443be18e80c09cc9e02a46d30ceb6589d6376575d3da05ed07b7b02`  
		Last Modified: Tue, 18 Mar 2025 03:15:04 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9c6d2ce01b29e61e2bebf41bab4c1c7f0ce9b3f41e2025309158949b0414e0`  
		Last Modified: Tue, 18 Mar 2025 03:26:06 GMT  
		Size: 28.4 MB (28353899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab316551c26e162dcee62b003d7615b59ebb7955471091ecd1954d698191746`  
		Last Modified: Tue, 18 Mar 2025 03:26:04 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146e7f9a4d48c4499a43b1bec303e0c3af4a3ba8f9b097ee5f0134d274474c52`  
		Last Modified: Tue, 18 Mar 2025 03:26:05 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfbf845da78f549534a3b2b91577030431add3e6ae42af07aff5fc4d3e005fe`  
		Last Modified: Tue, 18 Mar 2025 03:26:05 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ed9c1a5f237428df8d7d5b0e4713a5ddb1626c085896ebb08d9d50b5a194cb`  
		Last Modified: Tue, 18 Mar 2025 05:50:01 GMT  
		Size: 27.5 MB (27477984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d802f5a2685058e7f3201415a97a3bf9ec41febcd223d29287651f3e0ba30eab`  
		Last Modified: Tue, 18 Mar 2025 05:50:01 GMT  
		Size: 15.6 MB (15573012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afb4c022d7b39d5e469c9bfa71f6e980a8411fb9d7ea55c1ebebe26f06feadc`  
		Last Modified: Tue, 18 Mar 2025 05:50:00 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eb4dee13b3e9a9cfade1c3b7a5c9d1a73b954143bfcd6a48cd3aabd9510d0ba`  
		Last Modified: Tue, 18 Mar 2025 05:50:00 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da059f914aba18445cfcd0c6b176eb02a50f3e81f7b482afe33a987d34e804d8`  
		Last Modified: Tue, 18 Mar 2025 05:50:02 GMT  
		Size: 26.8 MB (26758065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290dedacb3c3522f7bac5907c6f6b8eac895d3d1d087409f010ae70439537696`  
		Last Modified: Tue, 18 Mar 2025 05:50:01 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3864840e4bc62bfb344198ce7da4b84bfdc01ca1b36c1e66b640b2c91d5c92e0`  
		Last Modified: Tue, 18 Mar 2025 05:50:02 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:9f60b8f6c96b0c7531dac7bf545ede0d96a5b8082db4e0c96eaa15a0f681b280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7628102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff0bfbe36d34c1bcdfc3c06f8209620c42623f6ec0774ef6c17628ead3f3c8ac`

```dockerfile
```

-	Layers:
	-	`sha256:12e992407605b100c7a209b8e7b09e321df0f7ae10ca64631d9d09a4cd9fe965`  
		Last Modified: Tue, 18 Mar 2025 05:50:00 GMT  
		Size: 7.6 MB (7579845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f662a90c806935a3ba45b3e11b997a0fb403965fcb085c28fe5bad59e617f6c`  
		Last Modified: Tue, 18 Mar 2025 05:49:59 GMT  
		Size: 48.3 KB (48257 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.1-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:6243ece39c0ac44984155eb58f33c21558fa4bb63a18c8dfa43e0b90f622eacd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.3 MB (212319976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d769630abe6f7befde21dddbfbfeb4edcab89c5fc4479ce0a4ba42faac5b3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 11 Feb 2025 20:06:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.1.32
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Feb 2025 20:06:56 GMT
WORKDIR /var/www/html
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Feb 2025 20:06:56 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 	version='6.7.2'; 	sha1='ff727df89b694749e91e357dc2329fac620b3906'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
VOLUME [/var/www/html]
# Tue, 11 Feb 2025 20:06:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Feb 2025 20:06:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b260f9f21520ff4ef8ecebbd464f756c4b42eeef8d200ff3739e0360d36e011b`  
		Last Modified: Tue, 18 Mar 2025 03:15:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02ec70644549123b866d1c2182ff0cbc0649aaf062785663e3cf3f77c813173`  
		Last Modified: Tue, 18 Mar 2025 03:15:22 GMT  
		Size: 80.8 MB (80816102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a92f3c840861f6c757cffe1b678b36ac8639e938b70d826614eef6eda30939f`  
		Last Modified: Tue, 18 Mar 2025 03:15:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04cd78c670861e8dba9dbf8c573c92f62fa64cfb13a69d6e4e83261db9137009`  
		Last Modified: Tue, 18 Mar 2025 03:15:21 GMT  
		Size: 12.0 MB (12001634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01ca4498169940ebccbbded72739fd587ea0044446e1c9ba0df2b3a72763b44`  
		Last Modified: Tue, 18 Mar 2025 03:15:21 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257541a71ab09b17603550bcf7b28bb997d6adb584d2cbb30db3f2c7fc64e795`  
		Last Modified: Tue, 18 Mar 2025 03:34:40 GMT  
		Size: 26.4 MB (26449818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf07d343e82d2dd617b442b57c20594060c0042b96138b044e7abc65d255abc`  
		Last Modified: Tue, 18 Mar 2025 03:34:40 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57a8ca730b4193c9aeaed32bd8b1ed6f5982191f698714e9f0adbe01b9104b4`  
		Last Modified: Tue, 18 Mar 2025 03:34:40 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f1a3ff3f442492bbc59e9287bb962415a91a0252018d8338e7c99a70216fda`  
		Last Modified: Tue, 18 Mar 2025 03:34:40 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0aac93617223891c9652cf5f29ac4a3c372a4d8a95df464f8db49c63ff0cce`  
		Last Modified: Tue, 18 Mar 2025 05:24:53 GMT  
		Size: 26.0 MB (26011775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406358e514f5afb5aa5d4045829ad35561a35b8b91542cbfd389910f6666fc8e`  
		Last Modified: Tue, 18 Mar 2025 05:24:53 GMT  
		Size: 13.4 MB (13404052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac09ac2940428d8b3d175e6f73ebb00fe47aeaee347d9432b23a9659d95a514d`  
		Last Modified: Tue, 18 Mar 2025 05:24:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92388071d9b9aea09129e871691ad1a73f16485cfb18327ad76b89b1a93a6e5a`  
		Last Modified: Tue, 18 Mar 2025 05:24:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3505e2957f4adf300b2b2595e12f2337f16c4038a986d5ee47aa836ec6a99ce7`  
		Last Modified: Tue, 18 Mar 2025 05:24:54 GMT  
		Size: 26.8 MB (26758070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a962c6b320ad66299f56a01a2c95a89729f7e037728c2f9dcd62b33298600a82`  
		Last Modified: Tue, 18 Mar 2025 05:24:53 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a357232351c6bd803bb8a181071b92fb51071d2b7246767ed98660220461bc`  
		Last Modified: Tue, 18 Mar 2025 05:24:54 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:5c0fe5b91bb9760c7e56d94a134fdaa940c7abbbaf55a5532aae84249ecc21df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c282e71de8a317ec28053b14e4f5287497c93d61e04f65344ba53ce960ae0d`

```dockerfile
```

-	Layers:
	-	`sha256:224bac5fd85a8a36d628af9432d6738332b4565dc7ccfb0b36efc539afacb24e`  
		Last Modified: Tue, 18 Mar 2025 05:24:52 GMT  
		Size: 7.4 MB (7431173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44d0111794479a5af52fece0fec4a8204ea1ecedc3ea8aec1816ef99e8a6d8d6`  
		Last Modified: Tue, 18 Mar 2025 05:24:52 GMT  
		Size: 48.2 KB (48197 bytes)  
		MIME: application/vnd.in-toto+json
