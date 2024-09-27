## `wordpress:6-php8.3-fpm`

```console
$ docker pull wordpress@sha256:86efcebe52f5e2e861fa2c95e59706fe9c4323e6928e8161976e2edbfe3cb765
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

### `wordpress:6-php8.3-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:43644eeac85e6e201590723629b374c624cc790d8b556602fd010f0dd96e6065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.6 MB (242607592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a6bb0a07cc6ff842a1c6813134dc29083ac0de34909a01bfba705f7a9b0d6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 12 Sep 2024 19:33:49 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Thu, 12 Sep 2024 19:33:49 GMT
CMD ["bash"]
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 12 Sep 2024 19:33:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Sep 2024 19:33:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 12 Sep 2024 19:33:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Sep 2024 19:33:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Sep 2024 19:33:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Sep 2024 19:33:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 12 Sep 2024 19:33:49 GMT
ENV PHP_VERSION=8.3.12
# Thu, 12 Sep 2024 19:33:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 12 Sep 2024 19:33:49 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 12 Sep 2024 19:33:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 12 Sep 2024 19:33:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 12 Sep 2024 19:33:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 12 Sep 2024 19:33:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Sep 2024 19:33:49 GMT
WORKDIR /var/www/html
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 12 Sep 2024 19:33:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 19:33:49 GMT
EXPOSE 9000
# Thu, 12 Sep 2024 19:33:49 GMT
CMD ["php-fpm"]
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	version='6.6.2'; 	sha1='7acbf69d5fdaf804e3db322bad23b08d2e2e42ec'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
VOLUME [/var/www/html]
# Thu, 12 Sep 2024 19:33:49 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Sep 2024 19:33:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07fc0890b857ec241446d5da032bf36da2a006ce8868ba150a76a1ee16772b39`  
		Last Modified: Fri, 27 Sep 2024 07:40:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:141aa7d58c576d5efbf995cfdd139044be15add60b2f0e5f7b295fdc4cc511d3`  
		Last Modified: Fri, 27 Sep 2024 07:41:08 GMT  
		Size: 104.3 MB (104345685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2720d4bca8b3db19acbea04618296e463e4cde1df16c277954505ad4e50893eb`  
		Last Modified: Fri, 27 Sep 2024 07:40:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8962688a93444367055b9b5efaa2bf2390fcf6504c24bd4ae2fafddf0848f0a9`  
		Last Modified: Fri, 27 Sep 2024 07:43:29 GMT  
		Size: 12.8 MB (12807811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b6fdd4f599402cf077b581d0c7e8fd6380e2d66b10a64caffaf2a4bf1b4ec7`  
		Last Modified: Fri, 27 Sep 2024 07:43:28 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7a22a3639cd01da730fb0f3edb7c3a9fdc08fe560a9ada1f45d541e04581aa`  
		Last Modified: Fri, 27 Sep 2024 07:44:35 GMT  
		Size: 28.0 MB (28015701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6eb7e247b37060b5b7380b029c0449ea5d785889b4c1125e05b7be44a433691`  
		Last Modified: Fri, 27 Sep 2024 07:44:31 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0b8c1af4c25e4064e7373e8c65f746567d313110b61ad8820f8cd1b406ecd2e`  
		Last Modified: Fri, 27 Sep 2024 07:44:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22e6287c8b7631a52ce5cb44b6c0d030e1fa6274ad217359f2f2877032ac8ce`  
		Last Modified: Fri, 27 Sep 2024 07:44:31 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab74a2db12fedb4fc33327ba1688e90ea3a6b8e61a3c32c3741f93a4ac1589d`  
		Last Modified: Fri, 27 Sep 2024 07:59:15 GMT  
		Size: 26.4 MB (26376523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad001e949f73e8fc1634e7a32373656956e5f1fb6e621a695ae1f5d582e5ba7`  
		Last Modified: Fri, 27 Sep 2024 07:59:15 GMT  
		Size: 17.5 MB (17453180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3a29dbb7c9a52fa71771bbd2d8af0a6cfb09445341ae5a68ddd259cc68fd9f`  
		Last Modified: Fri, 27 Sep 2024 07:59:15 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13202b5b3cce4e41d7286840989a0a177f845ea0aa8d1d5a5d06e7b6ac10f9d2`  
		Last Modified: Fri, 27 Sep 2024 07:59:15 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefe01ca70344f1c38a500bbb70a8b942f8c059bc0a38322533784abaab4e2b0`  
		Last Modified: Fri, 27 Sep 2024 07:59:17 GMT  
		Size: 24.5 MB (24464774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c4249466cecee340911d3aca49d321bbddc3e5bab344cf284d82263bfb4cb9`  
		Last Modified: Fri, 27 Sep 2024 07:59:16 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca654ae407ad094a9ba107d5d61344a5fc82381436bf3ca8eab905295dd89099`  
		Last Modified: Fri, 27 Sep 2024 07:59:16 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:b5951682a3fc0037e306b381c02b9564591d14b9f63285662c1aae0c43b54d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7631985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08916f26e293180f1905bd15ec1a7b9fa6c9e8d5d0e3c1bb725b80aaa8f0dace`

```dockerfile
```

-	Layers:
	-	`sha256:62b2b65c7726f0bc44d1898c2413265f75e0e9d072475d4fb3de3ddce97f19b2`  
		Last Modified: Fri, 27 Sep 2024 07:59:14 GMT  
		Size: 7.6 MB (7584781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5061588e66eb3ef1d584475e7b23952b49d8b7c2dce73b19213b631f24970618`  
		Last Modified: Fri, 27 Sep 2024 07:59:14 GMT  
		Size: 47.2 KB (47204 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:62b793824eee006ecf118970d65420895eed4ff9f19e09d40c516e7f88737e3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.7 MB (211734229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ceabcff5bd4e52929742e82a41c14a368ea0f0148f0b74cf8658f98e7b37e6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:32 GMT
ADD file:c162e60b24ef6aed489ba1986f407fd9ab4ace659e0e3e6759ffac7eb0b7f770 in / 
# Wed, 04 Sep 2024 21:48:32 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:18:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 22:18:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 22:19:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:19:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 22:19:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 22:19:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:19:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:19:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 22:46:54 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 04 Sep 2024 22:46:54 GMT
ENV PHP_VERSION=8.3.11
# Wed, 04 Sep 2024 22:46:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Wed, 04 Sep 2024 22:46:55 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Wed, 04 Sep 2024 22:47:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 22:47:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 22:57:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 22:57:30 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 04 Sep 2024 22:57:32 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 22:57:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 22:57:32 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 22:57:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 04 Sep 2024 22:57:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Sep 2024 22:57:33 GMT
EXPOSE 9000
# Wed, 04 Sep 2024 22:57:33 GMT
CMD ["php-fpm"]
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	version='6.6.2'; 	sha1='7acbf69d5fdaf804e3db322bad23b08d2e2e42ec'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
VOLUME [/var/www/html]
# Thu, 12 Sep 2024 19:33:49 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Sep 2024 19:33:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:44990bd21e0c5db65674bd030d12ea2461a14f2bb4007469bc2667c8535a8357`  
		Last Modified: Wed, 04 Sep 2024 21:51:32 GMT  
		Size: 26.9 MB (26887411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cf852a9ba86e2887cb6ae81a22fd3cf861010abcf57ae1066ec0b59a523a8a`  
		Last Modified: Thu, 05 Sep 2024 00:04:02 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc51225fc9b9e1a6df96d433497faacd05a9849b6e148315b9b6ea2063d55e9b`  
		Last Modified: Thu, 05 Sep 2024 00:04:17 GMT  
		Size: 82.0 MB (81995015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ac14ff273c17e96586bdbeac20331d8b9eff59891a0eed04365468f870f6d2`  
		Last Modified: Thu, 05 Sep 2024 00:04:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfd6f8109f1cfe10e074af8af1d4a36851b91b417983d43dbd2804227b66d13`  
		Last Modified: Thu, 05 Sep 2024 00:06:48 GMT  
		Size: 12.8 MB (12793175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f09632963987973ee51ae39d4f2b3dcc87cce319c798c2531c7fed0c08426a4`  
		Last Modified: Thu, 05 Sep 2024 00:06:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf4bd1d5555b3f02fbd87f476eeb6db0139c015fb206f410531f1159174b815`  
		Last Modified: Thu, 05 Sep 2024 00:07:56 GMT  
		Size: 26.5 MB (26494414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd92c0e948d7cfcb289806f8cefb058ae0e0fc77052e9e3c307f6e339f82c56`  
		Last Modified: Thu, 05 Sep 2024 00:07:51 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cc24077b1ce788191f5be369d36babd77c6ef9d01f14ce1fc151ce8e37e248`  
		Last Modified: Thu, 05 Sep 2024 00:07:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad714e4c4f3da075d523265a6dcae940ba82f8644f0df3c0b217fc0bc065d5b`  
		Last Modified: Thu, 05 Sep 2024 00:07:51 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:109e87744644a46965e28415b577cb457bec01d1b03b80f811fadba7cd29a411`  
		Last Modified: Fri, 06 Sep 2024 03:35:09 GMT  
		Size: 25.8 MB (25823876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893f47d12f321fe38b88c58ba0e2d8c68193f8453bbfc36046b9a91ce7d3b82c`  
		Last Modified: Fri, 13 Sep 2024 01:46:05 GMT  
		Size: 13.3 MB (13257901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a388002e870f505f8a162ce0639f44cc68e9c4f5aaa81a7d3a78b4374ce83c`  
		Last Modified: Fri, 13 Sep 2024 01:46:04 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf05d3539d7e8a4310923fef4829efbec63882e831c1c44ead0805c4013ba0d`  
		Last Modified: Fri, 13 Sep 2024 01:46:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03661ab52e2f70e8ef9ac0624d5d490287badfa10a8ad54598fbc3233993ee9b`  
		Last Modified: Fri, 13 Sep 2024 01:46:05 GMT  
		Size: 24.5 MB (24464770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bd2761649c8b9a3039e486fad83bdbbb710c02d8ea1567baf81dbf3639032a`  
		Last Modified: Fri, 13 Sep 2024 01:46:05 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ccbcee6e1cbc961592f493f8adbb350e0a63f88f102316ca35975fc7fc4b3a`  
		Last Modified: Fri, 13 Sep 2024 01:46:05 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:8cece08f1fc6674f281e9f5a88b3cdc68329d26a48825bf74d0083191121b4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7438628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbe1badffb20238bb4448084b7ea5dddd2861793d5c29d163210ee7ba951246`

```dockerfile
```

-	Layers:
	-	`sha256:d78bd83b3c08bfc12471115c1e943bd52e6e910ccc0e2279a1220b3906992559`  
		Last Modified: Fri, 13 Sep 2024 01:46:04 GMT  
		Size: 7.4 MB (7391310 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65784cb22f9a600a4cb5043b4d60a9e87a7088ad9adf191aac054a01151c3219`  
		Last Modified: Fri, 13 Sep 2024 01:46:03 GMT  
		Size: 47.3 KB (47318 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:bcc412d4efb18ecb2fcce311aff2f174690f0271c543bafeadac480ea2367018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **200.9 MB (200939038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb1ae36a8649712cff7fd980bf64702a7cf5b9451465b03c9fa95c6dbe93742a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Sep 2024 21:58:08 GMT
ADD file:90772cdf7913d0ef1bf41e513a6205fa3195a1583476a536ec770e8381f77ac1 in / 
# Wed, 04 Sep 2024 21:58:08 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:46:50 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 22:46:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 22:47:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:47:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 22:47:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 22:47:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:47:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:47:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 23:15:37 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 04 Sep 2024 23:15:37 GMT
ENV PHP_VERSION=8.3.11
# Wed, 04 Sep 2024 23:15:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Wed, 04 Sep 2024 23:15:38 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Wed, 04 Sep 2024 23:15:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 23:15:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:24:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 23:24:33 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:24:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 23:24:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 23:24:35 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 23:24:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 04 Sep 2024 23:24:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Sep 2024 23:24:36 GMT
EXPOSE 9000
# Wed, 04 Sep 2024 23:24:36 GMT
CMD ["php-fpm"]
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	version='6.6.2'; 	sha1='7acbf69d5fdaf804e3db322bad23b08d2e2e42ec'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
VOLUME [/var/www/html]
# Thu, 12 Sep 2024 19:33:49 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Sep 2024 19:33:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:670631d7a00e03a2701d6b6aff29204afdeff4cd2da308462d92f5743156ede1`  
		Last Modified: Wed, 04 Sep 2024 22:01:44 GMT  
		Size: 24.7 MB (24718265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52af8d0fa86c9b158af0ab781cb65e065749146b3fe2c329cb4e9d0af8b14067`  
		Last Modified: Thu, 05 Sep 2024 00:26:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ecdfb85b1e01962d1365bfe3926bbbfe42185d9c8b60d0930000a9db914c4f`  
		Last Modified: Thu, 05 Sep 2024 00:26:57 GMT  
		Size: 76.2 MB (76163311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860c94c7af381cee44c718f3a335927de4a439a9ae12847fc214772a3860cd10`  
		Last Modified: Thu, 05 Sep 2024 00:26:44 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd26bfa8a4a68690a825130a6a0054fbfe14839601e18f9132033107177a7c90`  
		Last Modified: Thu, 05 Sep 2024 00:29:20 GMT  
		Size: 12.8 MB (12793141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a202414f64881516b30d66bc081952e3f79d7f3274d4a354a2485213d34bd40`  
		Last Modified: Thu, 05 Sep 2024 00:29:19 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0bee99d0593952d502be0aa28afa70644bb41ca516207cadd24a6cd242d4d4a`  
		Last Modified: Thu, 05 Sep 2024 00:30:31 GMT  
		Size: 25.6 MB (25598707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22c0de14ad2a9219ee461cc2b7cef284107826c27c2a28d05da14ca0965587d`  
		Last Modified: Thu, 05 Sep 2024 00:30:26 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deba02e36e20827b869ae9bc92e6bf0fd7ccc23ef57016aa180ed3f8b7951abc`  
		Last Modified: Thu, 05 Sep 2024 00:30:26 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6771cbc5a5d52ffd442c8bdb0c2c32cf8008c835f593a0141f106e2eb33951`  
		Last Modified: Thu, 05 Sep 2024 00:30:26 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffe2502b998bd69c93f44ed9720c10d6dd88caeeec63c31affaa400ee8bf8d9`  
		Last Modified: Fri, 06 Sep 2024 04:29:06 GMT  
		Size: 25.2 MB (25160654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9eeeda54608083a1e0f4805e530fc6d6a3c9e23c6b8925adf359851f82ff098`  
		Last Modified: Fri, 13 Sep 2024 04:17:07 GMT  
		Size: 12.0 MB (12022495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8e0edefacb39d0583ddf635027af114a8caeb69591a29b702301b5a9afeb25`  
		Last Modified: Fri, 13 Sep 2024 04:17:06 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860781efcc5517999493772e2960231df61ced47914be3fb332db702cd722347`  
		Last Modified: Fri, 13 Sep 2024 04:17:06 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3c2cf7ff33f259eb8c1d8fcf9e6739581a6abe9a7ec1a700e1c374d8a5b111`  
		Last Modified: Fri, 13 Sep 2024 04:17:08 GMT  
		Size: 24.5 MB (24464798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6dc800ecdc6bebf4d8ad0887d32b239b5e7cca6b729db19273843851cc4c5c4`  
		Last Modified: Fri, 13 Sep 2024 04:17:07 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab039f9d68b4c6b313696ea55bbe24d9a289d6ae1f4ce2ed20c7090b857bb13`  
		Last Modified: Fri, 13 Sep 2024 04:17:07 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:0efd9f647bd7bd11fd1f05f7a1727ea8f2620b52cfd0d7da5d54c2fc9d7e4241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7443293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31fd190fd2b39afd1a55db29acce1ba716e8e866255ff5d76428d49c7dde340`

```dockerfile
```

-	Layers:
	-	`sha256:012280d5d65c994ff53e970cdf83ce92e91c7760c98e0307880ff76b78a43636`  
		Last Modified: Fri, 13 Sep 2024 04:17:07 GMT  
		Size: 7.4 MB (7395976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c7e881b842bbe2656821168c0debeebfa35a25321d7b95bc0c30850e3f7b3624`  
		Last Modified: Fri, 13 Sep 2024 04:17:06 GMT  
		Size: 47.3 KB (47317 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:c682636b9bd9bd5838bdfae3bbc393ac779f3437b9f976dd8cdc266ca2d5988a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.6 MB (232579942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b6564af4a3ba1630afe4bbdc99c421e6495efeb27b83672b9cc1dc883d02e5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:52 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 04 Sep 2024 21:39:53 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:30:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 22:30:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 22:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:30:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 22:30:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 22:30:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:30:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:30:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 22:55:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 04 Sep 2024 22:55:24 GMT
ENV PHP_VERSION=8.3.11
# Wed, 04 Sep 2024 22:55:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Wed, 04 Sep 2024 22:55:24 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Wed, 04 Sep 2024 22:55:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 22:55:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:06:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 23:06:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 04 Sep 2024 23:06:43 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 23:06:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 23:06:43 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 23:06:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 04 Sep 2024 23:06:44 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Sep 2024 23:06:44 GMT
EXPOSE 9000
# Wed, 04 Sep 2024 23:06:44 GMT
CMD ["php-fpm"]
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	version='6.6.2'; 	sha1='7acbf69d5fdaf804e3db322bad23b08d2e2e42ec'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
VOLUME [/var/www/html]
# Thu, 12 Sep 2024 19:33:49 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Sep 2024 19:33:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9125f50077837c519800d65edc67294c009e30fcc820455fbefc671b63081421`  
		Last Modified: Thu, 05 Sep 2024 00:18:28 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c15c4686903cb5bbd6cabc5447788b26574756d94e02c0952258c66bb2b4379`  
		Last Modified: Thu, 05 Sep 2024 00:18:40 GMT  
		Size: 98.1 MB (98131394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8893eb8a52e8af8365ae670e2549bcff74923def7137abb8dbd4657905297f01`  
		Last Modified: Thu, 05 Sep 2024 00:18:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1d1917b7af2f83e78728c20781a193cb6b3ad89ea56dedf9102e92890c99ab`  
		Last Modified: Thu, 05 Sep 2024 00:21:10 GMT  
		Size: 12.8 MB (12794866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61b696322d8944902cbeb34dea221a6a3d45e578ab60ddbd7a117f4cbe05f04c`  
		Last Modified: Thu, 05 Sep 2024 00:21:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc23d9120e90b7f53cb089126556a8c32206d4ddb98472ffbc10d43c17884a2`  
		Last Modified: Thu, 05 Sep 2024 00:22:15 GMT  
		Size: 28.0 MB (27959114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb60d5564aaf6f6b45bc927ba83303322ccf1fc4dd9c2548dd794bc199b3a124`  
		Last Modified: Thu, 05 Sep 2024 00:22:12 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88fb1ff3c4488f9ef10516a5ad9b65c30713370fdf38732a071e4eb81ac6161`  
		Last Modified: Thu, 05 Sep 2024 00:22:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f1e4b464d0134a9f2ca0e34ba84985305aa231cca784c011d9fc490154eb48`  
		Last Modified: Thu, 05 Sep 2024 00:22:12 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534e2181cf59c2e88afbd6f59770d81457cac7752bc95953560070eff71391cb`  
		Last Modified: Thu, 05 Sep 2024 20:51:40 GMT  
		Size: 26.3 MB (26289814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b57bb90101734648ea76f8584a4060ba838bb8d7810b9c322c844b8878bb2cc`  
		Last Modified: Fri, 13 Sep 2024 02:34:01 GMT  
		Size: 13.8 MB (13765736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1997b9d058d998b639ebd68ae9b91868d7841d1d170801568b75ed29bdeb9142`  
		Last Modified: Fri, 13 Sep 2024 02:34:00 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38e4e29f06875c870cb06560163da191355485764ab70398dc5ab23d2d016d5`  
		Last Modified: Fri, 13 Sep 2024 02:34:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2ba88c80d212e52ce2db2f55306f8847937426ec1c11f5717de24e8f5bae10`  
		Last Modified: Fri, 13 Sep 2024 02:34:01 GMT  
		Size: 24.5 MB (24464796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d73584234c32d885ce0f51748195ca9754cb9ec171cf0f86fab558333a7d5fa`  
		Last Modified: Fri, 13 Sep 2024 02:34:01 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b2da0523959db8ecbe3521907b4dc0bac06718f7474244f96a92bbacc39060`  
		Last Modified: Fri, 13 Sep 2024 02:34:01 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:5c6ba57006269836b7495da92c903b7dc48c5e06b111c34304b046cf57042675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7661013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0cdc86f14308c659ed82501d8647c6a39d699c6285ca5cc1514e3be0a1ddd4`

```dockerfile
```

-	Layers:
	-	`sha256:d88257759e7c58dd8a7d618c19ffb89b4375253ea02eb85ac30d8a8e4cce2368`  
		Last Modified: Fri, 13 Sep 2024 02:34:01 GMT  
		Size: 7.6 MB (7613517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54ade7dc91ae21592d46e65af95127d281bdfa7234af6d81d24dafb2e1151568`  
		Last Modified: Fri, 13 Sep 2024 02:34:00 GMT  
		Size: 47.5 KB (47496 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:11cffc5e789578851b8ac8800af785dae135154aedf197f98ac5316978c4c449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237762857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50bf745a9954b8da22d58bde37a8cb784af192fbecb6ac51a2d332c9dfa226f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Sep 2024 22:44:34 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 04 Sep 2024 22:44:34 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:46:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 23:46:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 23:46:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:46:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 23:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 23:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 23:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 23:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Sep 2024 00:38:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 12 Sep 2024 19:33:49 GMT
ENV PHP_VERSION=8.3.12
# Thu, 12 Sep 2024 19:33:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 12 Sep 2024 19:33:49 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 12 Sep 2024 19:33:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 12 Sep 2024 19:33:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 12 Sep 2024 19:33:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 12 Sep 2024 19:33:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Sep 2024 19:33:49 GMT
WORKDIR /var/www/html
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 12 Sep 2024 19:33:49 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Sep 2024 19:33:49 GMT
EXPOSE 9000
# Thu, 12 Sep 2024 19:33:49 GMT
CMD ["php-fpm"]
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	version='6.6.2'; 	sha1='7acbf69d5fdaf804e3db322bad23b08d2e2e42ec'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
VOLUME [/var/www/html]
# Thu, 12 Sep 2024 19:33:49 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Sep 2024 19:33:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d31e4426139e19c94ca0942df7023cf26932c267261b263dbd848554444817`  
		Last Modified: Thu, 05 Sep 2024 03:02:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c70cae078252759f892081775f43cfce9b4bca811fa4ee5046fc050063c4cf`  
		Last Modified: Thu, 05 Sep 2024 03:02:34 GMT  
		Size: 101.5 MB (101514423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5066486db10391a0fdfecfd181c1c0ac73eefce83f0210b43e3ba3f66cc2c0`  
		Last Modified: Thu, 05 Sep 2024 03:02:11 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20e07f67d1b1f0dddfcaa2df9c4918d393dc01845fcd759f7a941881a3b74e7`  
		Last Modified: Fri, 27 Sep 2024 03:23:09 GMT  
		Size: 12.8 MB (12806931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654f262870e890ea9aedf0890f1d1acde58e3f8ec8ad2aab7ca02a8fd154df6e`  
		Last Modified: Fri, 27 Sep 2024 03:23:08 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621d7f7dbff892cb19c9a04d8f1d9404c3fca1d7112edcf880def5637ef0076c`  
		Last Modified: Fri, 27 Sep 2024 03:24:26 GMT  
		Size: 28.5 MB (28525107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28ff44163af1b5b1625c31a712497498d87c4ceab005a7a39cd5529ea8b363e`  
		Last Modified: Fri, 27 Sep 2024 03:24:20 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0664c0cabc6b54f128bb3fd386fb0dad63820a796cfaa9f6507a3b442a16ee4`  
		Last Modified: Fri, 27 Sep 2024 03:24:20 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196f4b7c97c9598415d43776c18fc454bc7e4c89ac60b81b1104f277817668ec`  
		Last Modified: Fri, 27 Sep 2024 03:24:21 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e33c187ca61b615a8c5b0b81681518264505ee56b131166c89303102ecf04d5`  
		Last Modified: Fri, 27 Sep 2024 05:01:25 GMT  
		Size: 26.8 MB (26822652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745187b71d410c265b15cff6667e6a3e94906a8c3014f487a71d190e372fda83`  
		Last Modified: Fri, 27 Sep 2024 05:01:25 GMT  
		Size: 13.5 MB (13466997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922508fa7bd231dbb23df49c8cad16a157c77ac37c7e00643135b08084fc1bc5`  
		Last Modified: Fri, 27 Sep 2024 05:01:24 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa242ed03043239cb8e0c04b968c3b40fcd07319aab878f9df6b48c3b1ae635`  
		Last Modified: Fri, 27 Sep 2024 05:01:25 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b4943d8134ee322bba07dc35b2ab6e9720e07cd8f48948ed398c72504ce901c`  
		Last Modified: Fri, 27 Sep 2024 05:01:26 GMT  
		Size: 24.5 MB (24464777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dda22f5a28b5f730669857bd5f47fff3c0fe5e0edf092f958853af86608d6ac`  
		Last Modified: Fri, 27 Sep 2024 05:01:26 GMT  
		Size: 2.4 KB (2354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e0dc3936395861f5280d60e1b8f9e655902f1667ac03241574e65a5a4abd72`  
		Last Modified: Fri, 27 Sep 2024 05:01:26 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:3dc12c84c7f200ee919e71e1f081d73499543080f38ce37a0b08ed6fee7bc602
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7605531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62946076c7501ea070c3cdf1cc284fb14c03e8701607948fa5eec8da892e6482`

```dockerfile
```

-	Layers:
	-	`sha256:65c067d444e5b3242029faef3f04dd398324632e5d4622f3d25b8415f021554a`  
		Last Modified: Fri, 27 Sep 2024 05:01:23 GMT  
		Size: 7.6 MB (7558364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ece9285f58d4f5473e3900f45501b66ab82e2a297a1f8bd8497028db8bf24f00`  
		Last Modified: Fri, 27 Sep 2024 05:01:23 GMT  
		Size: 47.2 KB (47167 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-fpm` - linux; mips64le

```console
$ docker pull wordpress@sha256:31d6659a43278df065156f838d670bb7afd5a7803543b59803c35e0fb3c2c7e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212851476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4755cb38b4466fb3db8cca7e4dfdbe51173ece1fc1cb3467afefb660157ac42`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Sep 2024 22:15:45 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 04 Sep 2024 22:15:50 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 23:23:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 23:23:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 23:25:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 23:25:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 23:25:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 23:25:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 23:25:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 23:25:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 05 Sep 2024 00:36:19 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 05 Sep 2024 00:36:22 GMT
ENV PHP_VERSION=8.3.11
# Thu, 05 Sep 2024 00:36:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Thu, 05 Sep 2024 00:36:29 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Thu, 05 Sep 2024 00:37:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 05 Sep 2024 00:37:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Sep 2024 01:24:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Sep 2024 01:24:38 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 05 Sep 2024 01:24:44 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Sep 2024 01:24:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Sep 2024 01:24:51 GMT
WORKDIR /var/www/html
# Thu, 05 Sep 2024 01:24:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 05 Sep 2024 01:25:01 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Sep 2024 01:25:04 GMT
EXPOSE 9000
# Thu, 05 Sep 2024 01:25:08 GMT
CMD ["php-fpm"]
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	version='6.6.2'; 	sha1='7acbf69d5fdaf804e3db322bad23b08d2e2e42ec'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
VOLUME [/var/www/html]
# Thu, 12 Sep 2024 19:33:49 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Sep 2024 19:33:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd61d7a0bd26fdefd1fc3f6685c32109220be495dcc46fe17919766e554de48`  
		Last Modified: Thu, 05 Sep 2024 03:51:29 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1187d9c88570478f80b55a3e07d23bb40e2db5e9069089775ddb5d5a54f4af4`  
		Last Modified: Thu, 05 Sep 2024 03:52:27 GMT  
		Size: 80.7 MB (80667470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b165b263f070f18c828e0e5ed25251a1e38f37f96ea4eb4a5727bbc912240e5`  
		Last Modified: Thu, 05 Sep 2024 03:51:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baa97a479b21f3012318c12a2e8dc15fa84297c2822cd00910bae3dc68c0f28`  
		Last Modified: Thu, 05 Sep 2024 03:55:07 GMT  
		Size: 12.6 MB (12588032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb19405f2b499bcb6eb06b0536609372d9c1a0cc8d552294b21d471a3a8f0764`  
		Last Modified: Thu, 05 Sep 2024 03:55:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20397ae5dae64075a2450543810ddaecac5dee0149bc567144302b661b04cb7`  
		Last Modified: Thu, 05 Sep 2024 03:57:17 GMT  
		Size: 26.9 MB (26901689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c714a5eba68c3cf1ed55293fe3b3121d22d27d559101cd7bd0bfaa8136810050`  
		Last Modified: Thu, 05 Sep 2024 03:57:01 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8cb8ca842a294b4f959127c719a281904c1239ee879410adcc21a6a830931c9`  
		Last Modified: Thu, 05 Sep 2024 03:57:01 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cbd558978208a15268e45f88f7430585e6224575657d52e1ced2dfe471eb97`  
		Last Modified: Thu, 05 Sep 2024 03:57:01 GMT  
		Size: 9.2 KB (9189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eee9a3ace9b833c2452958dd347aef760bd77bf82b2cf58d9a4010734e02182`  
		Last Modified: Fri, 06 Sep 2024 07:37:29 GMT  
		Size: 26.1 MB (26149499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3599ddbe9a2846fcf28ff38b220da00aa66a3a5c88c60d1377d35b18d6adfa0`  
		Last Modified: Thu, 12 Sep 2024 22:56:00 GMT  
		Size: 12.9 MB (12937262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde1665d689d2f4daf1a842a32c2a9e3a889bca5b74c1e9b47c98ab8b79637bb`  
		Last Modified: Thu, 12 Sep 2024 22:55:58 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b076c51bf32d6455b19eb3ea6e428fcd3feed9baa16f32b743cfce077c6b0170`  
		Last Modified: Thu, 12 Sep 2024 22:55:58 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88af589d522b2dab95e9d715eb81bb5dd8d9230c04cdcb19880f90c2520f4ce9`  
		Last Modified: Thu, 12 Sep 2024 22:56:01 GMT  
		Size: 24.5 MB (24464796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4601b5b3cdd99f93e9a3e4d80e3fefbee942d83ba61dc42d5238817ebe2c23fc`  
		Last Modified: Thu, 12 Sep 2024 22:55:59 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b486b00b685d7d6604d28284697f00bb292039b09726fce9282d725f5eb5d25a`  
		Last Modified: Thu, 12 Sep 2024 22:55:59 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:3691bbb58eb97b14182ea319114c7a06316cd4664b0982e584557d98dcd0891e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 KB (47046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d1b89d610ca3b6e33672c74ab0ea9badc6b0b70a8706da97cfaec7790246330`

```dockerfile
```

-	Layers:
	-	`sha256:b3049e129c1ea2b864fdca0ced4ecb6c58603ef985467781bf42652570ed434e`  
		Last Modified: Thu, 12 Sep 2024 22:55:58 GMT  
		Size: 47.0 KB (47046 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:bb8a42276339126f3b638b85cf1a1bd4e0615780f3919de2f031688606f0f74d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245887821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03dd647f7c8f504fe34569ce356ab466b780be332ddb04c19dbf3a8ca1377330`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:52 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 04 Sep 2024 22:25:54 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 22:47:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 06 Sep 2024 22:47:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 06 Sep 2024 22:47:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 06 Sep 2024 22:48:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:48:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:48:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:48:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:48:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:33:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 06 Sep 2024 23:33:52 GMT
ENV PHP_VERSION=8.3.11
# Fri, 06 Sep 2024 23:33:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Fri, 06 Sep 2024 23:33:53 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Fri, 06 Sep 2024 23:34:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 06 Sep 2024 23:34:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:43:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Sep 2024 23:43:41 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 06 Sep 2024 23:43:42 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Sep 2024 23:43:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Sep 2024 23:43:43 GMT
WORKDIR /var/www/html
# Fri, 06 Sep 2024 23:43:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 06 Sep 2024 23:43:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Sep 2024 23:43:45 GMT
EXPOSE 9000
# Fri, 06 Sep 2024 23:43:45 GMT
CMD ["php-fpm"]
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	version='6.6.2'; 	sha1='7acbf69d5fdaf804e3db322bad23b08d2e2e42ec'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
VOLUME [/var/www/html]
# Thu, 12 Sep 2024 19:33:49 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Sep 2024 19:33:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ea9222f7ab10e7e2a9b68be641a3f942d5a7828fdd853395622a6bb1c0ce0f`  
		Last Modified: Sat, 07 Sep 2024 01:42:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14aed28a8d8a0a890612409f5cac111426f3ccecc75786a57fb266d50a47a42`  
		Last Modified: Sat, 07 Sep 2024 01:42:23 GMT  
		Size: 103.3 MB (103326259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6076862523211f1e3bf09abbf03b4bc3beb2b313a114be849f608398557061d4`  
		Last Modified: Sat, 07 Sep 2024 01:42:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199ae3973bd9af05a1b2881b6c614a3e7f051b3ca6c5e4935df7d4d9b3d4669b`  
		Last Modified: Sat, 07 Sep 2024 01:46:36 GMT  
		Size: 12.8 MB (12794454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76e50ebaf15ea2d690e85113f33c4bf083ec388be888948831c3ebe4de14b390`  
		Last Modified: Sat, 07 Sep 2024 01:46:35 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e331a62321d01b432337d5ea9feb5a0d6cad1cf28caf92b08b376c228935a5`  
		Last Modified: Sat, 07 Sep 2024 01:47:45 GMT  
		Size: 29.1 MB (29075304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a118257269a140220d9901e2c72a660845b1bd35eca1f7ae2dd39ad50f82eaf4`  
		Last Modified: Sat, 07 Sep 2024 01:47:40 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44759cc902457707ff178bc2bfe8a8a754f457c91e5ca08103ef698f2c9592bd`  
		Last Modified: Sat, 07 Sep 2024 01:47:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c925598d3b635ee5abdc139a83e20144587ba38edf09a5ee0fb5b5b051a05964`  
		Last Modified: Sat, 07 Sep 2024 01:47:40 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93409985873e688b901a0f48ba6058378e9b948d7589b247a2c080109e046a9`  
		Last Modified: Sat, 07 Sep 2024 13:10:30 GMT  
		Size: 27.5 MB (27478147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855e1c86aefe76b2f068172d55f01740344d764442f0aed8902ecc91fe406438`  
		Last Modified: Fri, 13 Sep 2024 06:41:15 GMT  
		Size: 15.6 MB (15608854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47839cda4b256e4f14a013c0e65d0ebd1fe012a5fe52facae128185f276d12b1`  
		Last Modified: Fri, 13 Sep 2024 06:41:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdfa0f9ca27cd0c4a5fa99db8f261cc0faa2432ece34add7e91dfbf71e2d553`  
		Last Modified: Fri, 13 Sep 2024 06:41:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:642b05436120d07ce4ab287d6dd7b44388bf839c4332ff19f1a930902eb831b3`  
		Last Modified: Fri, 13 Sep 2024 06:41:15 GMT  
		Size: 24.5 MB (24464776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3371a9a051cf79b03595dd6c8e59734bceaa525ea56ea72a4acae8da8796f3c9`  
		Last Modified: Fri, 13 Sep 2024 06:41:15 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c403e043d06f0f52ba09911bd95bdc6450c16a5ae2b9172bade9a2eea7b9ed24`  
		Last Modified: Fri, 13 Sep 2024 06:41:15 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:8b2efd2e348bc9f83dc1508e01eb76af1a1c209398d7031c3ca3d560caa60dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e21d1de5c854e885564c1a445078e3a2ac8f8a7792f7b2ace29af12609172b3`

```dockerfile
```

-	Layers:
	-	`sha256:1f0498515eb75dfd0766d49b667c3e4d8abc147a9d5412801db5d6f7f49e7849`  
		Last Modified: Fri, 13 Sep 2024 06:41:14 GMT  
		Size: 7.6 MB (7563671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18c88d563557f3b4813e3621e0b9d728ea1a6b5a0ce31827544b6d3a392b7be3`  
		Last Modified: Fri, 13 Sep 2024 06:41:14 GMT  
		Size: 47.2 KB (47250 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.3-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:81af6b718be591544d91ba6684b80690ce1f531faaddef5094d5667e266afe20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212158026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62145fad1d8c3f0c8477defeb0cb5d1ad25f01a99bfa7fbeb910dbfc9c85d41e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 04 Sep 2024 21:42:50 GMT
ADD file:728128617ba2b026c358eb266cd495be84354c4e5dc4ecc2953cb829190a4546 in / 
# Wed, 04 Sep 2024 21:42:52 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:12:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 04 Sep 2024 22:12:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 04 Sep 2024 22:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 04 Sep 2024 22:12:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 04 Sep 2024 22:12:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 04 Sep 2024 22:12:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:12:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 04 Sep 2024 22:12:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 04 Sep 2024 22:37:06 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 04 Sep 2024 22:37:06 GMT
ENV PHP_VERSION=8.3.11
# Wed, 04 Sep 2024 22:37:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.11.tar.xz.asc
# Wed, 04 Sep 2024 22:37:07 GMT
ENV PHP_SHA256=b862b098a08ab9bf4b36ed12c7d0d9f65353656b36fb0e3c5344093aceb35802
# Wed, 04 Sep 2024 22:37:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 04 Sep 2024 22:37:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 04 Sep 2024 22:45:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 04 Sep 2024 22:45:26 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 04 Sep 2024 22:45:26 GMT
RUN docker-php-ext-enable sodium
# Wed, 04 Sep 2024 22:45:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 04 Sep 2024 22:45:26 GMT
WORKDIR /var/www/html
# Wed, 04 Sep 2024 22:45:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 04 Sep 2024 22:45:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Sep 2024 22:45:27 GMT
EXPOSE 9000
# Wed, 04 Sep 2024 22:45:27 GMT
CMD ["php-fpm"]
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
RUN set -eux; 	version='6.6.2'; 	sha1='7acbf69d5fdaf804e3db322bad23b08d2e2e42ec'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
VOLUME [/var/www/html]
# Thu, 12 Sep 2024 19:33:49 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 12 Sep 2024 19:33:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 12 Sep 2024 19:33:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:95fe27c895a828dc681ee4a0cbea0264c47528dad525efdb9641a375666536bd`  
		Last Modified: Wed, 04 Sep 2024 21:47:41 GMT  
		Size: 27.5 MB (27490321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9c3e85da8b09b5b347e0de23df0ba14b87db8c71b84ff72bafeff05ac4c45d`  
		Last Modified: Wed, 04 Sep 2024 23:43:14 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d162a779ea2f70207f50c43a8ea8a2afc36c812e56c03883aef22591b1fadd`  
		Last Modified: Wed, 04 Sep 2024 23:43:27 GMT  
		Size: 80.8 MB (80817858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d512ffc352f972eede4ede7944fbab31c430f84671da665932f51478717b92e0`  
		Last Modified: Wed, 04 Sep 2024 23:43:14 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae17c14c1c07a7b8eb13ea43fcdbb1b0e733581c2e85c0813c19bbc790a4d57`  
		Last Modified: Wed, 04 Sep 2024 23:45:09 GMT  
		Size: 12.8 MB (12793488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eeb671d1add74b790bf0e080fe77c5ecc70c27721c557fcefb934420c105ef`  
		Last Modified: Wed, 04 Sep 2024 23:45:08 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5fd5b9ad9c4031b98f3d8ab1a3620350bd7d7e0acab8c3aed4291976620be5`  
		Last Modified: Wed, 04 Sep 2024 23:45:52 GMT  
		Size: 27.1 MB (27118612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:910003a671fd9f46a998f5d2ffc300ba8f6efb96301d547281e8816e5ec1b43b`  
		Last Modified: Wed, 04 Sep 2024 23:45:48 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0301835d1d894fec57c6fdd320390cb044e64d62e857a40bec3dcbeb9d05a784`  
		Last Modified: Wed, 04 Sep 2024 23:45:48 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5551e50ecab0e0570817ebb16dcad8744f6752698952bedd135433239bd743ae`  
		Last Modified: Wed, 04 Sep 2024 23:45:49 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c924457e60f1c2d40d7c4a0f2bfb8c5817996629603d41479b7e461315fa621`  
		Last Modified: Fri, 06 Sep 2024 02:42:26 GMT  
		Size: 26.0 MB (26012051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b05e1e5f7a5c398199103dc716874a55b4a323687af98e5855d658a71dc8ff3f`  
		Last Modified: Fri, 13 Sep 2024 03:08:47 GMT  
		Size: 13.4 MB (13443228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dda80468ffc39e77308e24daea3bf54bc7501d23415aabd5677f0196645831`  
		Last Modified: Fri, 13 Sep 2024 03:08:46 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7990611b355b13230394b7a8d6a1aba2161584be4ca97bc62c057e757eaa718e`  
		Last Modified: Fri, 13 Sep 2024 03:08:46 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f72371ca17d648d7a31470e56c82cbb865dad055febfa2f253a1c7d35adffe6`  
		Last Modified: Fri, 13 Sep 2024 03:08:47 GMT  
		Size: 24.5 MB (24464798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00dad912b3b07a2c380cd5da0ab336dff4e46990cb7a00fb869030f0feadf1e`  
		Last Modified: Fri, 13 Sep 2024 03:08:47 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a31512bd0b11ba2ac75179c585ead63c83dbef003acd8392a27aea1245260db`  
		Last Modified: Fri, 13 Sep 2024 03:08:47 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.3-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:5e087420c478a4bf9405ed075e966e869738889f0cabc17a590240d26681b8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7462661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc8ec70bcd320f439ee191b3fedac344a2acdfbfed341202120fc2544dd52d8`

```dockerfile
```

-	Layers:
	-	`sha256:5841cde44da7bc9846846e2a7e5cf6360d1338bb6f4dbd34cf8a80e9fe5debbf`  
		Last Modified: Fri, 13 Sep 2024 03:08:46 GMT  
		Size: 7.4 MB (7415465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:344079184bad1e62c9790cda8d3cda42604d2a91eced9f273265aa6252e2ce0c`  
		Last Modified: Fri, 13 Sep 2024 03:08:46 GMT  
		Size: 47.2 KB (47196 bytes)  
		MIME: application/vnd.in-toto+json
