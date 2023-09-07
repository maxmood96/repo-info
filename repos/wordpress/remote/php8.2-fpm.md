## `wordpress:php8.2-fpm`

```console
$ docker pull wordpress@sha256:2f573e3995a82fceca85ec27e18c8f621be83c510e91a063848282234f366b2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `wordpress:php8.2-fpm` - linux; amd64

```console
$ docker pull wordpress@sha256:e1eebf813c4f76193145fd0f8109e46c35ebad06dfe8baa03747dc903a5320d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253180957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626d1aa2976f501b38573cd7ccda026299dace4fc364d7d30ab03aadd2085698`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 16 Aug 2023 00:59:46 GMT
ADD file:997f5a9b32407d96efac41a1cfafb318f77de077c8b5cd7065b6ec9796b4bf5e in / 
# Wed, 16 Aug 2023 00:59:47 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 02:12:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 02:12:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 02:12:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 02:12:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 02:12:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 02:12:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 02:12:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 02:12:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 02:41:04 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 06:35:31 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 06:35:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 06:35:31 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 06:35:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 06:35:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 06:46:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 06:46:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 06:46:44 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 06:46:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 06:46:44 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 06:46:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 06:46:44 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 06:46:44 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 06:46:44 GMT
CMD ["php-fpm"]
# Mon, 04 Sep 2023 15:29:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 04 Sep 2023 15:30:21 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Mon, 04 Sep 2023 15:30:22 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Mon, 04 Sep 2023 15:30:23 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Mon, 04 Sep 2023 15:30:26 GMT
RUN set -eux; 	version='6.3.1'; 	sha1='052777aef40e7f627c63c8a26eefe37b843a44df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Mon, 04 Sep 2023 15:30:27 GMT
VOLUME [/var/www/html]
# Mon, 04 Sep 2023 15:30:27 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Mon, 04 Sep 2023 15:30:27 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Mon, 04 Sep 2023 15:30:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 04 Sep 2023 15:30:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:52d2b7f179e32b4cbd579ee3c4958027988f9a8274850ab0c7c24661e3adaac5`  
		Last Modified: Wed, 16 Aug 2023 01:04:30 GMT  
		Size: 29.1 MB (29124563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635676b59bff48bb8bf1480dd07a2ec477ac43d5d8f589b04a4b49600280dbf0`  
		Last Modified: Wed, 16 Aug 2023 04:30:36 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dbc2d7054ba7a357e67b9a5bbeb76074fa786bbeb65777f71fbbc4106e616d`  
		Last Modified: Wed, 16 Aug 2023 04:30:51 GMT  
		Size: 104.3 MB (104340610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8748b1b28b494d0c88f7ff96b5b0e31ae6f2db72cafa2a6f4e6f50f9359c2c26`  
		Last Modified: Wed, 16 Aug 2023 04:30:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cccfd282f9b3b171618286c3a0df70baae4787b972bcf4d202f7bae035638e8f`  
		Last Modified: Sat, 02 Sep 2023 08:35:00 GMT  
		Size: 12.4 MB (12354634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b6f2bb26004a477bd8728dbd6b281dd28fd001d0f87e64ce7ec81bcf14582d`  
		Last Modified: Sat, 02 Sep 2023 08:34:59 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2fc59ad47bc49f429f9e1b76a7b70d0ed89e78bcc0e32b7111af789281e61d`  
		Last Modified: Sat, 02 Sep 2023 08:36:10 GMT  
		Size: 27.8 MB (27793186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf13dac9526759df137a36cd01fd924919485135661c73419a362757fd331cdc`  
		Last Modified: Sat, 02 Sep 2023 08:36:06 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e89b7036b992924d12cf334061a96df757da1b88098e75738c938853d9c6153`  
		Last Modified: Sat, 02 Sep 2023 08:36:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9add0967676b70701b3b17ba3de8b5c51c582d636e6f19ebb0c35b966f936db8`  
		Last Modified: Sat, 02 Sep 2023 08:36:06 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd30862005a71f131cb1499bf00fc7cd6372add3cfbcc84e9eb1fe28ffbe1d0a`  
		Last Modified: Mon, 04 Sep 2023 15:37:05 GMT  
		Size: 26.4 MB (26376741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99482198b7688f78a097dbe26bd75ba1aa8a3de1ee4d23d979ed9148a02fe881`  
		Last Modified: Mon, 04 Sep 2023 15:37:06 GMT  
		Size: 29.9 MB (29899979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d926d2d062e0f2a61cf8cd70eb433f442e3f565ed37af75185c0e2f2fee876`  
		Last Modified: Mon, 04 Sep 2023 15:37:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bca27162138d71b833f756e94b53d285168a61a798b45eb35844bf0c43c880f`  
		Last Modified: Mon, 04 Sep 2023 15:36:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c1b3987c904e1c539ba1bf89c022b1f25b9528731b13e17bb5de948b64a1ee`  
		Last Modified: Mon, 04 Sep 2023 15:37:03 GMT  
		Size: 23.3 MB (23273533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f04322d8aa09c6eaaf9abda7cda3dc4bd0301e7b7d03c554d163bd3a867f45`  
		Last Modified: Mon, 04 Sep 2023 15:36:59 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca43fc16de2f4b66e8858bd985f9762f17e600aa34c8d4dc9a59c488afee44ae`  
		Last Modified: Mon, 04 Sep 2023 15:36:59 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php8.2-fpm` - linux; arm variant v5

```console
$ docker pull wordpress@sha256:7383188bc5f553d8caf940667e72a3facfc8d2429f8be4dd3632dbd362142cd0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.5 MB (223467822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0973b8aa258552f82a2bd5be7029de6a90e8fba2fb48c478b71fe08bf77ffa7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 07 Sep 2023 00:48:30 GMT
ADD file:e7b77e5797ddb7e058507462fd5f5aad6864ba08ebc4a6c2743dae81ed0f445d in / 
# Thu, 07 Sep 2023 00:48:31 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 01:11:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 07 Sep 2023 01:11:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 Sep 2023 01:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 01:11:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 Sep 2023 01:11:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 07 Sep 2023 01:11:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 01:11:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 Sep 2023 01:11:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 Sep 2023 01:37:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 07 Sep 2023 01:37:16 GMT
ENV PHP_VERSION=8.2.10
# Thu, 07 Sep 2023 01:37:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Thu, 07 Sep 2023 01:37:16 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Thu, 07 Sep 2023 01:37:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 07 Sep 2023 01:37:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Sep 2023 01:45:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Sep 2023 01:45:53 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 07 Sep 2023 01:45:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Sep 2023 01:45:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Sep 2023 01:45:54 GMT
WORKDIR /var/www/html
# Thu, 07 Sep 2023 01:45:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 07 Sep 2023 01:45:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 Sep 2023 01:45:54 GMT
EXPOSE 9000
# Thu, 07 Sep 2023 01:45:54 GMT
CMD ["php-fpm"]
# Thu, 07 Sep 2023 14:52:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 Sep 2023 14:53:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 07 Sep 2023 14:53:44 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 07 Sep 2023 14:53:44 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 07 Sep 2023 14:53:49 GMT
RUN set -eux; 	version='6.3.1'; 	sha1='052777aef40e7f627c63c8a26eefe37b843a44df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Thu, 07 Sep 2023 14:53:49 GMT
VOLUME [/var/www/html]
# Thu, 07 Sep 2023 14:53:49 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Thu, 07 Sep 2023 14:53:49 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Thu, 07 Sep 2023 14:53:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 07 Sep 2023 14:53:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d971e043cc5e8068fe39c736806d279b128c720a08d2e0d41002dcf027787939`  
		Last Modified: Thu, 07 Sep 2023 00:51:35 GMT  
		Size: 27.0 MB (26983530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02aad406c905f84981df74ef828e09148cd5014924dfbffd72809e40b22bf1b7`  
		Last Modified: Thu, 07 Sep 2023 02:42:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa99c5db0e2b2db0e03293c0b8668f52b971e7eec6c95b74c1b041bc68336b6d`  
		Last Modified: Thu, 07 Sep 2023 02:42:53 GMT  
		Size: 82.0 MB (82026515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2217e264f2268ac3618d71edbfa1493e7bfe4df9920f379c40a77f0882961d4c`  
		Last Modified: Thu, 07 Sep 2023 02:42:35 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cfbc9250f7a12446082660faf93c02777b87935be7b8af146d84261fbc5229`  
		Last Modified: Thu, 07 Sep 2023 02:45:27 GMT  
		Size: 12.4 MB (12352924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2782ebee432a84c292f86fa879808ca831153847a3d104b24b4664c23dedb4`  
		Last Modified: Thu, 07 Sep 2023 02:45:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41fca091185e1741f94c55890c418ae46040c2486403c449724e000125e4ca88`  
		Last Modified: Thu, 07 Sep 2023 02:46:43 GMT  
		Size: 26.3 MB (26291953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672241f4157990517958da7f3599b882d476e1d323430df0544468dabea24691`  
		Last Modified: Thu, 07 Sep 2023 02:46:36 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:106481d62f2acd77a409225ea31b5db242df98245eee050cf33c9f0a9d495b6a`  
		Last Modified: Thu, 07 Sep 2023 02:46:36 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b85cf4b14d002e74e4afb3e055bcd420f8c248ae6895209c8ce64505336a553`  
		Last Modified: Thu, 07 Sep 2023 02:46:36 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3752e7cd7dc9ffaaeb5dd04dbbd596910b782f0ac2bb8df4379c7a424dd2d218`  
		Last Modified: Thu, 07 Sep 2023 14:57:37 GMT  
		Size: 25.8 MB (25821679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64326c257bfee19020e8a3e66d28ff72764f2559f30666c3524f807d7072840`  
		Last Modified: Thu, 07 Sep 2023 14:57:37 GMT  
		Size: 26.7 MB (26699984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47af781e45abada44b570c2b468168ccd74bf695970537fa973fd86e9b17fda`  
		Last Modified: Thu, 07 Sep 2023 14:57:30 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40231d433dc11e82ed87a9a3e610449ac46d54f99a5d6672f2b14535ad0dc34a`  
		Last Modified: Thu, 07 Sep 2023 14:57:30 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab20e54f5326508685c0bddfe091d74f3dfd6c5bb90736358c617ce2192e3fe`  
		Last Modified: Thu, 07 Sep 2023 14:57:34 GMT  
		Size: 23.3 MB (23273553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7077068c798a0c1c33093240c74647a153fc2174cb9811fa00075d2eb53f9fe6`  
		Last Modified: Thu, 07 Sep 2023 14:57:30 GMT  
		Size: 2.3 KB (2346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6348d7363c090178088f9919e0206f09af1285511a553c81d7cd19cc4542390d`  
		Last Modified: Thu, 07 Sep 2023 14:57:30 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php8.2-fpm` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:f64a7c27bb0a38e6c66e8b0d0b4f259906880094c8c0036120d67ec659e41cd7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.4 MB (212370150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58222089d7f48b033d020b1d3d9ec767730684664f7d9d0984c30787fad85ec5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 16 Aug 2023 00:17:12 GMT
ADD file:45cc27bd11f601d2fef5d7494a1a6253287e6d22e108e39c0884761c7533cd9c in / 
# Wed, 16 Aug 2023 00:17:12 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:09:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 01:09:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 01:09:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 01:09:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 01:09:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 01:09:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 01:09:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 01:09:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 01:34:00 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 02:44:31 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 02:44:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 02:44:32 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 02:44:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 02:44:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 02:58:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 02:58:50 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 02:58:51 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 02:58:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 02:58:51 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 02:58:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 02:58:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 02:58:53 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 02:58:53 GMT
CMD ["php-fpm"]
# Sat, 02 Sep 2023 07:27:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 07:29:11 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Sat, 02 Sep 2023 07:29:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 02 Sep 2023 07:29:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 02 Sep 2023 07:29:16 GMT
RUN set -eux; 	version='6.3.1'; 	sha1='052777aef40e7f627c63c8a26eefe37b843a44df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Sat, 02 Sep 2023 07:29:16 GMT
VOLUME [/var/www/html]
# Sat, 02 Sep 2023 07:29:16 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Sat, 02 Sep 2023 07:29:16 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Sat, 02 Sep 2023 07:29:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Sep 2023 07:29:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a44aa9565b062e4216f7b39ce6c67dcc5376e10f76caec55bd3acd1cc8b76b75`  
		Last Modified: Wed, 16 Aug 2023 00:21:27 GMT  
		Size: 24.8 MB (24805419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08b4dde5a9219b85577e6b27a7ad67564abbd05e87b21ddbba71ef5765ef432`  
		Last Modified: Wed, 16 Aug 2023 03:05:55 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8f9a339e07912a00b79ade0609518d0b6c9a890ef8ed5b1aaf6f123b28fa2dc`  
		Last Modified: Wed, 16 Aug 2023 03:06:07 GMT  
		Size: 76.2 MB (76217037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa7b4363d3fbe8892ffc33a00cc8899d85c243b0f9d757d4824e7725a6d0b1d7`  
		Last Modified: Wed, 16 Aug 2023 03:05:54 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6b9ea9a9103e929aafb0f8b7dd6510bd639f1dc591b85c4a8bad655d3f4bc5`  
		Last Modified: Sat, 02 Sep 2023 04:38:40 GMT  
		Size: 12.4 MB (12352911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e80c8044e8180f4ce9cecbd0f908e2fecf929169a25d47ac2c114794e2d50e`  
		Last Modified: Sat, 02 Sep 2023 04:38:39 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d1114fccd2aa62362900c36a851e2c46f3632656197c3873bf48ec846ccfd9`  
		Last Modified: Sat, 02 Sep 2023 04:39:53 GMT  
		Size: 25.4 MB (25400486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b16d71ab54925004181bc03e45acb80506572fc9e1af72526801d68e14e5144`  
		Last Modified: Sat, 02 Sep 2023 04:39:49 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23c685db7081673e03e88568dd7f2a41d3befa8f286c6ba7526d461fa44dfd14`  
		Last Modified: Sat, 02 Sep 2023 04:39:49 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef62c80b297d2555ad1564b78a8372011270187473c8942adc6c9850b38e67a`  
		Last Modified: Sat, 02 Sep 2023 04:39:49 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddac4923b2c94bf9b7a255f5743590ea456c34f78f9a832290a9a5d3ed950e94`  
		Last Modified: Sat, 02 Sep 2023 07:35:07 GMT  
		Size: 25.2 MB (25165336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180ba9db14a1b14c621c6e749bf7d7b0a2145307ffdf843b1610c309670d7b8f`  
		Last Modified: Sat, 02 Sep 2023 07:35:07 GMT  
		Size: 25.1 MB (25137710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f2b263a65c1a0238851e1bdc04bcecc9384b00b3a11597b77db8962221d239`  
		Last Modified: Sat, 02 Sep 2023 07:35:01 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ebc3e6d1768eba0ae571d8467843b621ac3ff098f5b0334621796311378a0f`  
		Last Modified: Sat, 02 Sep 2023 07:35:01 GMT  
		Size: 394.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74150b0870df9850988859a576566d87157eef67341a17140fde35d0a169389`  
		Last Modified: Sat, 02 Sep 2023 07:35:05 GMT  
		Size: 23.3 MB (23273532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c452ec62d62687afe26ebb30235ebd71624bfe13c28b4b9ea191d2166cf4b23`  
		Last Modified: Sat, 02 Sep 2023 07:35:01 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811cb0ea893640c140c9ac6d9f1f2f9a1be02bddc5ad4852b36068bcce14951f`  
		Last Modified: Sat, 02 Sep 2023 07:35:01 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php8.2-fpm` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:da5e1e3d3715743a56ce116f87cdfbac6d7df7ce1c863b60950a4bcb143b31a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244508298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752308e8347b4044d9f4fc3e84f5a7f485afb7a3545313fa2eb4b4052cf50340`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:57 GMT
ADD file:bc58956fa3d1aff2efb0264655d039fedfff28dc4ff19a65a235e82754ee1cfa in / 
# Tue, 15 Aug 2023 23:39:57 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 04:21:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 04:21:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 04:22:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 04:22:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 04:22:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 04:22:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 04:22:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 04:22:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 04:49:38 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 05:18:58 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 05:18:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 05:18:58 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 05:19:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 05:19:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 05:29:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 05:29:23 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 05:29:23 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 05:29:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 05:29:23 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 05:29:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 05:29:24 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 05:29:24 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 05:29:24 GMT
CMD ["php-fpm"]
# Sat, 02 Sep 2023 09:55:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 09:56:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Sat, 02 Sep 2023 09:56:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 02 Sep 2023 09:56:25 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 02 Sep 2023 09:56:28 GMT
RUN set -eux; 	version='6.3.1'; 	sha1='052777aef40e7f627c63c8a26eefe37b843a44df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Sat, 02 Sep 2023 09:56:28 GMT
VOLUME [/var/www/html]
# Sat, 02 Sep 2023 09:56:28 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Sat, 02 Sep 2023 09:56:28 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Sat, 02 Sep 2023 09:56:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Sep 2023 09:56:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4ee097f9a36616fddb52e45aba72142c4bc6f2e594f0a746e406acfde4f02f51`  
		Last Modified: Tue, 15 Aug 2023 23:43:21 GMT  
		Size: 29.2 MB (29157256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cbea39f63906a97f303179be046ab209476a01863e9bdec86af8f323302906`  
		Last Modified: Wed, 16 Aug 2023 06:26:06 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e255c1ce22a7316f5c3b6a28b2b1eafc749afbe18efadf8f72a871a2136b5a6f`  
		Last Modified: Wed, 16 Aug 2023 06:26:16 GMT  
		Size: 98.1 MB (98111384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd06eedb7624b234e9cc7f3e03a7b1878d16c13b439a1bf49317c8a4771fa18e`  
		Last Modified: Wed, 16 Aug 2023 06:26:06 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8575105243dd82ca52359a912633d7d2373517d2ab0c699f179887702231bae4`  
		Last Modified: Sat, 02 Sep 2023 07:13:04 GMT  
		Size: 12.4 MB (12354457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc37097238b963a13d2fbdcb266255469ecc27485e456aa3947c7b4904b0de3`  
		Last Modified: Sat, 02 Sep 2023 07:12:59 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db486b1efd2e8c9fa5933d536a0fddfe52dab524c582d1ab0035579a2118fe2`  
		Last Modified: Sat, 02 Sep 2023 07:14:09 GMT  
		Size: 27.8 MB (27757795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a773e4b92be855036e7c83e835dd2e242726fd406cee9d8d9f369810d0ab2914`  
		Last Modified: Sat, 02 Sep 2023 07:14:06 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946ef57bdcbc49305937cad73633a66ce5bad9b1a6fe7170612a546ab9d8382d`  
		Last Modified: Sat, 02 Sep 2023 07:14:06 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d63a2b717fd62fc2b670c507babf50897b17b979e74b77178c4e7bbbb54fa02a`  
		Last Modified: Sat, 02 Sep 2023 07:14:06 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e542e7fc765ba7f7a86f40f2306ddb459aa4e2417c2ff58a55bd2cb324b3b216`  
		Last Modified: Sat, 02 Sep 2023 10:01:54 GMT  
		Size: 26.3 MB (26288829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4871d9b5edc80f1517a5903f0e36833310aa3d93501d64358f9c163517997a`  
		Last Modified: Sat, 02 Sep 2023 10:01:54 GMT  
		Size: 27.5 MB (27547339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:157db399fa00e447f90e2b347612dcbdfb63d0b601a3dc5c86eb81469a2b0279`  
		Last Modified: Sat, 02 Sep 2023 10:01:49 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce949b69ac76d286a994b43d99c1ec705c66ff4a5730b892087cf08490fec2ea`  
		Last Modified: Sat, 02 Sep 2023 10:01:49 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:587134b96ee57495cf8ed1efc3ca284f75d4b200ee44750557700f174b20e701`  
		Last Modified: Sat, 02 Sep 2023 10:01:52 GMT  
		Size: 23.3 MB (23273533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:595fb869937f2971f7fcb6c94770c8e028cd124b03dbedd46cd338db13f509b9`  
		Last Modified: Sat, 02 Sep 2023 10:01:49 GMT  
		Size: 2.3 KB (2348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d52bd78f86787f84526bba0d4d0a67bb170effc46827561056fe9c1512748e`  
		Last Modified: Sat, 02 Sep 2023 10:01:49 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php8.2-fpm` - linux; 386

```console
$ docker pull wordpress@sha256:b164184186067c065ea0ac575ca0332cd73c209855f7ad5fdb7beb496ce69d3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.7 MB (251714640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a3d1d1c39ab4d290856f80c4f594390d9b2c33fe5ce2f2cabc132c179d35761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Aug 2023 23:39:01 GMT
ADD file:ffdb2f26091492ac2e82793b461bb70da9ce1d68d219ec0db182b4510e82586b in / 
# Tue, 15 Aug 2023 23:39:01 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 03:44:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 03:44:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 03:44:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 03:44:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 03:44:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 03:44:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 03:44:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 03:44:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 04:32:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 03:27:37 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 03:27:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 03:27:37 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 03:27:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 03:27:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 03:48:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 03:48:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 03:48:18 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 03:48:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 03:48:18 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 03:48:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 03:48:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 03:48:19 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 03:48:19 GMT
CMD ["php-fpm"]
# Sat, 02 Sep 2023 10:39:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 10:41:46 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Sat, 02 Sep 2023 10:41:47 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 02 Sep 2023 10:41:47 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 02 Sep 2023 10:41:52 GMT
RUN set -eux; 	version='6.3.1'; 	sha1='052777aef40e7f627c63c8a26eefe37b843a44df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Sat, 02 Sep 2023 10:41:52 GMT
VOLUME [/var/www/html]
# Sat, 02 Sep 2023 10:41:52 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Sat, 02 Sep 2023 10:41:52 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Sat, 02 Sep 2023 10:41:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Sep 2023 10:41:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a12cc43de7614ac71c57865601eb4cedd27ce910b66c5091e07781b8547d5b0b`  
		Last Modified: Tue, 15 Aug 2023 23:43:26 GMT  
		Size: 30.1 MB (30141823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb61ec40f5db69c213102749fea3915c3ce93b2064e3bf6a045e986dfe20a7bc`  
		Last Modified: Wed, 16 Aug 2023 07:31:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d167e851ee2ef31308f9f4ecfc454e5bea793866222cc2afc69c7b0bf37809c`  
		Last Modified: Wed, 16 Aug 2023 07:32:03 GMT  
		Size: 101.5 MB (101506138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e90fee09e6b0af369884a2562788ef1f96299e6e1325a3e892f38b5590f398`  
		Last Modified: Wed, 16 Aug 2023 07:31:39 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355eb07320612cc643ae3f1a0afeeb4822e821ca31c0e99bee85fc172808d44e`  
		Last Modified: Sat, 02 Sep 2023 07:00:35 GMT  
		Size: 12.4 MB (12353891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43f850f2834112335b624c5eedda7ed02691167fae58b72c318853aeac93a75`  
		Last Modified: Sat, 02 Sep 2023 07:00:34 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb819e9e561a1c51a1fb66fae69505a0adbf85512df0651a31c564369ffded46`  
		Last Modified: Sat, 02 Sep 2023 07:01:56 GMT  
		Size: 28.3 MB (28323141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860d66cefe99bf22dc1be903ed383f8515458078906e05ba2b1c3072c8f91dff`  
		Last Modified: Sat, 02 Sep 2023 07:01:50 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a200a61a29016fcf97774dccd2f60c281169cb4903887d3f4a22f644e1fc3bf`  
		Last Modified: Sat, 02 Sep 2023 07:01:50 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3822edde06773f63c1e438bc8f1336881577fa8ec86ee7eae8713f0023abeb80`  
		Last Modified: Sat, 02 Sep 2023 07:01:50 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b8d821b8228bd7f1fbe191045d659904ea7556169b6ed744dc441a78d34cd1`  
		Last Modified: Sat, 02 Sep 2023 10:49:58 GMT  
		Size: 26.8 MB (26829774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e420cbe846acbd9194e6f752a09aa6c8dcfe621bcd18a9deec1c805e39bcfbca`  
		Last Modified: Sat, 02 Sep 2023 10:49:59 GMT  
		Size: 29.3 MB (29268630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8101a2e841cc14c5c0796dfb459b663524840a7aa63f3668e31624b199caea`  
		Last Modified: Sat, 02 Sep 2023 10:49:48 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50c0a22e13f785750d11915e00c47da07fb4b761ccf341c814a9ce74aa68669b`  
		Last Modified: Sat, 02 Sep 2023 10:49:48 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776c1d06dacede09d51d57e5e84f100efe83c17bfda19e931470ac0ca30922b5`  
		Last Modified: Sat, 02 Sep 2023 10:49:54 GMT  
		Size: 23.3 MB (23273535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57788d57937d80ffdcf956d48fb8bfb905a765aee3303540d1126a206f649fb`  
		Last Modified: Sat, 02 Sep 2023 10:49:48 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5cc4579e3cf682a37f699a0d00bf379e491ce291f1b18b7a2974c0f1844df6`  
		Last Modified: Sat, 02 Sep 2023 10:49:48 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php8.2-fpm` - linux; mips64le

```console
$ docker pull wordpress@sha256:96f02baa58a651215cd432e776eb2c7a1d1d95735b44a219f741492231485b9e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225133767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efcc8b48414516be972319adba57b4f1462c9cad2f0c65ebef613e32067532eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 16 Aug 2023 00:08:43 GMT
ADD file:6122efd66f4e010b48e48eeb243d900439ef783f5a10df76043546a288d35d38 in / 
# Wed, 16 Aug 2023 00:08:47 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 00:47:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 00:47:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 00:49:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 00:49:36 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 00:49:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 00:49:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 00:49:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 00:49:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 02:58:21 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 04:43:50 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 04:43:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 04:43:56 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 04:44:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 04:44:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 05:30:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 05:30:26 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 05:30:32 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 05:30:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 05:30:38 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 05:30:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 05:30:47 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 05:30:50 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 05:30:53 GMT
CMD ["php-fpm"]
# Sat, 02 Sep 2023 13:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 13:35:10 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Sat, 02 Sep 2023 13:35:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 02 Sep 2023 13:35:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 02 Sep 2023 13:35:43 GMT
RUN set -eux; 	version='6.3.1'; 	sha1='052777aef40e7f627c63c8a26eefe37b843a44df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Sat, 02 Sep 2023 13:35:48 GMT
VOLUME [/var/www/html]
# Sat, 02 Sep 2023 13:35:52 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Sat, 02 Sep 2023 13:35:56 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Sat, 02 Sep 2023 13:36:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Sep 2023 13:36:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:52390931db742e6fb36945aff79b92fea76dcfe0964f8a5cf7e5b5faaa40b80f`  
		Last Modified: Wed, 16 Aug 2023 00:19:34 GMT  
		Size: 29.1 MB (29121481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3862b29f341bbf3da16b944e02f2d0961e69940ccb034fb905880cf79c6a11`  
		Last Modified: Wed, 16 Aug 2023 10:01:54 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a7f5b8a93b3d93f636840f197a35dfeac134e5a661b80cd59b7221b3212371`  
		Last Modified: Wed, 16 Aug 2023 10:02:49 GMT  
		Size: 80.7 MB (80670713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8baacd58ebb9b6781c5a69d6fde75aa2193e3ffe207f9e0f9ded1d5f75cfdb9`  
		Last Modified: Wed, 16 Aug 2023 10:01:54 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4b8fe24835a535649a4e8a6dbf416e6d5aef00478f56f34e84a223b39ce606`  
		Last Modified: Sat, 02 Sep 2023 08:47:02 GMT  
		Size: 12.1 MB (12148565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fcae029ff8aec52db5a1576add991043e41c85cebd159488cd8aff26a801a4`  
		Last Modified: Sat, 02 Sep 2023 08:46:59 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeb3ed2a8285d4341194c873256a128c7bfe5b8b07a7d8b582f7b8f9db9dc28c`  
		Last Modified: Sat, 02 Sep 2023 08:49:02 GMT  
		Size: 26.7 MB (26691449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c35db9887180a78530d6aab1a8bb3021d6754758b38332d61c0b78b04eec0b5`  
		Last Modified: Sat, 02 Sep 2023 08:48:46 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbd635b1656f2f377308a0f301ed7750024e918dba822b20385088ce5afc7b3`  
		Last Modified: Sat, 02 Sep 2023 08:48:46 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2a2af811e00a74bde79b74c8d5dddeb1103d89166415b240a9ff8a9c3b6cca`  
		Last Modified: Sat, 02 Sep 2023 08:48:46 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0045223b9e82aed46a2d95bb7bd299268f14333b5420e98bbec28c63f2bb9884`  
		Last Modified: Sat, 02 Sep 2023 13:39:39 GMT  
		Size: 26.2 MB (26151784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c447aac33f365020ac325d8fd49ba186f9decd5c1b325422600ca013f9f38fd`  
		Last Modified: Sat, 02 Sep 2023 13:39:42 GMT  
		Size: 27.1 MB (27058413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9339bfc438a71f79446623b806a23a423496250fe9a1dc2a6759e0f0e0e683c`  
		Last Modified: Sat, 02 Sep 2023 13:39:18 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ee1db645b374719a53c4aec45eb8a72b2b422326bff87d8cef12e723ca5ee8`  
		Last Modified: Sat, 02 Sep 2023 13:39:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0cd8e8569a94a5e9a65cde65de82b634404c6c4af14fe98d3efb0495d7a7387`  
		Last Modified: Sat, 02 Sep 2023 13:39:34 GMT  
		Size: 23.3 MB (23273682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2129d44c4f49a2eebe1b0b85edd6a11f96397333a6a63437ee58fcfa6f5e14`  
		Last Modified: Sat, 02 Sep 2023 13:39:18 GMT  
		Size: 2.3 KB (2348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5d2b8ea5e7acb78370a4828e36a0f811e6e6580db54791f6e3ab361d250847`  
		Last Modified: Sat, 02 Sep 2023 13:39:18 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php8.2-fpm` - linux; ppc64le

```console
$ docker pull wordpress@sha256:08edce354f11022c7e9d479550769eb5757fcbbf33bc8e27e278bff290127f0e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.3 MB (258346317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de407dc99db7e3a4c468e1040f0eaf5b234bfd15daad5224d0707c30f22b992a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 16 Aug 2023 01:09:33 GMT
ADD file:9578bf6d6b33f2ba960ab9309642d1c9dcc131d7b9e6f818b8cc4b843fe3aec8 in / 
# Wed, 16 Aug 2023 01:09:35 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 05:28:43 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 05:28:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 05:29:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 05:29:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 05:29:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 05:29:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 05:29:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 05:29:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 06:12:01 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 06:24:11 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 06:24:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 06:24:13 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 06:24:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 06:24:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 06:42:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 06:42:07 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 06:42:11 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 06:42:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 06:42:17 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 06:42:21 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 06:42:23 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 06:42:23 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 06:42:24 GMT
CMD ["php-fpm"]
# Sat, 02 Sep 2023 14:01:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 14:04:06 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Sat, 02 Sep 2023 14:04:09 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 02 Sep 2023 14:04:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 02 Sep 2023 14:04:15 GMT
RUN set -eux; 	version='6.3.1'; 	sha1='052777aef40e7f627c63c8a26eefe37b843a44df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Sat, 02 Sep 2023 14:04:17 GMT
VOLUME [/var/www/html]
# Sat, 02 Sep 2023 14:04:17 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Sat, 02 Sep 2023 14:04:18 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Sat, 02 Sep 2023 14:04:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Sep 2023 14:04:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0500920b409f06d69819525676ebf090702285435050f7b1f973c8c7b034ea7c`  
		Last Modified: Wed, 16 Aug 2023 01:15:59 GMT  
		Size: 33.1 MB (33119300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2e6e5406b2dccdbf8965fa25b50cc70411a95216b41467e2ede0212a0e7f08`  
		Last Modified: Wed, 16 Aug 2023 08:58:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80755cdde4fd6e8e28d68655d3521ec5e67290dfee7272cd3acd0dcc17b068de`  
		Last Modified: Wed, 16 Aug 2023 08:58:43 GMT  
		Size: 103.3 MB (103305694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0254a184608d86c91650e63d986034b42c934a37347cb3805b628077221bd4d`  
		Last Modified: Wed, 16 Aug 2023 08:58:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61ffcb478d8e14545a7ab8fac8b88ce080955ff87db7735dfecaf1cd684efe3`  
		Last Modified: Sat, 02 Sep 2023 09:19:49 GMT  
		Size: 12.4 MB (12354227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9383f661c14459b39b00ac3043c766a45de2bbbc1852a10974cb7efcc30859`  
		Last Modified: Sat, 02 Sep 2023 09:19:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee4eb357827296ce1d82b8dd767a8f6e8382ce206abb61f102f044add5db206`  
		Last Modified: Sat, 02 Sep 2023 09:21:44 GMT  
		Size: 28.9 MB (28862068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db04cb6a9b8bdbc023a4a9dfae2fecebdb6a77e8e0041046a64a074ec2fff351`  
		Last Modified: Sat, 02 Sep 2023 09:21:36 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea508d3812d781d35449f21c151eb1596efcc3a93ab6d4cfe132b726599450cf`  
		Last Modified: Sat, 02 Sep 2023 09:21:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f59cb27d108ba3998e47aa2106239e904886eed35a69595095e0e117dc2a93b`  
		Last Modified: Sat, 02 Sep 2023 09:21:36 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5e08bc8d1327b6936289bb58c21d0151ca2fa6a42e252ac339082cf70e3c83f`  
		Last Modified: Sat, 02 Sep 2023 14:15:39 GMT  
		Size: 27.5 MB (27477424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:747814d2229a18830132ad72907a98a1f7a16a31e486eb1716e1e36e0662c430`  
		Last Modified: Sat, 02 Sep 2023 14:15:41 GMT  
		Size: 29.9 MB (29936353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:353f865794c2a4025624b63943398f05201a03dbab3086aa8124fa4772f23240`  
		Last Modified: Sat, 02 Sep 2023 14:15:30 GMT  
		Size: 366.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f90e57af8f040394f48e499cc8bafe5f4d1737e95826728cd4c6ca3512fb99be`  
		Last Modified: Sat, 02 Sep 2023 14:15:30 GMT  
		Size: 395.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841a749b0e01bd5f365d1f3ac26553fbe991a099da81ab7d9559e238714227cc`  
		Last Modified: Sat, 02 Sep 2023 14:15:36 GMT  
		Size: 23.3 MB (23273533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08865c63266d381475fb54058c29665531a832ebddb7b82808dfa4589c1d208c`  
		Last Modified: Sat, 02 Sep 2023 14:15:30 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3157b8bc1c538873c65f4ee6c04506a8b4f0ac8aafe48ee50b5931812913b6`  
		Last Modified: Sat, 02 Sep 2023 14:15:30 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:php8.2-fpm` - linux; s390x

```console
$ docker pull wordpress@sha256:125bb86f03a9dabae4a2b15916007c69c237ffd78d45adbe13483b001e2d67b2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223356888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba44f5acf59aad26546f6bd57ea8f7c10d20ac5baf61d534669309bfcb4190d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 15 Aug 2023 23:42:31 GMT
ADD file:53543c10022986b61ebedef43821a8984443468fb85c225a6fa19c8d6c76f642 in / 
# Tue, 15 Aug 2023 23:42:34 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 07:30:18 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 16 Aug 2023 07:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 16 Aug 2023 07:30:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 16 Aug 2023 07:30:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Aug 2023 07:30:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 16 Aug 2023 07:30:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 07:30:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Aug 2023 07:30:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Aug 2023 07:52:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 02 Sep 2023 02:56:12 GMT
ENV PHP_VERSION=8.2.10
# Sat, 02 Sep 2023 02:56:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.10.tar.xz.asc
# Sat, 02 Sep 2023 02:56:13 GMT
ENV PHP_SHA256=561dc4acd5386e47f25be76f2c8df6ae854756469159248313bcf276e282fbb3
# Sat, 02 Sep 2023 02:56:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 02 Sep 2023 02:56:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 02 Sep 2023 03:04:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 02 Sep 2023 03:04:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 02 Sep 2023 03:04:18 GMT
RUN docker-php-ext-enable sodium
# Sat, 02 Sep 2023 03:04:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 02 Sep 2023 03:04:18 GMT
WORKDIR /var/www/html
# Sat, 02 Sep 2023 03:04:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 02 Sep 2023 03:04:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 02 Sep 2023 03:04:19 GMT
EXPOSE 9000
# Sat, 02 Sep 2023 03:04:19 GMT
CMD ["php-fpm"]
# Sat, 02 Sep 2023 06:57:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ghostscript 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 02 Sep 2023 06:58:55 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libicu-dev 		libjpeg-dev 		libmagickwand-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$extDir"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Sat, 02 Sep 2023 06:58:57 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 02 Sep 2023 06:58:58 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 02 Sep 2023 06:59:02 GMT
RUN set -eux; 	version='6.3.1'; 	sha1='052777aef40e7f627c63c8a26eefe37b843a44df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Sat, 02 Sep 2023 06:59:04 GMT
VOLUME [/var/www/html]
# Sat, 02 Sep 2023 06:59:04 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Sat, 02 Sep 2023 06:59:04 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Sat, 02 Sep 2023 06:59:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 02 Sep 2023 06:59:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e165c0f9e8f698888061cd00c559fc4e4751505fa2e647bfbf5b2ff0dadafbd2`  
		Last Modified: Tue, 15 Aug 2023 23:47:53 GMT  
		Size: 27.5 MB (27489761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e30d834caf2222467a93c5d22e9493c707e2425a7435eeb8657e1709895060`  
		Last Modified: Wed, 16 Aug 2023 09:10:44 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ad83262d187e94f990c751c94c41771b823f0fb0b3e991f229d2514ddab5a4`  
		Last Modified: Wed, 16 Aug 2023 09:10:55 GMT  
		Size: 80.8 MB (80803885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cc457ca056620bcf6317223056b768b7c0137e6603db8b0341ae10f2bba5fe`  
		Last Modified: Wed, 16 Aug 2023 09:10:43 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b891bbfea8ff90ab36bd6db3f3c6c8d0f4d8a89515274b7f7a8fc94c08baebbe`  
		Last Modified: Sat, 02 Sep 2023 04:28:26 GMT  
		Size: 12.4 MB (12353314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58bbcd13f0c38b363deba5cbae9eaf71987a0200781595fd796186c4d9b924e`  
		Last Modified: Sat, 02 Sep 2023 04:28:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c27256b76b60d88f76bd8fd497f972bda99d6e6a4f945ab83fb01fd760c8a4`  
		Last Modified: Sat, 02 Sep 2023 04:29:07 GMT  
		Size: 26.7 MB (26731213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa36b80dad95c1c771e190b83c5c26b10e1909eb8395c8745fabaf7c2c22cb92`  
		Last Modified: Sat, 02 Sep 2023 04:29:03 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f11b566d3b61f964b0055ed3acb7d7ac826fd9b544e3822c6cebd9adc609ba7`  
		Last Modified: Sat, 02 Sep 2023 04:29:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d818f183dc677ccbe9873e4d8a76e86588cf1f6c29c26600b54a4391a7d2106`  
		Last Modified: Sat, 02 Sep 2023 04:29:03 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3ca268ac7479d572d3b0eb278b65d63e3a0c5cd0858668d8735883deb003c7c`  
		Last Modified: Sat, 02 Sep 2023 07:04:43 GMT  
		Size: 26.0 MB (26014133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80dcc2d99f604dc4299fdafdc89490c59f80deecf87d5c052a8d2311a0e6476`  
		Last Modified: Sat, 02 Sep 2023 07:04:44 GMT  
		Size: 26.7 MB (26673326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:887617f456e328f8f1ee236c6502d4691f0a36a76345b00890a66576d4d49c46`  
		Last Modified: Sat, 02 Sep 2023 07:04:38 GMT  
		Size: 365.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f4da94995a241054eee561b932a3cea5cc73162ec834bbb6e6272e3d1f2fe2`  
		Last Modified: Sat, 02 Sep 2023 07:04:38 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3833ff448887221f20254d5b5ed56b1072ae28adcc520b528e4ee355c8537a95`  
		Last Modified: Sat, 02 Sep 2023 07:04:41 GMT  
		Size: 23.3 MB (23273542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da42af97f90f598037f630812c87f6abe84ed06128ec8354c30fc65f04924d14`  
		Last Modified: Sat, 02 Sep 2023 07:04:39 GMT  
		Size: 2.3 KB (2348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db7e4b6f48e2ae7e9a84d7f8864a264a07b5def2ec90fcde17b1f0c104e4eab`  
		Last Modified: Sat, 02 Sep 2023 07:04:39 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
