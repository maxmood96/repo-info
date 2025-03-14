## `wordpress:6-fpm`

```console
$ docker pull wordpress@sha256:7cdcad9845198f08d384f0de18fca2563d36fa5ecf84458d26259d8ac3705d97
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

### `wordpress:6-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:cc1836a81d90bd81ea540882db9226056476d2b005e36fd862d320475abe7721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243010041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd6a13d23df04af0222474ce332f55320ec26ab8ee1ad000e33975e19515c4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.2.28
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e62b3d46baa9bc185300384481ac06d218c85e228f704539d64af331c12078d`  
		Last Modified: Fri, 14 Mar 2025 00:51:48 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9938624012b190179877d40c34452f1745794aff651bd429ba056448302d68a`  
		Last Modified: Fri, 14 Mar 2025 00:51:50 GMT  
		Size: 104.3 MB (104345410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a1a077f656b2785bd914aa5f9c015facbe3aed90d7a1175e6ec5d937f09d58`  
		Last Modified: Fri, 14 Mar 2025 00:51:48 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32a66acd042939dda8e19905a00fc4f95bf83e01a1dd6fc6dba04a466b332c0`  
		Last Modified: Fri, 14 Mar 2025 00:51:48 GMT  
		Size: 12.3 MB (12257314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd43abb95b3b99dd4e139495aa6e76c2b26447ef6229287be9773c2a2c340c18`  
		Last Modified: Fri, 14 Mar 2025 00:51:49 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb86a29b2b8faf0433392f3a3b2d0242070998b471fc880599b914330898614`  
		Last Modified: Fri, 14 Mar 2025 00:51:49 GMT  
		Size: 27.6 MB (27587419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2606acf95d8bde06bcc801baf35366b588a3cce6a753fe79171db87dd218f6f6`  
		Last Modified: Fri, 14 Mar 2025 00:51:49 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc47f3a2f19fc99c8435ec6e0ace73dc3c8be1643892c41f734df21609a4656`  
		Last Modified: Fri, 14 Mar 2025 00:51:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7a6062a855fab6a556006470fdce0228493e7915a768a078d26381aba23486f`  
		Last Modified: Fri, 14 Mar 2025 00:51:50 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528fffd76372bda84d50a9f28655f8b01cba53c526de19d92c52be87edb4963e`  
		Last Modified: Fri, 14 Mar 2025 01:12:28 GMT  
		Size: 26.4 MB (26374108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754b32c31b1eba49c23459ffd50fb42afa1d6456fe2bfec98f31fd8b88bd2706`  
		Last Modified: Fri, 14 Mar 2025 01:12:28 GMT  
		Size: 17.5 MB (17450652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa900260810127674f095c20371af4f46a6fedb1a4c5afae21eb7401c2158db0`  
		Last Modified: Fri, 14 Mar 2025 01:12:28 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de332cc90896768ea7696cb415314ec8ebf70693eee728b4552544743d9e516`  
		Last Modified: Fri, 14 Mar 2025 01:12:28 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c9be1cb9d527881ffdc69bee908f5415e378dffc644b8c8a74e1ff79e949d6`  
		Last Modified: Fri, 14 Mar 2025 01:12:30 GMT  
		Size: 26.8 MB (26758065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec83ad3f927839e467168b52a342dad7ae3a55baa5251396c9775fe2b7d7696`  
		Last Modified: Fri, 14 Mar 2025 01:12:29 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893d20f0024f3c63637fd1eda11bb2689960ca1bc9caaf40965cc6d1bd7c9865`  
		Last Modified: Fri, 14 Mar 2025 01:12:30 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:fb2022d855b5360e7d0ea4c86cfe1d4566488e232bc3af3e5fe4201f3003ef2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7651669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310dc57b62e8cd7be54552986e9131cf00dfb783d89c6adb9383bbf87d0a36f5`

```dockerfile
```

-	Layers:
	-	`sha256:b5771c9fb2c4ab07687cd39eb94f451c1322fdb3bf922d5545385c5455d713bd`  
		Last Modified: Fri, 14 Mar 2025 01:12:28 GMT  
		Size: 7.6 MB (7602248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ebf5b8d27d23bc946133916fba75ccca8de7c49d218a8dacc3b79e5186f3711`  
		Last Modified: Fri, 14 Mar 2025 01:12:28 GMT  
		Size: 49.4 KB (49421 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:e203f6213790e311962d586ba34e2e929fa22f1edf035ae34f265b75de9f5f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211931036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054fe24bb90c320741a6fbc161ab63a3ae1312f0619d1b07cd1c506a206bf5dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1740355200'
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.2.28
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:174fac8933fd96ad2b4d9895010a9ca8188774a0fc61d763fbf1e3c87172a5b1`  
		Last Modified: Fri, 14 Mar 2025 00:17:47 GMT  
		Size: 12.3 MB (12255703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4587da7b68faab1496da9e291bb6c94baef8d06f3421d63afe1e030a34b954`  
		Last Modified: Fri, 14 Mar 2025 00:17:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e787692425ce9c5b94a54a76d7be0dc8c9248fe49116c88affca601e87a140`  
		Last Modified: Fri, 14 Mar 2025 01:21:45 GMT  
		Size: 26.1 MB (26086910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbba49c677c0b55142ea8238fce0d47a9b81da4967a8c6dee28b45241cf84c96`  
		Last Modified: Fri, 14 Mar 2025 01:21:44 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b55b3f69c0c5b87bc560f356072b6fb7980dc02816addfd2411f76f80551fc`  
		Last Modified: Fri, 14 Mar 2025 01:21:44 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aac5a740a4680921dbf093b1c0a3b64f4effb8de42c318dc89aa36b4b717819`  
		Last Modified: Fri, 14 Mar 2025 01:21:45 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0729f7272df23faa8cfe45c8482e62eaeedc0783bb60a79de67141ba873187`  
		Last Modified: Fri, 14 Mar 2025 02:51:41 GMT  
		Size: 25.8 MB (25823191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a5dbea65da593df69f2617aa05a70c5685658370e0a729566ef3ec641fd643`  
		Last Modified: Fri, 14 Mar 2025 02:51:40 GMT  
		Size: 13.3 MB (13255504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1a31fa476d4d6afbcec0554e56a7f16015355f989c26aaef7ee4ad0b7d01f8`  
		Last Modified: Fri, 14 Mar 2025 02:51:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9785f50329212ca0260f20a8b010e267aee5c3a75b9973a7adb6e1f339b233fb`  
		Last Modified: Fri, 14 Mar 2025 02:51:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e6e76fcc5fed4d09500820633c42da5e018399281e71aaa8eaf158688ad8dc`  
		Last Modified: Fri, 14 Mar 2025 02:51:42 GMT  
		Size: 26.8 MB (26758110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b177ec7e4186b0bdff1d7452256c6c5e9085aba62f69190d62dbb1733d4644d`  
		Last Modified: Fri, 14 Mar 2025 02:51:41 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db20626989bffbac3259f9d4338be805a7e00d920d6d7751e16470a28559f99`  
		Last Modified: Fri, 14 Mar 2025 02:51:42 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:5d4bf0cd8fe75a488debe69c2166408ef72d71fde7be939126af00e96b7ee21c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7457986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4d22fcc88172961a55b6ec3684eb240f993e3dc9fe7ff282d59339132e65a01`

```dockerfile
```

-	Layers:
	-	`sha256:be08c42312cacacf10fed4af434ae082272ce1b5404283bd793667c6aa150ca2`  
		Last Modified: Fri, 14 Mar 2025 02:51:40 GMT  
		Size: 7.4 MB (7408413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50c7a0069d7a5b05522aa82459f623808f594fb1655dc37beb6a93fba66828e3`  
		Last Modified: Fri, 14 Mar 2025 02:51:39 GMT  
		Size: 49.6 KB (49573 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:0d6383be755ad009ea01402717a10e3980c253b8be2c0d6e43102c51c8072be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.5 MB (201491658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cc848ce350a1369f96e64dedae7272e5f5a038ee58cee33e9b02f28d72f89a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.2.28
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:8cd292a4a13daa7cb1bb02b5239391a1bf6e5b2a51b7f308c154b00d7cdad293`  
		Last Modified: Fri, 14 Mar 2025 01:30:07 GMT  
		Size: 12.3 MB (12255707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a369bd6b33fc90ed98625cb023a271ae762566f55e6db7d5a1855b75981d3aa`  
		Last Modified: Fri, 14 Mar 2025 01:30:06 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e770874e1c2fedb62da4ac1dad703395c6ff98844ff540a1bb067ad019aa8eea`  
		Last Modified: Fri, 14 Mar 2025 01:35:41 GMT  
		Size: 25.2 MB (25194955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc40a33224ac137c40c67fb59f5da4ecc33ef905b66a280be3f4f8319f43f42`  
		Last Modified: Fri, 14 Mar 2025 01:35:40 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380a235120ac91ff9b8d7c81b3fac77969236409230b0e67525f012a4f655c88`  
		Last Modified: Fri, 14 Mar 2025 01:35:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268b04975060b6494c22108ad89e386e2817ceadda8f988d3a6a91dd64e0697e`  
		Last Modified: Fri, 14 Mar 2025 01:35:40 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b403ffcad28fa217b1c921278cf86f4ec70f2e77eb781c90deee27ec3daad5c`  
		Last Modified: Fri, 14 Mar 2025 04:14:35 GMT  
		Size: 25.2 MB (25161841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640b2ebd13211af51aa2e8a0a7137b5dd95a4473e8652d6ee90b632b9e87af54`  
		Last Modified: Fri, 14 Mar 2025 04:14:34 GMT  
		Size: 12.0 MB (12020670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85268f273f7d61b3259f69a572e3e01451b839c0697e0bffa08a6a4d8e95d7d8`  
		Last Modified: Fri, 14 Mar 2025 04:14:34 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5e1751895595d99fca895be069d52acfae8465241e58cf8921aeba0d933dbe`  
		Last Modified: Fri, 14 Mar 2025 04:14:34 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33dc407e28fef787b7e799e90ecd21d31a5d49969411af1da88e50ce2615ee40`  
		Last Modified: Fri, 14 Mar 2025 04:14:36 GMT  
		Size: 26.8 MB (26758108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc67ce1a0d327162d8797ba8243db9e39ddc30fe8d486605dc286f3343ae13e9`  
		Last Modified: Fri, 14 Mar 2025 04:14:35 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc666e1800b910497da30bf3bbb2591704578d7f8ccaf0b85131f743bcebe54`  
		Last Modified: Fri, 14 Mar 2025 04:14:36 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:db41631cf04fd03479220e40d68381da27118ae7af1e60411ad2194ee5f0fb1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a8a0962151707ad2b6a392b50e932e7e67c5c59e8ed648d74e1af86c0720f7`

```dockerfile
```

-	Layers:
	-	`sha256:15865a68929f4af651b2226f4a8a4e8605567f1fa663c76baeb76af1c615bea6`  
		Last Modified: Fri, 14 Mar 2025 04:14:34 GMT  
		Size: 7.4 MB (7413079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5508f887a1ea1581787052eac527f31b1397eb10c23232f3db7e8e59cdeae1b0`  
		Last Modified: Fri, 14 Mar 2025 04:14:33 GMT  
		Size: 49.6 KB (49573 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:aba32ac2647a566fbdc5686d41901e5c5425484da8e13ae5c3c60d6bf7a26620
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.8 MB (232812589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99bf57256af7955a9b3132d25e3f6b2078c4e971f556d1a1b0aacb54c871edf6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.2.28
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:4ac4232823be0667c82b09e794eae937ac24dda36546c7ae38d52080401a0653`  
		Last Modified: Fri, 14 Mar 2025 01:22:19 GMT  
		Size: 12.3 MB (12257233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21523d24049a2c116a9d8d26d1b9c462f11346258e50e227b6dd6f5fa0e4c78b`  
		Last Modified: Fri, 14 Mar 2025 01:22:19 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a3f83ad69a4a708ff1b6bdfa0ab1ff3794d99f7f70d67f09c02170f438cf52`  
		Last Modified: Fri, 14 Mar 2025 01:26:11 GMT  
		Size: 27.5 MB (27549576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8ebc55aa4a9d187acfc67ca269db5955831d0ba92097cb36b2438a1b477c60`  
		Last Modified: Fri, 14 Mar 2025 01:26:09 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35b089c64ee6309ae23275a3e06ef5b4e72bfdcd93b7065edd603b98c50885d`  
		Last Modified: Fri, 14 Mar 2025 01:26:09 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640c64ee926f7a87025196c1fdaaafa650ead8b5826de4adc0f31ee065809f20`  
		Last Modified: Fri, 14 Mar 2025 01:26:10 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4860f1a12adff44bff846ee867b81743a474f7e6d2681deab8255df5c8d040a0`  
		Last Modified: Fri, 14 Mar 2025 04:55:32 GMT  
		Size: 26.3 MB (26287573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333e6d1882db7cb2cd7b632064753c8813967d5584ebbbfed4a4098b601c5de3`  
		Last Modified: Fri, 14 Mar 2025 04:55:31 GMT  
		Size: 13.8 MB (13763451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fb44e55d888be9ff898826310bd95e2ffd83dd5d04b794c7b00dc326dc863f`  
		Last Modified: Fri, 14 Mar 2025 04:55:31 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d894732448b6aff3dc4d8708402abe4f0bab57d166c25883aa77d1efdc76a9`  
		Last Modified: Fri, 14 Mar 2025 04:55:31 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c4e597902e4f2b25d2d26d01157a3fd4f0d0ab822873532b6e8a0ca7db2c09`  
		Last Modified: Fri, 14 Mar 2025 04:55:33 GMT  
		Size: 26.8 MB (26758095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f189f68584e8ea92ec83e4a336ad8b2fe747405c106cbddd9667d425373d18fb`  
		Last Modified: Fri, 14 Mar 2025 04:55:32 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad2840be34e5bf6ca07414e2e3ffc3a3765102cc1d018ba059d66214232f9f3`  
		Last Modified: Fri, 14 Mar 2025 04:55:33 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:1f31436910e761ef40e776ed3231f25c5cf1ef4f2c07fec494f34574ab820410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7680674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b21712452e60323f169139c9d2acfb081543078113f56c8d535e6b749182fa0`

```dockerfile
```

-	Layers:
	-	`sha256:4bb4668f6a1f95419da8b0839ffde5202a3aa13cf05ae4a91803f583bd108140`  
		Last Modified: Fri, 14 Mar 2025 04:55:31 GMT  
		Size: 7.6 MB (7631049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e5ae7bc2603f82c14fb2207f76a5c8bd05d5926e06712b956559e19cf1beacb`  
		Last Modified: Fri, 14 Mar 2025 04:55:30 GMT  
		Size: 49.6 KB (49625 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:f106d7eb1048a813340d66c2ba1af1e5199ce7e9bbc8381f8abe9b5948d2243d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.2 MB (238151265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ca439e7c03b7e0f2371650628717fde486c833de4af1f661fae3900975b1e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1740355200'
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.2.28
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:a424c1d96f8a4c2d56031254051a822634b1b977ca2bc56e7fd2adc3e742703a`  
		Last Modified: Tue, 25 Feb 2025 01:29:49 GMT  
		Size: 29.2 MB (29194590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2876a8fd03769fb93922a836819ad1b10231ada321f7ae8eb283173fcce453ef`  
		Last Modified: Fri, 14 Mar 2025 00:19:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22af02313e120f84582b4a654c5bf54bc763b0e07dee33578e0b4c169891f4bf`  
		Last Modified: Fri, 14 Mar 2025 00:19:15 GMT  
		Size: 101.5 MB (101513589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0703318fce1ff5cbb1a8e2515eeeb044a3c1a3bd69ea6b26f1e60fb3c8b954ef`  
		Last Modified: Fri, 14 Mar 2025 00:19:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bce9d4f50c61759bf7430f7c7371babfb14f6c59c1ce884040b1b535b494a02`  
		Last Modified: Fri, 14 Mar 2025 00:19:13 GMT  
		Size: 12.3 MB (12256533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7491da8ebcf86f929ce2c4f24aca117cc80e12a9e10b8ceb6db363b0bb9fb0`  
		Last Modified: Fri, 14 Mar 2025 00:19:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1816fb197a480a61d5331d80ed81134b0f9bb51897c54129d9943a70764a99`  
		Last Modified: Fri, 14 Mar 2025 00:19:14 GMT  
		Size: 28.1 MB (28119139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:410b26fbdaaa497925b7d22f9b2eb40cbc19b7dafa96f59fd96c592c17e4821b`  
		Last Modified: Fri, 14 Mar 2025 00:19:13 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a750ee7655d0ac1d3879ec63c216c6f43a99c9787d2d04cdd2a85da7dce0ddf6`  
		Last Modified: Fri, 14 Mar 2025 00:19:14 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d38e5388a4483a39c2abd96432b41798d064fd7a43deb5693dfc802559fcf2b`  
		Last Modified: Fri, 14 Mar 2025 00:19:14 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89afebe94934939711881ad068c5d24c741057a8e5067903db1a0707c3b87c6d`  
		Last Modified: Fri, 14 Mar 2025 01:12:42 GMT  
		Size: 26.8 MB (26826216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc92646df56a954c1539fa5bd4892b7afd4e150d896e359f3ee3fa76aa29430`  
		Last Modified: Fri, 14 Mar 2025 01:12:42 GMT  
		Size: 13.5 MB (13465308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17108d33b3d19ac3bab479a129f8633f36ead3fb65334f1f2cf14ce1b77d0de4`  
		Last Modified: Fri, 14 Mar 2025 01:12:41 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da0eb6d7c4af900e6dbf0cfb84a60d458affab9b363e58c757b9a360976985e`  
		Last Modified: Fri, 14 Mar 2025 01:12:41 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0922cabd351c39ce82d52eebd28c7eb06429f416918e8390c754d7a5c5d945c`  
		Last Modified: Fri, 14 Mar 2025 01:12:42 GMT  
		Size: 26.8 MB (26758108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9dbad07a25b41d947538ce9447cb78709c8ab7b4e83b02f09af1d726391806b`  
		Last Modified: Fri, 14 Mar 2025 01:12:42 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262a4be5b61a70fb1f1858f00409d2f58d9e94a8d5490f2b6d47a0216837cb02`  
		Last Modified: Fri, 14 Mar 2025 01:12:42 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:bba6ef206c97e05261f75dfb26b0a6a77a4cde3d741cec1d9daec23f2dcfb076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7624840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0040942a293c25e8a719b6674fe6b9447aaf0c404df7c8f7891cbdf3607e48a`

```dockerfile
```

-	Layers:
	-	`sha256:3282372e005fdac7bb5b8f76e35926f189c37d0682c624ce7aa168d627fe5d81`  
		Last Modified: Fri, 14 Mar 2025 01:12:41 GMT  
		Size: 7.6 MB (7575479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e797991639412a0e84d0028f73e0981beffe19b7aa2c14a82d631f68eb12ced8`  
		Last Modified: Fri, 14 Mar 2025 01:12:41 GMT  
		Size: 49.4 KB (49361 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm` - linux; mips64le

```console
$ docker pull wordpress@sha256:9f6c36081612c5859cfc8ed4bcae9203d8292e674514ae0aa873371d0708eaa5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213971342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fa1dcc87d99efb38b0a37513c2b3b016874def8e6b21685eeba7171acc62d3e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.2.28
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:be5e465553f8e6f88a155a82c9fbb8653291976a39dd74f3861791dc4ca1bd24`  
		Last Modified: Fri, 14 Mar 2025 01:51:49 GMT  
		Size: 12.3 MB (12255331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:286a3e02c77729b40d19312ef2ff51fb7fa57da178d19f86b90871cbd9c31a39`  
		Last Modified: Fri, 14 Mar 2025 01:51:47 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b954132be3b27fe3e7d2880c1d8e4a12341887ccd2df47baa8f6b837a7592f2e`  
		Last Modified: Fri, 14 Mar 2025 01:51:50 GMT  
		Size: 26.7 MB (26692165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d62bebb4ee1daac881baf11e482cfa5e3789b2c525ea4c40922d195b5626f4`  
		Last Modified: Fri, 14 Mar 2025 01:51:47 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e26951b05da5b647ffc72c1c382ced601a53db7eb49a62a78f4d762effba48`  
		Last Modified: Fri, 14 Mar 2025 01:51:48 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efc49f8653bfa106f950b85d26cbf2ce001e1982a1c9583f23d24552377cd1f`  
		Last Modified: Fri, 14 Mar 2025 01:51:48 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96354c3f949f5d6d03a828d422e8a4fc93b52d127bbb3aa4fd72bf2495f4d58`  
		Last Modified: Fri, 14 Mar 2025 07:36:52 GMT  
		Size: 26.2 MB (26152131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2f7d9f4efb461fd83b2c1da35981bcfe6ec3966b2ef56057e3c94af054254a`  
		Last Modified: Fri, 14 Mar 2025 07:36:51 GMT  
		Size: 12.9 MB (12933437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed63d50c05f448934491491ecd36e90a40b64ef7b64ba35b30c2083249e307c`  
		Last Modified: Fri, 14 Mar 2025 07:36:49 GMT  
		Size: 367.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb9ef73ec3312a9284d28e1c9cb53b006ba02472813150866be2cdba28b982f`  
		Last Modified: Fri, 14 Mar 2025 07:36:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b90a0a34e56584b0052b92af2195fc1a049873fbde34dde92ef0ada7f7b3ca`  
		Last Modified: Fri, 14 Mar 2025 07:58:28 GMT  
		Size: 26.8 MB (26758086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a30fc5550b289225f4352e120875a59d969d7a09a4f8524d96e1aadfcf6dc29`  
		Last Modified: Fri, 14 Mar 2025 07:58:26 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799f3499a74113703b8b416aa97cc895e2705e1b1334ff007485099d57bed4c8`  
		Last Modified: Fri, 14 Mar 2025 07:58:26 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:3011ac08ac9212c623b18f533ee24b770be42cb9b0e82f0b3d932d20e8c0c766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 KB (49311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a110fe21d421425729d5702be1d52bf59b089fc3ebc9786e88c4349de61d3675`

```dockerfile
```

-	Layers:
	-	`sha256:2109072603b52a0db12e3aca78375aa6c217e8064283eaffd5f2d00f0ca4970e`  
		Last Modified: Fri, 14 Mar 2025 07:58:25 GMT  
		Size: 49.3 KB (49311 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:9920f5af351c0ee67df816c805768a3424bc34b644de20430f0ec64c60258eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246145074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69312038d96901082ee64620c9e0b3ac1d96ed4f6714545b5e95e0bc9af2dcc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 11 Feb 2025 20:06:56 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_VERSION=8.2.28
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Tue, 11 Feb 2025 20:06:56 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 20:06:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:0b183a9e9a626652b70cd5c8539551c8cb640af571a1c9042e0132f037d4b647`  
		Last Modified: Fri, 14 Mar 2025 00:29:55 GMT  
		Size: 12.3 MB (12256822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e56b8480c0833bf885706daaa24ae51671535d736d1bd6502f4ec24bee98fdf`  
		Last Modified: Fri, 14 Mar 2025 00:29:54 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88581c8d587c4893c5d0e4f3ec9f4da6276370c261bf429c722590c5a22c891`  
		Last Modified: Fri, 14 Mar 2025 00:33:48 GMT  
		Size: 28.7 MB (28651590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d060d61f8218819b5d303c6753fc9b191fdbb4217767776b6b827de24183cbe`  
		Last Modified: Fri, 14 Mar 2025 00:33:46 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af774f56e0b9582a37b1689788bc10d7be95ddf0f7e9f52f79edfba6c4224caa`  
		Last Modified: Fri, 14 Mar 2025 00:33:47 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9017bee2d3c3c1b999a96f6729cee863c91f221ddcaec49b3087c6a6e07f43`  
		Last Modified: Fri, 14 Mar 2025 00:33:47 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4bc850b9badb3c2defbdd2848e200f8b34df3dbe7447688a383654f4c0c1ee`  
		Last Modified: Fri, 14 Mar 2025 03:04:20 GMT  
		Size: 27.5 MB (27478170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40c589c22329e35e2b71bf0d9b4399f4c23fc2a51298086027157d4843bb638`  
		Last Modified: Fri, 14 Mar 2025 03:04:20 GMT  
		Size: 15.6 MB (15606742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54712efe643996ddbce26d7d3daac933af287dba0544ce6997e123ace8284060`  
		Last Modified: Fri, 14 Mar 2025 03:04:19 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e02b83fc6962c3d2c33026c403e80705ca8ba4ea7e02f296c00a67d542617dc`  
		Last Modified: Fri, 14 Mar 2025 03:04:19 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d47329c4314aa4f2d717389102bc31597c4ab9b3cedb8e87ececbe67b897b0`  
		Last Modified: Fri, 14 Mar 2025 03:04:22 GMT  
		Size: 26.8 MB (26758110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5af997ae0f102f039a749129b96057b2657728af0d9428c12fb7903dbfb9ea`  
		Last Modified: Fri, 14 Mar 2025 03:04:20 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4ced945bb7e90c1adc03c523ff7b0c28aba801c67bb6e68722f1a33f7fd790`  
		Last Modified: Fri, 14 Mar 2025 03:04:21 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:f5a249a8dbf5f0bf42e31b0e7089fb408f5c48182c041e5fb5617c70df73e400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7630565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6716f1be1c532690eee70c226037d430e5df37e5a5893efbd43c5f2b43acb5`

```dockerfile
```

-	Layers:
	-	`sha256:dc3771a257e8a6cc8487a0b97dfc6d9457131a45fc0d0b39395b115846ba135f`  
		Last Modified: Fri, 14 Mar 2025 03:04:19 GMT  
		Size: 7.6 MB (7581069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b4e16cbe54b35de5e7443ab359727c94c19cdf8b4ab81702bfdc68c363b8e5`  
		Last Modified: Fri, 14 Mar 2025 03:04:19 GMT  
		Size: 49.5 KB (49496 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:78f51bf9d68dd33d4bbf92115ba4cdcba7dde0b759156f089ed7ca1394ee3db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212872446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fed2e379f3dafe35a7533db1607918ce2f3050bec0f14fe7acc78b0469a9242`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 16:49:54 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1740355200'
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 16:49:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_VERSION=8.2.27
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.27.tar.xz.asc
# Thu, 19 Dec 2024 16:49:54 GMT
ENV PHP_SHA256=3eec91294d8c09b3df80b39ec36d574ed9b05de4c8afcb25fa215d48f9ecbc6b
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 16:49:54 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 16:49:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 16:49:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 16:49:54 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 16:49:54 GMT
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
	-	`sha256:3eefde14b579084aa246cf00dc6c854838126943c1094713b3710e7a85c8faea`  
		Last Modified: Tue, 25 Feb 2025 03:16:07 GMT  
		Size: 12.3 MB (12259115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3772561ebfedc809537ceabefccf160aec0ca4f9fe42a52bd9f2e433af73811`  
		Last Modified: Tue, 25 Feb 2025 03:16:07 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacae8a8bbc34d5cf6833dc557cb102d185e1ec4a6c72871af7bc2f647a2e177`  
		Last Modified: Tue, 25 Feb 2025 03:23:03 GMT  
		Size: 26.7 MB (26702882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82897955807eab3e04eb59e46a994ab97e5d54ddce45b459484cd88f6aea1dc6`  
		Last Modified: Tue, 25 Feb 2025 03:23:02 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b456e59cc7c7306ef948877393c6967e5627d0867930390cf28e3ceb66cc800f`  
		Last Modified: Tue, 25 Feb 2025 03:23:02 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682ead698671721de7709de77be4f3f939a2b71bd50ed23cfd7bf4d386c0c652`  
		Last Modified: Tue, 25 Feb 2025 03:23:02 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8222c742470e2eef9fd87b6fcd640bf8020741eaaf5f5198d3ab9215e08f73`  
		Last Modified: Tue, 25 Feb 2025 07:10:02 GMT  
		Size: 26.0 MB (26011878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508ddf90d2f3b3dbf67be2106a1d8f5bb3d0a4c6c2370b58ebce4e0ad01f8d0a`  
		Last Modified: Tue, 25 Feb 2025 07:10:02 GMT  
		Size: 13.4 MB (13440754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8ae03c83359cbdfe712f389a53ca82f95029dabb8775e15fb20cfa6eec495d`  
		Last Modified: Tue, 25 Feb 2025 07:10:02 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e71380cdf3d88456a432841e7fc6dc6a0414c62db1b50150c03096fc245466`  
		Last Modified: Tue, 25 Feb 2025 07:10:02 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec38f86e63cfdd79f6a0062a4cfe0206c82d66919adf00c09aad87a5c92b09e5`  
		Last Modified: Tue, 25 Feb 2025 07:10:03 GMT  
		Size: 26.8 MB (26758105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700fb76b691af2ed5980553657fd6323ec6615f1e87520c7ae028b571a44e994`  
		Last Modified: Tue, 25 Feb 2025 07:10:02 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05cd76081be1b2abf863cb37462c725ded111b2dd55c2533969d44f5fb0d1c6`  
		Last Modified: Tue, 25 Feb 2025 07:10:03 GMT  
		Size: 1.7 KB (1720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:1e3127ae1f875bdbf43a2269a75529263f7535a87f2e0187276e3affde141fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25887a63abf233da2376e4869c088aaca94781ecdb85656528417b4f20c363f`

```dockerfile
```

-	Layers:
	-	`sha256:0a13c52733234371d4ef317cfd60c684f2f9714c82d6de276bab0a16109935f2`  
		Last Modified: Tue, 25 Feb 2025 07:10:01 GMT  
		Size: 7.4 MB (7432373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1bd5181f9f853009fc64004a8ee19ec4be1dd34f82acf72d72d37c8a52aa2d6`  
		Last Modified: Tue, 25 Feb 2025 07:10:01 GMT  
		Size: 49.4 KB (49413 bytes)  
		MIME: application/vnd.in-toto+json
