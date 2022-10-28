## `joomla:php8.1-fpm-alpine`

```console
$ docker pull joomla@sha256:038b784b221970e883276ba82c91bf0b4d1f92f1a471ea80837657e15e3d4f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `joomla:php8.1-fpm-alpine` - linux; amd64

```console
$ docker pull joomla@sha256:63a81ebdb36058c5a19319c9154bf78fc8748814124cc3ecafffe44a5ed1824a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.8 MB (106828535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:927eda568fae4e77001a4c055d031281da3abbc7e1151c41820ff4a8f932cea2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:21:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 06 Oct 2022 23:21:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 06 Oct 2022 23:21:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 06 Oct 2022 23:21:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Oct 2022 23:21:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 06 Oct 2022 23:21:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Oct 2022 23:21:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Oct 2022 23:21:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Oct 2022 23:46:47 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 06 Oct 2022 23:46:47 GMT
ENV PHP_VERSION=8.1.11
# Thu, 06 Oct 2022 23:46:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Thu, 06 Oct 2022 23:46:47 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Thu, 06 Oct 2022 23:46:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Oct 2022 23:46:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Oct 2022 23:54:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Oct 2022 23:54:53 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Oct 2022 23:54:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Oct 2022 23:54:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Oct 2022 23:54:54 GMT
WORKDIR /var/www/html
# Thu, 06 Oct 2022 23:54:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 06 Oct 2022 23:54:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 23:54:55 GMT
EXPOSE 9000
# Thu, 06 Oct 2022 23:54:55 GMT
CMD ["php-fpm"]
# Fri, 07 Oct 2022 07:46:43 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 07 Oct 2022 07:46:43 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 07 Oct 2022 07:46:49 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Fri, 07 Oct 2022 07:48:53 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.21; 	pecl install memcached-3.2.0; 	pecl install redis-5.3.7; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 07 Oct 2022 07:48:54 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 07 Oct 2022 07:48:54 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 07 Oct 2022 07:48:54 GMT
VOLUME [/var/www/html]
# Thu, 27 Oct 2022 00:24:55 GMT
ENV JOOMLA_VERSION=4.2.3
# Thu, 27 Oct 2022 00:24:55 GMT
ENV JOOMLA_SHA512=8d24be3f0f1dd616d4ddc84ace89f7944b23bb32037a198b5c04c1f9e39c59a4496c760b5dd71bafe5b081799be630f2a905b11093760a9eb183e8f62db6d0bb
# Thu, 27 Oct 2022 00:25:03 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.2.3/Joomla_4.2.3-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 27 Oct 2022 00:25:03 GMT
COPY file:0606560d4086c1b747df5afb8b84de5e317d50368eb37b8af3407cb091e8cae8 in /entrypoint.sh 
# Thu, 27 Oct 2022 00:25:04 GMT
COPY file:1462a25aec948bc277b1371aaf3aa304bc9427dd018b0df243093decbe0bcba6 in /makedb.php 
# Thu, 27 Oct 2022 00:25:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 00:25:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e3d893f0c48a66489b58937fa04412ed69f5d5fac3caf0cfad1fbfcf1d76f1a`  
		Last Modified: Fri, 07 Oct 2022 01:00:52 GMT  
		Size: 1.7 MB (1721106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e145bee0134d72cb2154c552a09f6ad3aff2f689dbc21569a41a22fa106707f`  
		Last Modified: Fri, 07 Oct 2022 01:00:52 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b06443bf3c2fd550395a4f14db54c869b35981ee29ab7da6bdab3816b1f3c8b`  
		Last Modified: Fri, 07 Oct 2022 01:00:52 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcf781e0f6d7adea0198fcebbc006b6a88700c2e517948fda52ef455df3d0a34`  
		Last Modified: Fri, 07 Oct 2022 01:03:09 GMT  
		Size: 11.8 MB (11817545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c453a30d82112a9ce2576aa8e48a3b8e879eed9e844fe7d6e3bff8eebe75c77`  
		Last Modified: Fri, 07 Oct 2022 01:03:08 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0e29aee4ac62f19826b64bc24ba58cc3a500e64e9fb9ddad8a54a177ff5704`  
		Last Modified: Fri, 07 Oct 2022 01:04:01 GMT  
		Size: 12.4 MB (12381995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62ac613ab8c6cd61ba9698b09320b6d111b05fa2dc2df77a00078581023c0a9`  
		Last Modified: Fri, 07 Oct 2022 01:03:58 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc3193aaec386c51eb6c78b33624b37974a23edfb15469dd8369811b18933ab`  
		Last Modified: Fri, 07 Oct 2022 01:03:58 GMT  
		Size: 18.8 KB (18839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde810c8ad2f091a5bfe72a73997470586609ef2c8524b415beb917011fde2a7`  
		Last Modified: Fri, 07 Oct 2022 01:03:58 GMT  
		Size: 8.6 KB (8621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74db6f6b55338128d115edc47259390d4204819d90c9dda528b3105f20d9b66`  
		Last Modified: Fri, 07 Oct 2022 07:53:42 GMT  
		Size: 47.7 MB (47660584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7409a4ad104afae5043aa28e68fcb9c48fdf7fbcc78e101286b8c952399df421`  
		Last Modified: Fri, 07 Oct 2022 07:53:36 GMT  
		Size: 6.6 MB (6573987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fb32d03dbf8f45dd46bb8732fb36bb242d144ca5383ade03602d2c51bfc60c`  
		Last Modified: Fri, 07 Oct 2022 07:53:32 GMT  
		Size: 67.3 KB (67286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333febdbcbab41afdf6a429aefe53b5ddca9f0e1d718c25e9c76a9e8d0f3c300`  
		Last Modified: Fri, 07 Oct 2022 07:53:32 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932ac8b03ccb1641deee9025fd356ee53f50f5a4a156d0f1adf077f61b06a7d3`  
		Last Modified: Thu, 27 Oct 2022 00:29:52 GMT  
		Size: 23.8 MB (23765106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a572990491779044f1de35eb2008af5989eeb8c1aa350675e8c9fff90e3e5ef0`  
		Last Modified: Thu, 27 Oct 2022 00:29:48 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b127c35c3be2c164c124e6e598c2c63b856086010822f63e926679b7c714de4`  
		Last Modified: Thu, 27 Oct 2022 00:29:48 GMT  
		Size: 726.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull joomla@sha256:c706e643fecc4764eedaf49b7c3b84edf3cd46c0e08d361de58d839d3ac9ca98
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100746138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:887feed84810233af667d0c50f9c00548abac5c5f2aa17754ad80c9ea6b48977`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:22 GMT
ADD file:e8733e8cc0a81e15ca4041760b6e27392c34171512d34405a9b262b1fff5c687 in / 
# Tue, 09 Aug 2022 17:49:22 GMT
CMD ["/bin/sh"]
# Thu, 27 Oct 2022 21:51:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 27 Oct 2022 21:51:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 27 Oct 2022 21:51:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 27 Oct 2022 21:51:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 27 Oct 2022 21:51:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 27 Oct 2022 21:51:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 27 Oct 2022 21:51:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 27 Oct 2022 21:51:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 27 Oct 2022 22:21:10 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 27 Oct 2022 22:48:35 GMT
ENV PHP_VERSION=8.1.11
# Thu, 27 Oct 2022 22:48:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Thu, 27 Oct 2022 22:48:35 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Thu, 27 Oct 2022 22:48:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 27 Oct 2022 22:48:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 27 Oct 2022 22:57:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 27 Oct 2022 22:57:55 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 27 Oct 2022 22:57:56 GMT
RUN docker-php-ext-enable sodium
# Thu, 27 Oct 2022 22:57:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 27 Oct 2022 22:57:56 GMT
WORKDIR /var/www/html
# Thu, 27 Oct 2022 22:57:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 27 Oct 2022 22:57:58 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 Oct 2022 22:57:58 GMT
EXPOSE 9000
# Thu, 27 Oct 2022 22:57:58 GMT
CMD ["php-fpm"]
# Fri, 28 Oct 2022 01:56:40 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 28 Oct 2022 01:56:40 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 28 Oct 2022 01:56:48 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Fri, 28 Oct 2022 01:59:18 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.21; 	pecl install memcached-3.2.0; 	pecl install redis-5.3.7; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 28 Oct 2022 01:59:19 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 28 Oct 2022 01:59:19 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 28 Oct 2022 01:59:19 GMT
VOLUME [/var/www/html]
# Fri, 28 Oct 2022 01:59:19 GMT
ENV JOOMLA_VERSION=4.2.3
# Fri, 28 Oct 2022 01:59:19 GMT
ENV JOOMLA_SHA512=8d24be3f0f1dd616d4ddc84ace89f7944b23bb32037a198b5c04c1f9e39c59a4496c760b5dd71bafe5b081799be630f2a905b11093760a9eb183e8f62db6d0bb
# Fri, 28 Oct 2022 01:59:28 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.2.3/Joomla_4.2.3-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 28 Oct 2022 01:59:28 GMT
COPY file:0606560d4086c1b747df5afb8b84de5e317d50368eb37b8af3407cb091e8cae8 in /entrypoint.sh 
# Fri, 28 Oct 2022 01:59:28 GMT
COPY file:1462a25aec948bc277b1371aaf3aa304bc9427dd018b0df243093decbe0bcba6 in /makedb.php 
# Fri, 28 Oct 2022 01:59:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 28 Oct 2022 01:59:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9506b835437abb4d8ba1683e00c500b8f77e1975e930b356fbb72f2dbdc274d9`  
		Last Modified: Tue, 09 Aug 2022 17:50:33 GMT  
		Size: 2.6 MB (2613965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275df827936e551c66b2058870bc70b8b5a7e1bdce2302001cd1df4447078681`  
		Last Modified: Fri, 28 Oct 2022 00:01:13 GMT  
		Size: 1.7 MB (1707972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d68dc6e1d01e17fb4b45b9f197f4f458b9b2f0eed46217e78280913dcef3b7`  
		Last Modified: Fri, 28 Oct 2022 00:01:13 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6133fbb2c00d6592f9c2b80a7e47cb971c55e91ad01d2ea30359cd4fe65a9130`  
		Last Modified: Fri, 28 Oct 2022 00:01:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be35aac4f631d4c83f0dc1a673652cc1490445b23a338c21fc2c06ad98de057`  
		Last Modified: Fri, 28 Oct 2022 00:05:46 GMT  
		Size: 11.8 MB (11817524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735ce53a6e8a392cc2de2b5b74f7ea9dfa7ea71dda3cd6297e9c8ab310621a94`  
		Last Modified: Fri, 28 Oct 2022 00:05:45 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a43e175c930312ce26c872f90280eba80c7875387a2101b56478b078eb46af`  
		Last Modified: Fri, 28 Oct 2022 00:06:57 GMT  
		Size: 11.2 MB (11244064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cda06d6959190d41c121ad6e37828aa71e168bb262d1baebe8a003e453243a4`  
		Last Modified: Fri, 28 Oct 2022 00:06:54 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0743544665b476c8ddb5c1bed3d43cee5f779c5f2feb7fd0421d14c1094351`  
		Last Modified: Fri, 28 Oct 2022 00:06:54 GMT  
		Size: 18.6 KB (18641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2860a3a5efb8e571afd1a55a9a81455e2dfe09559f9c5732a675208c526ca4c`  
		Last Modified: Fri, 28 Oct 2022 00:06:54 GMT  
		Size: 8.6 KB (8620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c932d3089a5f648fa4f8ec1ec6673163017c97d1dc464a91b02b420cef13551d`  
		Last Modified: Fri, 28 Oct 2022 02:04:16 GMT  
		Size: 43.3 MB (43280684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49192fc8dfda8d7b0750d392896f2454d4f8fa60cbc06be32f4958d3bf9ac6b`  
		Last Modified: Fri, 28 Oct 2022 02:04:09 GMT  
		Size: 6.2 MB (6214767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2838cd3d576397248a98dd0f636b65148ecaa869b5e789c90b594233370025cf`  
		Last Modified: Fri, 28 Oct 2022 02:04:05 GMT  
		Size: 67.4 KB (67365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ffb111b9e8c324c9715fe1487edcf0b3d4919d4041a1f39eeadafe7636a810`  
		Last Modified: Fri, 28 Oct 2022 02:04:05 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a71339f4c198914d21c8104cbbcdb501ddddbbabe6b90d76b2d3225b7fd6fd`  
		Last Modified: Fri, 28 Oct 2022 02:04:11 GMT  
		Size: 23.8 MB (23765186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0271f6e86f5e67044aea89dbc0044e934c5eba55199d7a0290827fd179cc5b6a`  
		Last Modified: Fri, 28 Oct 2022 02:04:05 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d008c87e435d0ec9b4a5f2311d6f1badec146ec41c401fc4e5e5363e31f2fe5`  
		Last Modified: Fri, 28 Oct 2022 02:04:05 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull joomla@sha256:2c97c27538488475c39988213e37fe8d2b1a8f646946b8e809eafea86e05d415
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.4 MB (97441133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c86064f0175f36d0123dd046f8619b4be054ebb8830cd27f183bc68aaab836`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Aug 2022 16:57:44 GMT
ADD file:75521fe16320b193092588f6f31052c85e736965ceb11673de18bd14965a45e6 in / 
# Tue, 09 Aug 2022 16:57:44 GMT
CMD ["/bin/sh"]
# Wed, 26 Oct 2022 00:07:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 26 Oct 2022 00:07:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 26 Oct 2022 00:07:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 26 Oct 2022 00:07:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 26 Oct 2022 00:07:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 26 Oct 2022 00:07:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Oct 2022 00:07:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Oct 2022 00:07:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 26 Oct 2022 00:48:37 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 26 Oct 2022 01:40:07 GMT
ENV PHP_VERSION=8.1.11
# Wed, 26 Oct 2022 01:40:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Wed, 26 Oct 2022 01:40:07 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Wed, 26 Oct 2022 01:40:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 26 Oct 2022 01:40:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 26 Oct 2022 01:48:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 26 Oct 2022 01:48:41 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 26 Oct 2022 01:48:42 GMT
RUN docker-php-ext-enable sodium
# Wed, 26 Oct 2022 01:48:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 26 Oct 2022 01:48:42 GMT
WORKDIR /var/www/html
# Wed, 26 Oct 2022 01:48:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 26 Oct 2022 01:48:43 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 01:48:43 GMT
EXPOSE 9000
# Wed, 26 Oct 2022 01:48:43 GMT
CMD ["php-fpm"]
# Wed, 26 Oct 2022 19:38:12 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 26 Oct 2022 19:38:12 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 26 Oct 2022 19:38:19 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Wed, 26 Oct 2022 19:40:42 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.21; 	pecl install memcached-3.2.0; 	pecl install redis-5.3.7; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Wed, 26 Oct 2022 19:40:43 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 26 Oct 2022 19:40:44 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 26 Oct 2022 19:40:44 GMT
VOLUME [/var/www/html]
# Thu, 27 Oct 2022 10:19:44 GMT
ENV JOOMLA_VERSION=4.2.3
# Thu, 27 Oct 2022 10:19:44 GMT
ENV JOOMLA_SHA512=8d24be3f0f1dd616d4ddc84ace89f7944b23bb32037a198b5c04c1f9e39c59a4496c760b5dd71bafe5b081799be630f2a905b11093760a9eb183e8f62db6d0bb
# Thu, 27 Oct 2022 10:19:52 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.2.3/Joomla_4.2.3-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 27 Oct 2022 10:19:53 GMT
COPY file:0606560d4086c1b747df5afb8b84de5e317d50368eb37b8af3407cb091e8cae8 in /entrypoint.sh 
# Thu, 27 Oct 2022 10:19:53 GMT
COPY file:1462a25aec948bc277b1371aaf3aa304bc9427dd018b0df243093decbe0bcba6 in /makedb.php 
# Thu, 27 Oct 2022 10:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 Oct 2022 10:19:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c6556b3b6858c6fa1e328377cc2c4becdc9cd1bc3e7302aa7299936522cf93ba`  
		Last Modified: Tue, 09 Aug 2022 16:58:55 GMT  
		Size: 2.4 MB (2417065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c5f36e3f5e7b3849855eef16c10014e73d1bef3c120e72adc4843ac42c111e`  
		Last Modified: Wed, 26 Oct 2022 03:39:12 GMT  
		Size: 1.6 MB (1575412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65f20680485eedea08cd4c889c2f3717f1f917b137803c40bed508cdf444f02`  
		Last Modified: Wed, 26 Oct 2022 03:39:12 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746e7d5d1f4c8e27fc4f1d81157f3ea48ced64077baed5385929a5e60462b20a`  
		Last Modified: Wed, 26 Oct 2022 03:39:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198cd1c71bd17f15f35c2bd2aa0ae1a527208950e53dffc964dabf12e44d90ef`  
		Last Modified: Wed, 26 Oct 2022 03:52:04 GMT  
		Size: 11.8 MB (11817507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c0bf8d869575fb4f7561dbea21782ec584c5035fe4285d06b7847834ceb053`  
		Last Modified: Wed, 26 Oct 2022 03:52:02 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb34a6a734e507def98598eaf3565082f44ca0e0536e5049f5f7d5e0fbf24f4`  
		Last Modified: Wed, 26 Oct 2022 03:53:12 GMT  
		Size: 10.6 MB (10556301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3230fff26de8865bd7fedf4154a71745e3f54cf1990b68bc582033b9bc06220`  
		Last Modified: Wed, 26 Oct 2022 03:53:10 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0174c0e1663e235fd54504b9830e5e41136314f7ac0f162c03d93b6e3751b4c`  
		Last Modified: Wed, 26 Oct 2022 03:53:10 GMT  
		Size: 18.6 KB (18616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b224f1fc35fa7c4a3780305560453fd6f8c5b6162e3da0fb076f13ae42af5cd7`  
		Last Modified: Wed, 26 Oct 2022 03:53:10 GMT  
		Size: 8.6 KB (8617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08bdd02b0d9e0c12755a62d4fefc2f65744305ce92f491b375e03f60d638807f`  
		Last Modified: Wed, 26 Oct 2022 19:59:31 GMT  
		Size: 41.2 MB (41248353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56b04bfde200df7a53453aa3fdb90b08ea32e45a279f5e66612c60df76d5e55c`  
		Last Modified: Wed, 26 Oct 2022 19:59:25 GMT  
		Size: 6.0 MB (5959414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560d61106d1891982f60f4706d1e7849421e144cfc62a2d293d0bd92b4e492ad`  
		Last Modified: Wed, 26 Oct 2022 19:59:21 GMT  
		Size: 67.3 KB (67305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a656452105492c89834a38b9ad729d3afef42fd29a25cb3927de27e92bbc71c`  
		Last Modified: Wed, 26 Oct 2022 19:59:21 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a789f5574ba8b0b498512f2ec9f3e05e4d6686b6e1e2538fb0dcaadde37e24`  
		Last Modified: Thu, 27 Oct 2022 10:28:01 GMT  
		Size: 23.8 MB (23765201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3b965d7302e6cabe96cd99e05a16c5aa8cda10fc1844a2201a7683e789669b`  
		Last Modified: Thu, 27 Oct 2022 10:27:54 GMT  
		Size: 1.8 KB (1828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810ff616afa1d4d8eb2d81db0df2eae9dfdb8482c2e908cba43824fe4ae62c6a`  
		Last Modified: Thu, 27 Oct 2022 10:27:54 GMT  
		Size: 727.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:f966b23fb89be906ceb662d172f188aa87289c6da90466425821f3fd7ab23edd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.2 MB (105183153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8bd9bc529298538e9c74a7cce23f5d7e6e9ab6bd8ac45d81af75a1c8fa463f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:41 GMT
ADD file:960fd469d48cf79ba14bbda71f3192074ed860c112e30e0bc92bff3440cb45ab in / 
# Tue, 09 Aug 2022 17:39:42 GMT
CMD ["/bin/sh"]
# Tue, 25 Oct 2022 16:24:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 25 Oct 2022 16:24:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 25 Oct 2022 16:24:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 25 Oct 2022 16:24:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 25 Oct 2022 16:24:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 25 Oct 2022 16:24:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 16:24:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 25 Oct 2022 16:24:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 25 Oct 2022 17:13:15 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 25 Oct 2022 18:02:03 GMT
ENV PHP_VERSION=8.1.11
# Tue, 25 Oct 2022 18:02:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Tue, 25 Oct 2022 18:02:03 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Tue, 25 Oct 2022 18:02:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 25 Oct 2022 18:02:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 25 Oct 2022 18:10:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 25 Oct 2022 18:10:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 25 Oct 2022 18:10:35 GMT
RUN docker-php-ext-enable sodium
# Tue, 25 Oct 2022 18:10:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Oct 2022 18:10:35 GMT
WORKDIR /var/www/html
# Tue, 25 Oct 2022 18:10:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 25 Oct 2022 18:10:36 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Oct 2022 18:10:36 GMT
EXPOSE 9000
# Tue, 25 Oct 2022 18:10:36 GMT
CMD ["php-fpm"]
# Wed, 26 Oct 2022 11:38:30 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 26 Oct 2022 11:38:30 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 26 Oct 2022 11:38:35 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Wed, 26 Oct 2022 11:40:25 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.21; 	pecl install memcached-3.2.0; 	pecl install redis-5.3.7; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Wed, 26 Oct 2022 11:40:26 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 26 Oct 2022 11:40:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 26 Oct 2022 11:40:27 GMT
VOLUME [/var/www/html]
# Wed, 26 Oct 2022 20:52:50 GMT
ENV JOOMLA_VERSION=4.2.3
# Wed, 26 Oct 2022 20:52:50 GMT
ENV JOOMLA_SHA512=8d24be3f0f1dd616d4ddc84ace89f7944b23bb32037a198b5c04c1f9e39c59a4496c760b5dd71bafe5b081799be630f2a905b11093760a9eb183e8f62db6d0bb
# Wed, 26 Oct 2022 20:52:55 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.2.3/Joomla_4.2.3-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 26 Oct 2022 20:52:55 GMT
COPY file:0606560d4086c1b747df5afb8b84de5e317d50368eb37b8af3407cb091e8cae8 in /entrypoint.sh 
# Wed, 26 Oct 2022 20:52:55 GMT
COPY file:1462a25aec948bc277b1371aaf3aa304bc9427dd018b0df243093decbe0bcba6 in /makedb.php 
# Wed, 26 Oct 2022 20:52:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 20:52:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9b18e9b68314027565b90ff6189d65942c0f7986da80df008b8431276885218e`  
		Last Modified: Tue, 09 Aug 2022 17:40:38 GMT  
		Size: 2.7 MB (2707663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c3c1a63608ee746cfd0fb1d310f407f855ea0809df0a8d336fd6e4501ceae2`  
		Last Modified: Tue, 25 Oct 2022 19:41:26 GMT  
		Size: 1.7 MB (1715562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ebdb03735b66ed04ec81a33c9949c64b7ed3437ce31650fea31e9fc0acc293`  
		Last Modified: Tue, 25 Oct 2022 19:41:26 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661297bd570d111eb52d0966fa7e261bea3a4eda3f9fea437202fc7fd169dee7`  
		Last Modified: Tue, 25 Oct 2022 19:41:26 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de63708920c3a83c0284114727d15adfbca2edb8b9f5c045427329545865f27`  
		Last Modified: Tue, 25 Oct 2022 19:51:05 GMT  
		Size: 11.8 MB (11817546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec3b2189064490f7b83ad1dbd3a4f16675dd9903c208ed22dfea83f964eafdb`  
		Last Modified: Tue, 25 Oct 2022 19:51:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d65c93114e11a7f2ca7536908ce792ea2868fc7787f0cbb929716b4bdbb6800`  
		Last Modified: Tue, 25 Oct 2022 19:51:55 GMT  
		Size: 12.4 MB (12434383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a604684263b937a01062fd704353e9e66a0c66e5401780a14b8bdc7043cbfce`  
		Last Modified: Tue, 25 Oct 2022 19:51:53 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ee186f2b982aa9b2598af8b10fa79e9b89ce44aba04af7c2e0ff7df405a29d`  
		Last Modified: Tue, 25 Oct 2022 19:51:53 GMT  
		Size: 18.6 KB (18640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3694361473f3895f05c2ee100ef5643b399e6d12401bd38425622f543b44593`  
		Last Modified: Tue, 25 Oct 2022 19:51:53 GMT  
		Size: 8.6 KB (8620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2586532ab735e46560e7f00127f091202cc6f8c70bef6ab07f6b1c2fd495c156`  
		Last Modified: Wed, 26 Oct 2022 11:53:26 GMT  
		Size: 46.1 MB (46119664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80b416bb17584678c813656e7e54f42a0af8f70e5c74989af1f2adb14727f27`  
		Last Modified: Wed, 26 Oct 2022 11:53:21 GMT  
		Size: 6.5 MB (6521117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a1be4f5de3edcd48e03c6c617fbacfb8e0391670cf4a3d7b0bf856f87b902`  
		Last Modified: Wed, 26 Oct 2022 11:53:18 GMT  
		Size: 67.4 KB (67365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f66501fa82588b75c3829a58bfbe2198cb906e650d028be33f296730296399`  
		Last Modified: Wed, 26 Oct 2022 11:53:18 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70aae052b1fe480d2b1a7e56534de738645f873f982868af0b18b3daba62d747`  
		Last Modified: Wed, 26 Oct 2022 20:57:27 GMT  
		Size: 23.8 MB (23765176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2a80b6637a239d88dc3b8c1ff3b84d8fb9bfab725b6cf4a1c9896a3a0089aa`  
		Last Modified: Wed, 26 Oct 2022 20:57:23 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c82f46069fd61924134264059ee2429d826cbf25fa29d53c89220c9fe181a85`  
		Last Modified: Wed, 26 Oct 2022 20:57:24 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.1-fpm-alpine` - linux; 386

```console
$ docker pull joomla@sha256:55f01674e0f131d7f56fec79ad84eb52e2384aa5c46de55cd6e8dbaeac0ccfad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.0 MB (106013125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1ced4bd6ac75e773d6b774355804b3c8c058fd9144f6b03b06639e3ac0877e1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 21:01:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 06 Oct 2022 21:01:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 06 Oct 2022 21:01:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 06 Oct 2022 21:01:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Oct 2022 21:01:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 06 Oct 2022 21:01:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Oct 2022 21:01:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Oct 2022 21:01:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Oct 2022 21:26:35 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 06 Oct 2022 21:26:36 GMT
ENV PHP_VERSION=8.1.11
# Thu, 06 Oct 2022 21:26:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Thu, 06 Oct 2022 21:26:38 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Thu, 06 Oct 2022 21:26:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Oct 2022 21:26:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Oct 2022 21:34:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Oct 2022 21:34:52 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Oct 2022 21:34:53 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Oct 2022 21:34:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Oct 2022 21:34:54 GMT
WORKDIR /var/www/html
# Thu, 06 Oct 2022 21:34:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 06 Oct 2022 21:34:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 21:34:57 GMT
EXPOSE 9000
# Thu, 06 Oct 2022 21:34:58 GMT
CMD ["php-fpm"]
# Fri, 07 Oct 2022 04:06:02 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 07 Oct 2022 04:06:02 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 07 Oct 2022 04:06:09 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Fri, 07 Oct 2022 04:08:22 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.21; 	pecl install memcached-3.2.0; 	pecl install redis-5.3.7; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 07 Oct 2022 04:08:23 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 07 Oct 2022 04:08:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 07 Oct 2022 04:08:25 GMT
VOLUME [/var/www/html]
# Wed, 26 Oct 2022 20:41:07 GMT
ENV JOOMLA_VERSION=4.2.3
# Wed, 26 Oct 2022 20:41:07 GMT
ENV JOOMLA_SHA512=8d24be3f0f1dd616d4ddc84ace89f7944b23bb32037a198b5c04c1f9e39c59a4496c760b5dd71bafe5b081799be630f2a905b11093760a9eb183e8f62db6d0bb
# Wed, 26 Oct 2022 20:41:16 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.2.3/Joomla_4.2.3-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 26 Oct 2022 20:41:17 GMT
COPY file:0606560d4086c1b747df5afb8b84de5e317d50368eb37b8af3407cb091e8cae8 in /entrypoint.sh 
# Wed, 26 Oct 2022 20:41:18 GMT
COPY file:1462a25aec948bc277b1371aaf3aa304bc9427dd018b0df243093decbe0bcba6 in /makedb.php 
# Wed, 26 Oct 2022 20:41:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 20:41:19 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8429c35581dc2b06177afb14a55afbd6b92a75a15232d3596d5ef954c2b1fcdf`  
		Last Modified: Thu, 06 Oct 2022 22:46:39 GMT  
		Size: 1.8 MB (1820480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c702fb4048195b35060feca6dfae579d104b48448b0d0ddf019c60b1745fd0c`  
		Last Modified: Thu, 06 Oct 2022 22:46:42 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac06596e4ff3720f72e504820e969f1ef3dcf30c54166b940d1022d7f9fdd61`  
		Last Modified: Thu, 06 Oct 2022 22:46:39 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f464351862241fdbe92956c3c784d307681a155b20f95dff7c934c6376130af1`  
		Last Modified: Thu, 06 Oct 2022 22:49:24 GMT  
		Size: 11.8 MB (11817295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76d651407363e006530a07abf28f34d7efe5a037d22c28d7577d417accbb3a4b`  
		Last Modified: Thu, 06 Oct 2022 22:49:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7c15a0ada7af192019dac0527bd394348dc4700861a51fb2f68e5cb6d36494`  
		Last Modified: Thu, 06 Oct 2022 22:50:23 GMT  
		Size: 12.7 MB (12672992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f9e02b9d469bd378bb631553e1d488d7b5a2aab9e1516cbbf1fe4a90f717195`  
		Last Modified: Thu, 06 Oct 2022 22:50:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e5763a419f609b65f0b97dda98c093a9d4549ec71ed1a073544fe0f21ad8d3`  
		Last Modified: Thu, 06 Oct 2022 22:50:21 GMT  
		Size: 18.7 KB (18739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dc2d86ca4a1eba457e7d4cdf2aeb61122c210d8e1d102649fdfaf42e474c0cd`  
		Last Modified: Thu, 06 Oct 2022 22:50:21 GMT  
		Size: 8.6 KB (8622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0971ef03048ed5b747aac3114050fc0f912fcd6c9ecdead6619cc26dac06751`  
		Last Modified: Fri, 07 Oct 2022 04:15:00 GMT  
		Size: 46.2 MB (46249982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93dce57b7393ed115b15d89defc807ef50c58b6ec1bc48a2bcd3b221db121605`  
		Last Modified: Fri, 07 Oct 2022 04:14:56 GMT  
		Size: 6.8 MB (6775401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5d4b1c9602c8c7c97efa5ce436b047712c276e23415766e7750155d446dcf`  
		Last Modified: Fri, 07 Oct 2022 04:14:51 GMT  
		Size: 67.2 KB (67164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf4c74b6f1d49653792ae2cfa5824d4a3074236058bd8f30af821a7aa5a89e9`  
		Last Modified: Fri, 07 Oct 2022 04:14:51 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7001611155e87501d89102147ea97ac5d6351911d0b1b3a2406cf1ce001a41ac`  
		Last Modified: Wed, 26 Oct 2022 20:48:23 GMT  
		Size: 23.8 MB (23767987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ae7740fd140d5d94442f94686a854d6b69793ac06f2c3b0587697c598aa7fd`  
		Last Modified: Wed, 26 Oct 2022 20:48:19 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8800dc0f703a0d20cfffd05dd3860b1ff18df0e0a58ae6f0f275ba993e177a5`  
		Last Modified: Wed, 26 Oct 2022 20:48:19 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.1-fpm-alpine` - linux; ppc64le

```console
$ docker pull joomla@sha256:e37b7bf5502e923a3691465288a7d9164f6514603b01877c982f2584588a3557
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **112.8 MB (112762675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adae9ef537a81f1dad81b5d2ebfd5a1ef459fe6a05f15b3dd979458091666bb8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Aug 2022 17:17:09 GMT
ADD file:66b351666e41834033d334aeb3dc6998dea77aa22e8e254028c923fee67a41a8 in / 
# Tue, 09 Aug 2022 17:17:10 GMT
CMD ["/bin/sh"]
# Thu, 06 Oct 2022 23:59:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 06 Oct 2022 23:59:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 06 Oct 2022 23:59:50 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 06 Oct 2022 23:59:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 06 Oct 2022 23:59:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 06 Oct 2022 23:59:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Oct 2022 23:59:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 06 Oct 2022 23:59:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Oct 2022 00:32:26 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 07 Oct 2022 00:32:26 GMT
ENV PHP_VERSION=8.1.11
# Fri, 07 Oct 2022 00:32:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Fri, 07 Oct 2022 00:32:26 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Fri, 07 Oct 2022 00:32:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 07 Oct 2022 00:32:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 07 Oct 2022 00:42:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 07 Oct 2022 00:42:47 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 07 Oct 2022 00:42:49 GMT
RUN docker-php-ext-enable sodium
# Fri, 07 Oct 2022 00:42:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Oct 2022 00:42:50 GMT
WORKDIR /var/www/html
# Fri, 07 Oct 2022 00:42:53 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 07 Oct 2022 00:42:53 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Oct 2022 00:42:53 GMT
EXPOSE 9000
# Fri, 07 Oct 2022 00:42:54 GMT
CMD ["php-fpm"]
# Fri, 07 Oct 2022 09:58:23 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 07 Oct 2022 09:58:23 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 07 Oct 2022 09:58:36 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Fri, 07 Oct 2022 10:02:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.21; 	pecl install memcached-3.2.0; 	pecl install redis-5.3.7; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 07 Oct 2022 10:02:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 07 Oct 2022 10:02:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 07 Oct 2022 10:02:31 GMT
VOLUME [/var/www/html]
# Wed, 26 Oct 2022 20:19:50 GMT
ENV JOOMLA_VERSION=4.2.3
# Wed, 26 Oct 2022 20:19:50 GMT
ENV JOOMLA_SHA512=8d24be3f0f1dd616d4ddc84ace89f7944b23bb32037a198b5c04c1f9e39c59a4496c760b5dd71bafe5b081799be630f2a905b11093760a9eb183e8f62db6d0bb
# Wed, 26 Oct 2022 20:20:03 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.2.3/Joomla_4.2.3-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 26 Oct 2022 20:20:05 GMT
COPY file:0606560d4086c1b747df5afb8b84de5e317d50368eb37b8af3407cb091e8cae8 in /entrypoint.sh 
# Wed, 26 Oct 2022 20:20:06 GMT
COPY file:1462a25aec948bc277b1371aaf3aa304bc9427dd018b0df243093decbe0bcba6 in /makedb.php 
# Wed, 26 Oct 2022 20:20:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 20:20:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c79e5d1a8c89b87020a754c8a5c8370faaa37bfb5bca1d8af66770d522ef1caf`  
		Last Modified: Tue, 09 Aug 2022 17:18:26 GMT  
		Size: 2.8 MB (2803320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca3a3b32081770d8d84a7e4ab84cdd4d01b5a6350d96ebd161d4e0612d2e4a9`  
		Last Modified: Fri, 07 Oct 2022 02:13:07 GMT  
		Size: 1.8 MB (1772297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2175d7fbb352f035d82bd9705fe1ed1816644aadaefa77a474166470fd00e42b`  
		Last Modified: Fri, 07 Oct 2022 02:13:06 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ddaf49f63dc65bb9290753c44394973fdc7edbd724b1fbe4b8a1c440356cdb`  
		Last Modified: Fri, 07 Oct 2022 02:13:06 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2e22f5709118cb246edb704cbbb16dda1543bf6011b673c2f2d268f78c013d`  
		Last Modified: Fri, 07 Oct 2022 02:15:57 GMT  
		Size: 11.8 MB (11817549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b37db90acb607bd6d022dd5f203d9a1ab2d3e1001b9f4aad0ff79b06986837`  
		Last Modified: Fri, 07 Oct 2022 02:15:56 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f577cf088f0c9dadd89653ef1db26bb10f3369ebcc02a74f14291d1eb0cffaa4`  
		Last Modified: Fri, 07 Oct 2022 02:17:09 GMT  
		Size: 12.8 MB (12815961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04d42f547862477b259888cb5dd4f781c0ef53f99f865ea41370d7f5245d76b`  
		Last Modified: Fri, 07 Oct 2022 02:17:05 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70db646e7020ab16cb5f5155f643675cb4d9f669ec9048e03c53d9008873d560`  
		Last Modified: Fri, 07 Oct 2022 02:17:05 GMT  
		Size: 18.6 KB (18627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9911bac29e1c17f00850b5e425e18aa29937f9cf0d24acdb911a8eaca8c00e26`  
		Last Modified: Fri, 07 Oct 2022 02:17:05 GMT  
		Size: 8.6 KB (8618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ca8d12bb9dc443febf1fbae636254dd4b917cb3b133d9b420b1ca18c911970`  
		Last Modified: Fri, 07 Oct 2022 10:11:34 GMT  
		Size: 52.8 MB (52769515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869a8b6d57adf05df93f8938b1ce77a8fd89580366714497b677fd07beb42b89`  
		Last Modified: Fri, 07 Oct 2022 10:11:24 GMT  
		Size: 6.9 MB (6916954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a500f06b83d250610e0a04994aeda5034be511593dfe526825ded2fa035e182c`  
		Last Modified: Fri, 07 Oct 2022 10:11:18 GMT  
		Size: 67.3 KB (67289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f252b499a34088af09552f33afe792769686ffacdb8d4f43a17233edf38580`  
		Last Modified: Fri, 07 Oct 2022 10:11:18 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2814280b2149b5b44803616899a261a5e9d1529ad842df47cebbec02270e196a`  
		Last Modified: Wed, 26 Oct 2022 20:27:45 GMT  
		Size: 23.8 MB (23765126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:481df85379197cfbb2033fd3bd39f39031bdd91f02d113754a47a9422f0132b7`  
		Last Modified: Wed, 26 Oct 2022 20:27:38 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90d615ab1a73116754c6a60cdc0a61d52770e6886a2b0fe151cd5e02ae8e602`  
		Last Modified: Wed, 26 Oct 2022 20:27:38 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:php8.1-fpm-alpine` - linux; s390x

```console
$ docker pull joomla@sha256:d0a36f37d11c7d46412020af3f01bdb4b3f9dbfd6fdc2be7be17a55cac2f1490
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96208863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b728c3f39fddac759805c958a926f894f9a16c3c99828eca67ece45dae2944be`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Aug 2022 17:41:46 GMT
ADD file:b43a065471bc4711415d3c67cd5b6559b0c48ee7ffe9761530477cf457a6dc34 in / 
# Tue, 09 Aug 2022 17:41:46 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 01:27:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 07 Oct 2022 01:27:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 07 Oct 2022 01:27:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 07 Oct 2022 01:27:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Oct 2022 01:27:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 07 Oct 2022 01:27:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Oct 2022 01:27:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Oct 2022 01:27:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Oct 2022 01:55:40 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 07 Oct 2022 01:55:41 GMT
ENV PHP_VERSION=8.1.11
# Fri, 07 Oct 2022 01:55:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.11.tar.xz.asc
# Fri, 07 Oct 2022 01:55:42 GMT
ENV PHP_SHA256=3005198d7303f87ab31bc30695de76e8ad62783f806b6ab9744da59fe41cc5bd
# Fri, 07 Oct 2022 01:55:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 07 Oct 2022 01:55:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 07 Oct 2022 02:05:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 07 Oct 2022 02:05:32 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 07 Oct 2022 02:05:34 GMT
RUN docker-php-ext-enable sodium
# Fri, 07 Oct 2022 02:05:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Oct 2022 02:05:35 GMT
WORKDIR /var/www/html
# Fri, 07 Oct 2022 02:05:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 07 Oct 2022 02:05:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Oct 2022 02:05:37 GMT
EXPOSE 9000
# Fri, 07 Oct 2022 02:05:37 GMT
CMD ["php-fpm"]
# Fri, 07 Oct 2022 11:58:33 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Fri, 07 Oct 2022 11:58:33 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 07 Oct 2022 11:58:38 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Fri, 07 Oct 2022 12:00:47 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.21; 	pecl install memcached-3.2.0; 	pecl install redis-5.3.7; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Fri, 07 Oct 2022 12:00:49 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 07 Oct 2022 12:00:49 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Fri, 07 Oct 2022 12:00:49 GMT
VOLUME [/var/www/html]
# Wed, 26 Oct 2022 20:45:56 GMT
ENV JOOMLA_VERSION=4.2.3
# Wed, 26 Oct 2022 20:45:56 GMT
ENV JOOMLA_SHA512=8d24be3f0f1dd616d4ddc84ace89f7944b23bb32037a198b5c04c1f9e39c59a4496c760b5dd71bafe5b081799be630f2a905b11093760a9eb183e8f62db6d0bb
# Wed, 26 Oct 2022 20:46:14 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.2.3/Joomla_4.2.3-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Wed, 26 Oct 2022 20:46:19 GMT
COPY file:0606560d4086c1b747df5afb8b84de5e317d50368eb37b8af3407cb091e8cae8 in /entrypoint.sh 
# Wed, 26 Oct 2022 20:46:20 GMT
COPY file:1462a25aec948bc277b1371aaf3aa304bc9427dd018b0df243093decbe0bcba6 in /makedb.php 
# Wed, 26 Oct 2022 20:46:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 26 Oct 2022 20:46:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:790c84f1f3409eab952345157df7fa804ba6b5f06d4ceb6f2dfa3c6de2064397`  
		Last Modified: Tue, 09 Aug 2022 17:42:45 GMT  
		Size: 2.6 MB (2590597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793dde3b687f0aaad5df5bdf75b8def5a75f3e23c18eed049b7f33b63d1d9d4f`  
		Last Modified: Fri, 07 Oct 2022 03:27:12 GMT  
		Size: 1.8 MB (1776077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69b020cae1039f28b7553cbfface89b8dbc71291be52523b4d9a21212a9ec8b`  
		Last Modified: Fri, 07 Oct 2022 03:27:12 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6defbdf58b88d9209932f344cee98a6544b064956c7921f9a570c497be009815`  
		Last Modified: Fri, 07 Oct 2022 03:27:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0496ac5c1344509278f108079bb3c0e978fa37def9dd147c6e81760d9aa872`  
		Last Modified: Fri, 07 Oct 2022 03:29:06 GMT  
		Size: 11.8 MB (11817558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3588dd028d48411d80405f7324a8a312ef2de2ed8e276a2fbb565d17fe68d5`  
		Last Modified: Fri, 07 Oct 2022 03:29:05 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd6ae656c64171da192aec3693c3f4c25eb0118c12727d244a596efce6b6def`  
		Last Modified: Fri, 07 Oct 2022 03:29:48 GMT  
		Size: 11.6 MB (11571544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bad402b56624c79cfc0f89b3de5b3963aa1fcbc0468e045a181419bf6702b2d8`  
		Last Modified: Fri, 07 Oct 2022 03:29:47 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39687415754b7863e80f792999d209fd2f350c7c23545c04b1006b6dd5ecdde3`  
		Last Modified: Fri, 07 Oct 2022 03:29:47 GMT  
		Size: 18.6 KB (18640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d371f3e6bdaef8fe1ee206f734a5335514d93df3e6c72e86f2b46a937ef49e98`  
		Last Modified: Fri, 07 Oct 2022 03:29:47 GMT  
		Size: 8.6 KB (8618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec429b33528109a643bd4d634c636c4f1cabb6e27a90bdeff8d67f3df83232a3`  
		Last Modified: Fri, 07 Oct 2022 12:07:22 GMT  
		Size: 38.0 MB (37986496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa020f6c59847348aed16da963c6c8ca1cfb1bccdf0900d24b45e8528644b7c`  
		Last Modified: Fri, 07 Oct 2022 12:07:18 GMT  
		Size: 6.6 MB (6605519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87cb15fda0311eabdab9fc3a8284a0d7ebe4a0cdda3b73731810fa6eb0d75834`  
		Last Modified: Fri, 07 Oct 2022 12:07:16 GMT  
		Size: 61.3 KB (61270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c69e618ddba5604b4c58e1e5477ba6605140c4438215ee54eccf6f83f7facaa`  
		Last Modified: Fri, 07 Oct 2022 12:07:16 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d58a6be9be251adc1819708301279f0f6c01f3f42a47ba5cf5a2dce6f0a99e3`  
		Last Modified: Wed, 26 Oct 2022 20:52:36 GMT  
		Size: 23.8 MB (23765127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03722dd369484e5f66b373c82d692945d119ba8e3e8b0f28fb3d5768dd6d9d7e`  
		Last Modified: Wed, 26 Oct 2022 20:52:33 GMT  
		Size: 1.8 KB (1827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce310918d49be8611fe2f48270a811860f5615875be6fa6799b1c3923384fadf`  
		Last Modified: Wed, 26 Oct 2022 20:52:33 GMT  
		Size: 725.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
