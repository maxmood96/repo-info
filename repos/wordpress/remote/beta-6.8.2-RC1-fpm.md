## `wordpress:beta-6.8.2-RC1-fpm`

```console
$ docker pull wordpress@sha256:78630d7e0271c3aa5446f414180d7e6586ee23f827223332f88505a73b9bc602
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

### `wordpress:beta-6.8.2-RC1-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:7b54e595399c9dadb4ede42eb1f038ad09ba4256d8c4b77c18b51a142b9e72b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243714540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632db28b3f3e69688ab6c67ad0f8ad441294911d458dcfaf8e342db45fa5b518`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497ffba6e0f4b234746be4786b1337e7ce459b422d9dfcda2081622d65e74584`  
		Last Modified: Thu, 03 Jul 2025 23:05:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073cdee253a41348251bcfadec9f8e393b726e99f87fe81ab5b0ece83868df59`  
		Last Modified: Thu, 03 Jul 2025 23:05:06 GMT  
		Size: 104.3 MB (104331385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7a2d9b7912ff8c0587fd7128e058a4253b1ed1389e46793bedea37fee33af4`  
		Last Modified: Thu, 03 Jul 2025 23:05:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26ebe53368dcdb1ed1b27ac242ecc5b374ab3f60f192ca3654f8c9178147ec5`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 12.3 MB (12272288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b78a104d740a410b6c172d74b0394a78b9059738cfbb3191c511a3327121a1`  
		Last Modified: Thu, 03 Jul 2025 23:05:00 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ca9d95af5090fbb8f46c6f1c1af5025678ffdfbe4be8a87cf3e69d6cea0796`  
		Last Modified: Thu, 03 Jul 2025 23:05:02 GMT  
		Size: 27.6 MB (27588438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb3c2a4d9322fe2ddabae1cc4348b2e765077431cb5edb16c682a86a5c9d420`  
		Last Modified: Thu, 03 Jul 2025 23:05:00 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c659f0c7018344d159acb166ff8689e90699f4d2ba302c360c993b819cfa4b12`  
		Last Modified: Thu, 03 Jul 2025 23:05:00 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76aca633092544d6d87ced15ad18a31e8e5cee615f05f99238c5536fc11667c7`  
		Last Modified: Thu, 03 Jul 2025 23:05:00 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c60b9a08e9bec6380e0e08a568c70670438ca00ced9485430940afa999aed1`  
		Last Modified: Thu, 03 Jul 2025 23:05:00 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b591a14151c33941bfb56c5fcfc87172e99837bb9054a9b1fae291a055156f0`  
		Last Modified: Wed, 09 Jul 2025 15:06:16 GMT  
		Size: 26.4 MB (26374685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036e925d6e32deaaaebb0190cdcec63b29fccc8addf147be0c599a143039b847`  
		Last Modified: Wed, 09 Jul 2025 15:06:24 GMT  
		Size: 18.0 MB (18000917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:647dc7e732a9e2f468718836f251ddc6b0cde009394c6f90a4d42661807f7f9f`  
		Last Modified: Wed, 09 Jul 2025 15:06:16 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750ff271baba98658b95dbbbede852b3b3d37d011511fbdbf7268b13ff696c0d`  
		Last Modified: Wed, 09 Jul 2025 15:06:12 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7ce76c5275669854f2c4a5ef714b00f986e0e68ed465504e6d29e35a6256133`  
		Last Modified: Wed, 09 Jul 2025 15:06:26 GMT  
		Size: 26.9 MB (26898467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5454e7c0c4b841890b169fe023ae8ccc34bea5c2cc8c662fb6604a0d31c97b`  
		Last Modified: Wed, 09 Jul 2025 15:06:12 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb037b86b430c93591518f0b5f38af3cab665852b2b77f9ecdcdcbcd3beaff9`  
		Last Modified: Wed, 09 Jul 2025 15:06:13 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d20c54ec15ee9ea56fdd5b8de38421c5f3d095fc2061721f8052afd71962bd`  
		Last Modified: Wed, 09 Jul 2025 15:06:12 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8.2-RC1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:09598d5811ceee5baedaa4873dc3c7a0fd316f99e52665e45253cb529f46b794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7889381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9fb6c33cd4026cef4cdf75d15d33e2df6a2f5a8cd88a71feaeb13a3894ff18`

```dockerfile
```

-	Layers:
	-	`sha256:fe9c7e3cb1b44f18fbc7caf1837ea188fd517844afe802c58110c3b61ed12fd5`  
		Last Modified: Tue, 08 Jul 2025 22:14:54 GMT  
		Size: 7.8 MB (7835421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca180c61318725210e454189396ab787759771b78feabe9b9032cddfd583e1a`  
		Last Modified: Tue, 08 Jul 2025 22:14:55 GMT  
		Size: 54.0 KB (53960 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8.2-RC1-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:9713cba3ce4f480a5ed538fe6a72eccd420657a6f06861dd54710ce075561e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212542904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5c08b98512139d87967415521a0cebbeb619065906f75d523d638761304fae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1751241600'
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:57a7872a7ce75b95d171f720f215d4e72b887ae709c5c0b319f93f704bd71e07`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 25.8 MB (25762460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b05322491f7f224fdb6afd1a4feb0c269fe0910bd44e82e37a846aec3e465c`  
		Last Modified: Tue, 01 Jul 2025 03:03:10 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b493a89b33667d984de07320c027ba0599d73427f434c8ec42c944a6bd4aa`  
		Last Modified: Tue, 01 Jul 2025 03:03:27 GMT  
		Size: 82.0 MB (81973614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eef43b7ed80f2af53848f0179316741b5f6d73203876a5f0f62b038d570f6c8`  
		Last Modified: Tue, 01 Jul 2025 03:03:10 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197dad158ba7b5dd057639af8c598a5aa40e03e971703b98dc2bbbc98b724597`  
		Last Modified: Thu, 03 Jul 2025 23:46:37 GMT  
		Size: 12.3 MB (12270326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59bf4febecc0d73178c2e3ec90b08f48aa768f1165f69a62ae86f4766efdea7`  
		Last Modified: Thu, 03 Jul 2025 23:46:35 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc24eb0ec34d61dfd64859ac51187d6011dbebcd483a1fc4786fb105f6fedfd4`  
		Last Modified: Fri, 04 Jul 2025 02:41:37 GMT  
		Size: 26.1 MB (26088201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a02e755a2df3aa9e919018cde04a076e9af32b77fcb65164db802beb1318f65`  
		Last Modified: Thu, 03 Jul 2025 23:57:51 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfd05eae06347c6fdf610295cdf4cd494486e2314ccf9520fb688d42bcc24aa`  
		Last Modified: Thu, 03 Jul 2025 23:57:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91cda8649d86bec56b028ea177c48c6a4f8a948007ceba8da99441f3d3d76e46`  
		Last Modified: Thu, 03 Jul 2025 23:57:50 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd2aab5f53dc5382fba0f6456c2fff0c063d11b09894ab96088311e140235763`  
		Last Modified: Thu, 03 Jul 2025 23:57:52 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42feed77b055947e964b39393c89ece1055153b1d21bcd100a6859b55cfa679d`  
		Last Modified: Fri, 04 Jul 2025 00:38:16 GMT  
		Size: 25.8 MB (25825003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88affaf02d3eba774f748f5419631760c3273b063e09171387852db00194cca9`  
		Last Modified: Fri, 04 Jul 2025 00:38:03 GMT  
		Size: 13.7 MB (13706611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9450e609272bc2bfa5da3685986c976931a06ccdefe8696d4a5b3cee55dcc87`  
		Last Modified: Fri, 04 Jul 2025 00:38:01 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271e8625a173950cae6a9f84426cfe5da8ac0cbdc46377e329a012515b82c734`  
		Last Modified: Fri, 04 Jul 2025 00:38:02 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bce6595a3e38df3225c3ef4d62a3e4f4c82c45dd0ceee55116a4000677c45a3`  
		Last Modified: Wed, 09 Jul 2025 21:23:39 GMT  
		Size: 26.9 MB (26898479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd8a13b590f85a8c3bb410fb131c591970f1872a7d79afbe62730b5118ac42`  
		Last Modified: Wed, 09 Jul 2025 21:23:37 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82836eac9f9d56f884d4154aa24c8e02aed220912490d18898c2d407cdae9d51`  
		Last Modified: Wed, 09 Jul 2025 21:23:38 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7e03dfd27f95e80c9ba87cdcfc41cbe7282f1ba3e7dd72d06c6073d64d6384`  
		Last Modified: Wed, 09 Jul 2025 21:23:39 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8.2-RC1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:7e25450a19791e32aac2b73a4ce561f16eff42ce92ef7c12fc4712eba190cc52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7692572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9a3c489b7e81c09a11ff8cd6611d92d0a2ce8ba0d8a6356eda5df66d082cfb`

```dockerfile
```

-	Layers:
	-	`sha256:c789d13238deaec3a400b5faa70ffdb585995eaceae7b8793d9bbcad8a897cc7`  
		Last Modified: Tue, 08 Jul 2025 22:15:02 GMT  
		Size: 7.6 MB (7638432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc68c8cec3e543952ad321f0dbe13d04bf8c6cadc430b25f1ed93e59ce0b7bdb`  
		Last Modified: Tue, 08 Jul 2025 22:15:03 GMT  
		Size: 54.1 KB (54140 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8.2-RC1-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:ae251aa9a9f9572c8be71af879c401cc43396c613d99d95b7f963a89f25380a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.1 MB (202102843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f03b881f30fa8088ce34a889dce3701b8b4a828f8ed87aed4ea64d2f8244310`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1751241600'
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:aa4115c1f73522274017cc9ef4668eb7be9359f354969cd6ffca48411714e948`  
		Last Modified: Tue, 01 Jul 2025 01:14:42 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef237a39acf4f8b50140ea0e65e44fb78759dd5c3014dea07a2e868cbaea5448`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d1f66f2aaac83b6eaf2006cda16a0feae7d183fb4de3fc7f021a3b94f4d2f5`  
		Last Modified: Tue, 01 Jul 2025 02:37:09 GMT  
		Size: 76.1 MB (76149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834cb9f18ec360ae1dafdba9049fa98c9a4c9dff8f407122be76f6644c8deb27`  
		Last Modified: Tue, 01 Jul 2025 02:37:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2404c7541d29c17ef2fef1c2b09c1d9c668be29347df29cb16c911eee7413966`  
		Last Modified: Fri, 04 Jul 2025 01:18:51 GMT  
		Size: 12.3 MB (12270273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7315450baf6945baae86236f9ff66821785627ba7e07e3f44ec14a4be1f077`  
		Last Modified: Fri, 04 Jul 2025 01:18:49 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06942f5776dc6ef0069eb5b3fcda6a7bb40d775c63f6341a9640687eb34a1589`  
		Last Modified: Fri, 04 Jul 2025 01:26:03 GMT  
		Size: 25.2 MB (25194392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75698d7d739d2408ad6c676bee67c427108f33e22360e562b0416bbb6ba39b0e`  
		Last Modified: Fri, 04 Jul 2025 01:26:01 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b5f9bee2dcbe097aa37da36864c3f1486ff1d40bde9f66bbaed69cee90f5ef`  
		Last Modified: Fri, 04 Jul 2025 01:26:02 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f3aa27f5383a264eb96b608b6aa562def5578ece647fb984daf0fc38ab3540`  
		Last Modified: Fri, 04 Jul 2025 01:26:02 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1410800bf25502b3b9212b18e2dbe9ee4efa7f3f69357d9c2264d44079906d03`  
		Last Modified: Fri, 04 Jul 2025 01:26:02 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164ec360fc79a9168448988bc62f0091eb804f3045d0abde30cffd5181c47ca6`  
		Last Modified: Fri, 04 Jul 2025 03:01:03 GMT  
		Size: 25.2 MB (25161760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4347b06b5adb4ce37eb20bcc7221faee8ef8ff747bca3e628081bec0a5af90`  
		Last Modified: Fri, 04 Jul 2025 03:01:02 GMT  
		Size: 12.5 MB (12471368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b563bfe6dc0918f53ee0b2c5baf5e4718240d595ad1dd9e6753f80eedb5e246d`  
		Last Modified: Fri, 04 Jul 2025 03:01:01 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc864af23df65adaf0529a0c046305fa7a2fe86c7742d627e4fd0f676c690ab6`  
		Last Modified: Fri, 04 Jul 2025 03:01:01 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36e639e5dd09aa19d48446611d530642e15bdeb7f107c79ec83e9230773fcd5`  
		Last Modified: Wed, 09 Jul 2025 21:24:05 GMT  
		Size: 26.9 MB (26898468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14590f8705cd3fccf60bf0ba3f5313e0b23a8a8bf62bf48bb8ad7dac717710b`  
		Last Modified: Wed, 09 Jul 2025 21:24:03 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77a0de1e3071d3da4f91f20da98fc763c233c4e6b1efc6c0e9ca39376e83f11`  
		Last Modified: Wed, 09 Jul 2025 21:24:04 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ac8e19ff0895aa7b28152ae888e5b11e69062a277c1cad83ba2d9ec7e9c6a90`  
		Last Modified: Wed, 09 Jul 2025 21:24:05 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8.2-RC1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:a654edd3905a6faaa5a336b9088e5f44fdc1b17d20c3a89f4695436a26b68c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7697240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836ef56f15cdfc012ec9f95f98de9f9deb17728ecb3341118c71a1bdf3cc0395`

```dockerfile
```

-	Layers:
	-	`sha256:c3f6f811a0128f01a5a2a50c80f3f465bcf238a789e6b6bfceeb6dda446edea5`  
		Last Modified: Tue, 08 Jul 2025 22:15:09 GMT  
		Size: 7.6 MB (7643100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85034ea8ddeef56adea7292ad271cc2f5a866a5339facbe897e1b026f1985cf1`  
		Last Modified: Tue, 08 Jul 2025 22:15:10 GMT  
		Size: 54.1 KB (54140 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8.2-RC1-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:d744dd0fabd00ba0a7ca9c72fcf8f52cf49f54341c3dc12223d6c3cd19d871e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.6 MB (233569609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f3a979af7dd52da5a0084b4b809a3b387ece8a0dc68a45f25beeeb410b18c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06f0a25db22853df6a6e6e4155e86895f626a540d37bf7e50bf413fd1fa8f12`  
		Last Modified: Thu, 03 Jul 2025 22:57:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d119d74c86b221b030b9083d0f51ada6b53b7c58ec2a87c7276bf5229a2d16`  
		Last Modified: Thu, 03 Jul 2025 22:57:42 GMT  
		Size: 98.1 MB (98130784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81367bd3a505020af3e40d8bc05177f06efe70245dd3740395c2183000421e42`  
		Last Modified: Thu, 03 Jul 2025 22:57:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc52c5ee84b97f4b6896417365b48fb16b142012e81662c47c8ada49a6fed5a`  
		Last Modified: Fri, 04 Jul 2025 00:52:50 GMT  
		Size: 12.3 MB (12272131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f3e08efb91357f62eef9c33f57b75cef142146846a08594a94651aaf203701`  
		Last Modified: Fri, 04 Jul 2025 00:52:48 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd91221b9916180691d9c5fa2d031c218b8872daeaef9715e675772a43222436`  
		Last Modified: Fri, 04 Jul 2025 01:00:31 GMT  
		Size: 27.6 MB (27590380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9847660bf77ac331de98c91f632dcaf31a2cadc3e2ac13eb362472a461459600`  
		Last Modified: Fri, 04 Jul 2025 01:00:29 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec259207ab2810fedf80398c18f23d799acc85719da5c1dffec290bf3ed3332d`  
		Last Modified: Fri, 04 Jul 2025 01:00:29 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af053d2b196f12b9e47ca19e02a45c2791236b02e3ae7bbff051c37a14c5bbf6`  
		Last Modified: Fri, 04 Jul 2025 01:00:29 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48f644793d9968655454dde283d44cd21ad1190c3b96deb09263a9074678db1e`  
		Last Modified: Fri, 04 Jul 2025 01:00:29 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89d3a59f491f7c62a587fae4a1ce548b8693bd50940b810a7d53230a23dada8`  
		Last Modified: Fri, 04 Jul 2025 03:38:39 GMT  
		Size: 26.3 MB (26286541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f702bbde967f249affaa5c9476cf70aa9e4334bf9d1f09f71b00b240670e1e`  
		Last Modified: Fri, 04 Jul 2025 03:38:38 GMT  
		Size: 14.3 MB (14295417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e50ae8a8d6063e790d6dd5da53b6059635a62e5e69713ea721d18b26bbb061`  
		Last Modified: Fri, 04 Jul 2025 03:38:36 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2deb28df401aea9902b123080391e694c960989cfb1cd659b8377466a4c31e1f`  
		Last Modified: Fri, 04 Jul 2025 03:38:36 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b961e0d8c5beba1e93e5bd95685ef2e00414918c16916dc0d1a3e59c91da07f7`  
		Last Modified: Wed, 09 Jul 2025 20:25:51 GMT  
		Size: 26.9 MB (26898473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbde4ba24d3d5b41fea6d502593ded8da8b4c3b185ded2fd72ff907ae80b2322`  
		Last Modified: Wed, 09 Jul 2025 20:25:49 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca4f455b1090fe8f202738a9c274737691c0e95722be38bb3985d48555f647a`  
		Last Modified: Wed, 09 Jul 2025 20:25:52 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0760ec93b2a2cd6ae3a69a76ebc94cbed052ec5596b3b3518e53b8bda18261ba`  
		Last Modified: Wed, 09 Jul 2025 20:25:54 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8.2-RC1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:ef3ab987e04d52757fbdf5a589e8160c39b64ef9ecadd295ccad52501cfaa847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7917205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7058ce1ae124557532a73a34c152ed537d47672843e206435909a953072856`

```dockerfile
```

-	Layers:
	-	`sha256:6158e209c121482a04b3b529d10ed70f83de592173a245ed8a7a163f13715ee0`  
		Last Modified: Tue, 08 Jul 2025 22:15:16 GMT  
		Size: 7.9 MB (7863003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e825cf7014762c121d3f9f3117b012568697277914c79110e8004c2e2abf9ab1`  
		Last Modified: Tue, 08 Jul 2025 22:15:17 GMT  
		Size: 54.2 KB (54202 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8.2-RC1-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:c9528359dddd74f8c7af758b4c8db4eb60e99ac68b19a0d8111ce9715354ab47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238852372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe9f60c3a5088bb72ce7ea5adf35c7cbbd7aa5d4f6a864451224efaf66eb013`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a24324802d6c1954d265483ed013ba2369e5cffd5a95d994022ebdbf3650cc`  
		Last Modified: Thu, 03 Jul 2025 23:08:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada39c11a5b43d4490bf6d09b50bad18bf2c449580f4e4f7d1b0938bb16b64fa`  
		Last Modified: Fri, 04 Jul 2025 00:11:18 GMT  
		Size: 101.5 MB (101515253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9462ffea36f638f242abb7ebb1b7b74092acb453d951ae056eb6080650429089`  
		Last Modified: Thu, 03 Jul 2025 23:08:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056502d644d78d77ed4a45f848cff8e6461803be80098af4ef87665625df730c`  
		Last Modified: Thu, 03 Jul 2025 23:08:25 GMT  
		Size: 12.3 MB (12271414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f8bba753631ea1d2dae6add440571473a8d59e329dcc601a261c480b978b854`  
		Last Modified: Thu, 03 Jul 2025 23:08:21 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8761a630b39aef3b5071d77cf48f1b4ed193a620b5bda0fd660cfeee0c1584fd`  
		Last Modified: Thu, 03 Jul 2025 23:08:32 GMT  
		Size: 28.1 MB (28119728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a879a4e2822f1a6c6bf6406663548d1823f766c3adf570ceaa15d2570d066619`  
		Last Modified: Thu, 03 Jul 2025 23:08:23 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b53739685eb250a0b8898223b1f6f6b021d72ddb650dbd923ea801ef63ad65a`  
		Last Modified: Thu, 03 Jul 2025 23:08:24 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e96f04ee5e23bfae586a0c5ed65e0f22909ecceadbd18823d9c693dc7e344d`  
		Last Modified: Thu, 03 Jul 2025 23:08:24 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71360f61352cf716968a205500370cfd81e7bba4a40f9781215731bca466b54a`  
		Last Modified: Thu, 03 Jul 2025 23:08:26 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fe322e75c3b270afb2804bfa88c6cc6e270c0adf5a95dfeb8fc24960707b6a`  
		Last Modified: Wed, 09 Jul 2025 21:24:51 GMT  
		Size: 26.8 MB (26828487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eac5ac29c1a253aff6609e80a3c6653a310a56213e88ce2954bbe4e5c2412a8`  
		Last Modified: Wed, 09 Jul 2025 21:24:47 GMT  
		Size: 14.0 MB (13988366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81940b695247f28ac189f85245e8e59fc3f7b7b81c14a4c633a0b5d843d92aaa`  
		Last Modified: Wed, 09 Jul 2025 21:24:45 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d302251400481c62b922f62ffc26e107f56b34f30c9fdb49e26a129d6877be`  
		Last Modified: Wed, 09 Jul 2025 21:24:45 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a151a45cbd0f90e0d615b2943c91fd962fd107a054cf93772c2a7cff0f8cdfa`  
		Last Modified: Wed, 09 Jul 2025 21:24:48 GMT  
		Size: 26.9 MB (26898482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7e0a660919e89fcbd5d1161f0b9025468c0e39fe07c0bf06e96ae3524aae31`  
		Last Modified: Wed, 09 Jul 2025 21:24:48 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b4e9ecd06fccad758ae36208924750d77fd8fd7ea71e0e2dc9496dde365cce2`  
		Last Modified: Wed, 09 Jul 2025 21:24:48 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276e93e51bd35e5050e0f11c1edafe6a786b68284d1c375241ef14f5eb37587e`  
		Last Modified: Wed, 09 Jul 2025 21:24:50 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8.2-RC1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:7c34138b4ec25b78fbbefa27e0e16d7227fe615560b905e29dece6386f2dc54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7861755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:854ce20a7130fae98cea4a5e4f39353b8bcf01fe96e837a7da58a280e540be02`

```dockerfile
```

-	Layers:
	-	`sha256:9a95523982a07bf7edf35ebe86180aa96c5f1543f4a2750fb97d93db9a5816ed`  
		Last Modified: Tue, 08 Jul 2025 22:15:23 GMT  
		Size: 7.8 MB (7807867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56c88ec6406beac97c65a491dc2562d55bdf474f005cec7da1341017a3184d14`  
		Last Modified: Tue, 08 Jul 2025 22:15:23 GMT  
		Size: 53.9 KB (53888 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8.2-RC1-fpm` - linux; mips64le

```console
$ docker pull wordpress@sha256:a2e72c996383c46a141ccfde06f2f9e87840b6f7cf7285dc8bbda4b0b523b45c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.7 MB (214702052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c4a97c653da12c05efbbd82363f87bc8628f44b945453cd0121f47ce72f80a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1751241600'
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fcacdf0767dbc0b08ad73fb46ff36dc2ec6b87367debc1e5018464dc1d3d7035`  
		Last Modified: Tue, 01 Jul 2025 01:15:02 GMT  
		Size: 28.5 MB (28516734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5e69eb612928f2b1edb8b79310fa7eb01b97eda1179aabfcea5395120a404`  
		Last Modified: Tue, 01 Jul 2025 04:33:31 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60c6c65191f30a3311d0f913382becc510cfefba81063f7617c9b537f70c6f7`  
		Last Modified: Tue, 01 Jul 2025 04:33:43 GMT  
		Size: 80.7 MB (80668384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bdcd15545dd72fcd7e549e199c0795e04a22a395d9ecc76e94dbc2d57e32d7`  
		Last Modified: Tue, 01 Jul 2025 04:33:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e52fcee92a20468faa7d3c982185b7691006ae6e310a75c5b2acb52427a4d5`  
		Last Modified: Fri, 04 Jul 2025 01:32:09 GMT  
		Size: 12.3 MB (12269918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d7f850fdbdcf3a1808687849c4a56bf71ba202e482e2c7d0c40595b224db65`  
		Last Modified: Fri, 04 Jul 2025 01:32:08 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b9a8d86e545a0ab7e77f1ec197f99bca84d28f1e4145291b7f9a684ed71b74`  
		Last Modified: Fri, 04 Jul 2025 02:05:23 GMT  
		Size: 26.7 MB (26692996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b337884be34de72e6d19b3aa9f6a42d9a37c01652df5df9ad285c6be574364fb`  
		Last Modified: Fri, 04 Jul 2025 02:05:21 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec5fd8fd8cb4abda46c3b5a0d1fd4d381c52c83f39c8325e03295fc80d59688`  
		Last Modified: Fri, 04 Jul 2025 02:05:21 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0e51e6df41ffc17943fe3232b5de2d7bfa89f2692a3afa102ac4223e314cbf`  
		Last Modified: Fri, 04 Jul 2025 02:05:21 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63170ed37f83befa702b0014124402b1c740e2b2541e6e5df00c79d045d9bc48`  
		Last Modified: Fri, 04 Jul 2025 02:05:21 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36fbff7d45e718006cb47d9fdc3123d5f04786c1ae5597610fb3182a76e8084`  
		Last Modified: Tue, 08 Jul 2025 22:16:22 GMT  
		Size: 26.2 MB (26153747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4884da393f881296b2b9052e4d6d97ff5a44bf43ba255606fccbed83bd981852`  
		Last Modified: Tue, 08 Jul 2025 22:16:22 GMT  
		Size: 13.5 MB (13483568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61282dff0812ccd58caddd5609a8c379b62695b6c887633e716a0dbf067651ec`  
		Last Modified: Tue, 08 Jul 2025 22:16:21 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a195b1bd6da416165ecc146669e2f2ca5e437d1a7724f9d2c6dbefd5dce41ab0`  
		Last Modified: Tue, 08 Jul 2025 22:16:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35783f19193a30366f6d1703bd560239bf5d6b19d429ad0a184b873aa91f2475`  
		Last Modified: Tue, 08 Jul 2025 22:16:24 GMT  
		Size: 26.9 MB (26898481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586925b208c7449ba62e7257d59e1e75eff4afda8da1e2d685904b07586ae9c4`  
		Last Modified: Tue, 08 Jul 2025 22:16:22 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65bd41e273d2bac3232f02eb58cc5fb49883c5c1ac13980fb1c250274cd03ca0`  
		Last Modified: Tue, 08 Jul 2025 22:16:22 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd5ce077ab6be3562888f8069a31554f3b32175adca66b9e2bbe626eabee2b`  
		Last Modified: Tue, 08 Jul 2025 22:16:22 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8.2-RC1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:f34a96256c7ae37580fae7f792ffa408a5eaaf67a840eb0d2e6d059e92d17236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 KB (53871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f33ff67287cbcfc0945650b4ff7c7546ff3ed3995c2049b0cc99c808ddc3fe09`

```dockerfile
```

-	Layers:
	-	`sha256:376ecb887375d0f750673833f56a00a87d4abb172fe8bbfa8cef9f58646a6cff`  
		Last Modified: Tue, 08 Jul 2025 22:15:30 GMT  
		Size: 53.9 KB (53871 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8.2-RC1-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:9a64e7e60e00bedf93734091272ad9adff4d47dd5aa96e35d2246fb8f28ef660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246863175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edba16b9106b566f3f198d8857aae730b6cf00ddfaa46270814feba70f8afa90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1751241600'
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c5884d20b08634214a92bd5de559876bf30e6c5453807c3014f5480eeba20662`  
		Last Modified: Tue, 01 Jul 2025 01:15:20 GMT  
		Size: 32.1 MB (32072820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36b68bed4d5c4fdbbd3f66cf1ee62569453e6d1dea00500a229578b96f8f6c3`  
		Last Modified: Thu, 03 Jul 2025 22:59:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c94ede1a54d9ac4e13b34ad1cd441b94ad5436ccfacbf6f1e5deb2957a47257`  
		Last Modified: Thu, 03 Jul 2025 22:59:12 GMT  
		Size: 103.3 MB (103326831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83487f2c5b5e9a02c2d3911052a6efe6e28cc68c5a06b7a0080d8ff6f6a2c72`  
		Last Modified: Thu, 03 Jul 2025 22:59:08 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997d8125a76ab4278ece79101a12541fd05f6a867797528b16876d66660c1d91`  
		Last Modified: Fri, 04 Jul 2025 00:17:07 GMT  
		Size: 12.3 MB (12271796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aabe88513bd28438cbb41b882b2746af427e8a30983889b8618dabdb5423aa0`  
		Last Modified: Fri, 04 Jul 2025 00:17:06 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9a6cd446b4daa72cc2ac680ba1edff5cfe933ce9a0ecb9c7f37a36ac5e2005f`  
		Last Modified: Fri, 04 Jul 2025 00:25:12 GMT  
		Size: 28.7 MB (28652420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cac8190c6127f0f22191b21ebfce18970e651c8d1cb7fbb99df8e6d9b8a20e3`  
		Last Modified: Fri, 04 Jul 2025 00:25:10 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c254088dac74d778c3b632701c6069cc989b70814a10b93239bd6557f03c1b`  
		Last Modified: Fri, 04 Jul 2025 00:25:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:585f14929c4b5ee95085fec187c630d187fa34ae6a738eb9c9f69a9505b8aa0e`  
		Last Modified: Fri, 04 Jul 2025 00:25:10 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38686d46686aa473429b0c81e10584b779437b065654a62893b47e4fc87cd4c6`  
		Last Modified: Fri, 04 Jul 2025 00:25:21 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0be3f462dfa2f5032c3475d9833dcc94899c5000adb5a156f727373fec3d58`  
		Last Modified: Fri, 04 Jul 2025 01:51:09 GMT  
		Size: 27.5 MB (27475511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7a4ed77d483e372c2103a70b00414c593e27d79300efd0879fd7bfed8f760f`  
		Last Modified: Fri, 04 Jul 2025 01:51:08 GMT  
		Size: 16.1 MB (16147112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a80fc545c3dd9e00975b3e1bd9734845462c333b517c5efc70b6ad6ec4c87e`  
		Last Modified: Fri, 04 Jul 2025 01:51:07 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bc4962b532133cdee592d3c0cf6a728bfa84dcc371dbc1f28b8c391a3cbd74a`  
		Last Modified: Fri, 04 Jul 2025 01:51:07 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cc5c0662c311ceb3cbe231026c2fb0a36c58e00cfde9023eb5675ad5930a2c`  
		Last Modified: Wed, 09 Jul 2025 21:25:34 GMT  
		Size: 26.9 MB (26898478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed020b4e2915de8c45fbca91a62bf4dd5ad100aa9fdb44bf6a8a9a1e0bfaf94d`  
		Last Modified: Wed, 09 Jul 2025 21:25:32 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fafc462b78f78ee0001fad6f960906c55db49d09dc465e1bec75e6646b951aa`  
		Last Modified: Wed, 09 Jul 2025 21:25:33 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f5597aa9a1ec4360e09226dade28595d54a1d67062cb71585ab9fe10759a3b8`  
		Last Modified: Wed, 09 Jul 2025 21:25:33 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8.2-RC1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:63e677c24d7bd8e52b0dc69b54be12199f62591cab33bd8bd6f86d89b5c0eb1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7866960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cdb945b05c6472ed67d222bfe3d7f7fbedbf5e5513020d1f4ad03ad2f32ecab`

```dockerfile
```

-	Layers:
	-	`sha256:ca073c3b39b96980712372470ec1fb74551be2bae7fe385eee9f0b04cf1f8e00`  
		Last Modified: Tue, 08 Jul 2025 22:15:33 GMT  
		Size: 7.8 MB (7812910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9b335dd8f5425ee509a6fceae05e94616e97a699b319a955f1527c0e397698`  
		Last Modified: Tue, 08 Jul 2025 22:15:34 GMT  
		Size: 54.0 KB (54050 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8.2-RC1-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:6e62e4cb364dff035b987b099bba02cbbf0e7213ae7bf9319416b968dca49221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213597817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3630b8ef82c24eb42211ff596f7f50cdfe7a1d03fd6f91c25ec33e1bc72bbcea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1751241600'
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libavif-dev 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:46b41ca6e821ec27aa0ddf43e603c69ca49f20e377997e4087ed991c9635aa70`  
		Last Modified: Tue, 01 Jul 2025 01:15:56 GMT  
		Size: 26.9 MB (26887811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20eb609875faf51e20c0ced671506012769a509c263093fc793d0aae0bcc9b5b`  
		Last Modified: Thu, 03 Jul 2025 22:58:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528c62694487a8c0f3520f828eaa12f12ec29ad4944569d71931f79d7011e046`  
		Last Modified: Thu, 03 Jul 2025 22:58:51 GMT  
		Size: 80.8 MB (80825817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbc2722da34fe4bf90187950be5838def4ad6dd2e97500d7f8d44fbb460783d`  
		Last Modified: Thu, 03 Jul 2025 22:58:46 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb8d4f5638d9f62e2ea9c4e82420e0926e36d2b4db557d0cf771001154767c`  
		Last Modified: Fri, 04 Jul 2025 00:20:37 GMT  
		Size: 12.3 MB (12270732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5440f58ffbc9adf9e9a68e76f10565e433e4a78f5c2ca77e2564f86a8c3dae84`  
		Last Modified: Fri, 04 Jul 2025 00:20:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1880cea240dcddfd7f026e0ad0db96496063afa9829d5bd61025fa547597f67`  
		Last Modified: Fri, 04 Jul 2025 00:27:18 GMT  
		Size: 26.7 MB (26704925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e601855b692db39dcec10620fbe6162fcd661ab89e29c889f61850104a6f4326`  
		Last Modified: Fri, 04 Jul 2025 00:27:16 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0a868d692eed7215d79937d449ff2aa21d36ab862fd6bd3c97bff0849d87f4`  
		Last Modified: Fri, 04 Jul 2025 00:27:16 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce2e286ca4f7f23cb9680c8a69d4c4694c975420c514dc1c33d8866afbf05e7`  
		Last Modified: Fri, 04 Jul 2025 00:27:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7eb5ed67bd1a1094caff6377e13f7732ac24fbdc82bf18cf2c84d003457449b`  
		Last Modified: Fri, 04 Jul 2025 00:27:16 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc5aa4384e55a8b98527805b87f24088718a8a9a02cd814ebe121569fc86f55`  
		Last Modified: Fri, 04 Jul 2025 01:41:04 GMT  
		Size: 26.0 MB (26012727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b1917548640f52615dd991c7d8c09079e891f0d9f1e36dbdfd9de33afa6e3b`  
		Last Modified: Fri, 04 Jul 2025 01:41:02 GMT  
		Size: 14.0 MB (13979105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c14b82525d7d591c5760194fcb1cc0bf228b386e924eeb95072a4323193673f`  
		Last Modified: Fri, 04 Jul 2025 01:41:01 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023e9a61e1827825dd5e1931efe0842a1759146cac867011e8095cd7bc8c9e46`  
		Last Modified: Fri, 04 Jul 2025 01:41:01 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aa8c198049df1f55c0db1f20747ee46c3a4485bec47286e2b86451bb1c613a`  
		Last Modified: Wed, 09 Jul 2025 21:25:55 GMT  
		Size: 26.9 MB (26898491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868380b70d18f3996dc5a0da10ae6e55aec57f5d9aede8ffb9258f9431a14f26`  
		Last Modified: Wed, 09 Jul 2025 21:25:53 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ff01cdbf2a1a3410e09c3defc5a93cc61476e8b952da3b6cae8ac4bd8ad3d5`  
		Last Modified: Wed, 09 Jul 2025 21:25:54 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bed186db56b5b5c371661df707e7c69f18b0d45f9b389934d07decab523ae5`  
		Last Modified: Wed, 09 Jul 2025 21:25:55 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8.2-RC1-fpm` - unknown; unknown

```console
$ docker pull wordpress@sha256:091f142afbcadaf91e02e7ebb0e5c70e0042673dd70772dc8b811a9d827c2d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7713449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06f993a7ad8bf67d58486808afdae2c3763ed335d8b3a7a25db38805b1b7a5e`

```dockerfile
```

-	Layers:
	-	`sha256:75f1b1238c3699cb2093e0d3aaa37c1b488846c7f0f49de86d0cb3f8553f5668`  
		Last Modified: Tue, 08 Jul 2025 22:15:40 GMT  
		Size: 7.7 MB (7659500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ac201a5743b88c2ea751414e2406810b6f748e64db9be26db2f59c3a22613ce`  
		Last Modified: Tue, 08 Jul 2025 22:15:40 GMT  
		Size: 53.9 KB (53949 bytes)  
		MIME: application/vnd.in-toto+json
