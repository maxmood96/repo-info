## `friendica:dev-fpm-alpine`

```console
$ docker pull friendica@sha256:9d5971f4f6c9b3a5f40af0b63dc5157c66b3a81a75aefe5171570a82f4759dad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `friendica:dev-fpm-alpine` - linux; amd64

```console
$ docker pull friendica@sha256:334b42557c4e34f0cc3a198f6c1bf3e4fab5f93ea098521f3da6c04507af0097
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51539510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:804d4eae8a5248a0ea3e85ca8157c3acb2afba1e7039b36d092714e9aa9af888`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:30:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:30:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:30:15 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:30:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:30:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:37:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:05:56 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 30 Oct 2020 00:41:04 GMT
ENV PHP_VERSION=7.3.24
# Fri, 30 Oct 2020 00:41:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.24.tar.xz.asc
# Thu, 05 Nov 2020 22:41:56 GMT
ENV PHP_SHA256=78b0b417a147ab7572c874334d11654e3c61ec5b3f2170098e5db02fb0c89888
# Thu, 05 Nov 2020 22:42:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Nov 2020 22:42:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Nov 2020 22:50:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Nov 2020 22:50:49 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Thu, 05 Nov 2020 22:50:52 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Nov 2020 22:50:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Nov 2020 22:50:53 GMT
WORKDIR /var/www/html
# Thu, 05 Nov 2020 22:50:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 05 Nov 2020 22:50:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Nov 2020 22:50:55 GMT
EXPOSE 9000
# Thu, 05 Nov 2020 22:50:55 GMT
CMD ["php-fpm"]
# Fri, 06 Nov 2020 03:08:42 GMT
RUN set -ex;     apk add --no-cache         rsync         git         msmtp         shadow         tini;
# Fri, 06 Nov 2020 03:10:36 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         pcntl         ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.3.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Fri, 06 Nov 2020 03:10:37 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 06 Nov 2020 03:10:37 GMT
VOLUME [/var/www/html]
# Fri, 06 Nov 2020 03:11:10 GMT
ENV FRIENDICA_VERSION=2020.12-dev
# Fri, 06 Nov 2020 03:11:10 GMT
ENV FRIENDICA_ADDONS=2020.12-dev
# Fri, 06 Nov 2020 03:11:11 GMT
COPY multi:79fafe1f110f1d1a4fd44f7b958b2a83de813fc7f8cfcefe662a6fa6e275cf3e in / 
# Fri, 06 Nov 2020 03:11:11 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Fri, 06 Nov 2020 03:11:12 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 06 Nov 2020 03:11:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f8bf6cfdbe614fef94f982905079c16e27b3de2d24eb1ff513d3d83e656ca2`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.3 MB (1340771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5be79740125b9e74a77885bf6ee2b0d25ac7ed9e9432c5aa7210bb3b00458a`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99dd6507fe563b66ba35badf706e1bbb2d39eb5d0a3c0d5a86a45d2af7e89c1`  
		Last Modified: Thu, 22 Oct 2020 07:36:55 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e6ba8c9fb18a5dcb870624c218fd85e7f8ce06c13c10b83d8997a2b4c0cd8f`  
		Last Modified: Fri, 06 Nov 2020 01:33:51 GMT  
		Size: 12.2 MB (12157505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51774d9e804b161fcb054ba38e24b5a55924a51640161088029b0fe6e05fa85`  
		Last Modified: Fri, 06 Nov 2020 01:33:48 GMT  
		Size: 501.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9a4b5dbf5f59fa7eeaae168f29ee9277625c7a4a605c639da1357081ee3ed5`  
		Last Modified: Fri, 06 Nov 2020 01:33:51 GMT  
		Size: 14.5 MB (14461873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b23a9ef43e37fcaaf26af09efb62dd1caa21075c888b7aa2cbb320b41b96367`  
		Last Modified: Fri, 06 Nov 2020 01:33:48 GMT  
		Size: 2.3 KB (2263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ed97dd4f90512484330376c45b34d21e4f1fe6d5a5540db12ae68c9e7a3141`  
		Last Modified: Fri, 06 Nov 2020 01:33:48 GMT  
		Size: 16.7 KB (16710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2d4d0540bae465aed3d568bcdaa85ff509db9c8fc112cb6ba4203d3879f92d8`  
		Last Modified: Fri, 06 Nov 2020 01:33:48 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8530ea7d9de728867a707fa0c903302ab2856c14f147d760b1d1e345961ecc6a`  
		Last Modified: Fri, 06 Nov 2020 03:12:11 GMT  
		Size: 11.4 MB (11380028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a97412216667e001aa33d7472f9af4fe8b1cefe942c9da46949277be864fd8`  
		Last Modified: Fri, 06 Nov 2020 03:12:09 GMT  
		Size: 9.4 MB (9368271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd95b9adcd8e949c0b08e4f687b75caac8d64e185cc9b0f16a0cfd6d4ad51a4a`  
		Last Modified: Fri, 06 Nov 2020 03:12:07 GMT  
		Size: 543.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5efbd9404df9ac710346f05d7c71f787d0c5d3301615be4d7167088049f81ed`  
		Last Modified: Fri, 06 Nov 2020 03:12:36 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758938db82bb8df61664f497a4d72ed703a06217ac342e4e144cb7c73c860c53`  
		Last Modified: Fri, 06 Nov 2020 03:12:36 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:8f4ac74bcb1767cf7b721a96282b4639a8754bfb28c87d8bd48b127435f6d921
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49784850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a18e7815c1f1b586d86872106b6a79b41da49c095773678e449ebdcf73975804`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:09 GMT
ADD file:dec4d3b6cf21c59820d1d74a554d0a193b5f4859e00b932f31ffe73f554d5afb in / 
# Thu, 22 Oct 2020 02:01:12 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:41:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:41:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:42:00 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:42:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:42:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:46:13 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 06:46:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:46:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:46:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:11:06 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 01 Dec 2020 02:27:49 GMT
ENV PHP_VERSION=7.3.25
# Tue, 01 Dec 2020 02:27:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.25.tar.xz.asc
# Tue, 01 Dec 2020 02:27:51 GMT
ENV PHP_SHA256=c71c00ad03079efb78d1a6b8623ca4f725be697dbd9a46debacbcc9a2475f329
# Tue, 01 Dec 2020 02:27:57 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 02:27:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:31:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 02:31:50 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 02:31:52 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 02:31:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 02:31:54 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 02:32:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 02:32:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 02:32:11 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 02:32:12 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 03:26:38 GMT
RUN set -ex;     apk add --no-cache         rsync         git         msmtp         shadow         tini;
# Tue, 01 Dec 2020 03:29:48 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         pcntl         ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.3.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Tue, 01 Dec 2020 03:29:52 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 01 Dec 2020 03:29:53 GMT
VOLUME [/var/www/html]
# Tue, 01 Dec 2020 03:30:39 GMT
ENV FRIENDICA_VERSION=2020.12-dev
# Tue, 01 Dec 2020 03:30:41 GMT
ENV FRIENDICA_ADDONS=2020.12-dev
# Tue, 01 Dec 2020 03:30:47 GMT
COPY multi:79fafe1f110f1d1a4fd44f7b958b2a83de813fc7f8cfcefe662a6fa6e275cf3e in / 
# Tue, 01 Dec 2020 03:30:48 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Tue, 01 Dec 2020 03:30:50 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 01 Dec 2020 03:30:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bad30e7b45c14f784ef29a828b5fc69db0ebdefebcde6a7c98f4f77ffc93a546`  
		Last Modified: Thu, 22 Oct 2020 02:01:42 GMT  
		Size: 2.6 MB (2601912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9bf946cf0a5f710967e36dd17cee52857cd6bda3def477e4f23823071a310d`  
		Last Modified: Thu, 22 Oct 2020 07:36:00 GMT  
		Size: 1.3 MB (1310155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fedfce6787031ac99140460dc123850a8ced1bdf113b93150f3c0a99891a588`  
		Last Modified: Thu, 22 Oct 2020 07:35:58 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2498251eae8b7a8b7d6fae9311ceec47f607cc852ba45c073a4fe55bf917b819`  
		Last Modified: Thu, 22 Oct 2020 07:35:58 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c42b8a7bbcff31a5d3cc2053ee4f4e9216cc6ad705b38d376e0b563795300efe`  
		Last Modified: Tue, 01 Dec 2020 02:55:22 GMT  
		Size: 12.2 MB (12155981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34eb50ed4653ceffede53490c6a092fba8878d278a6cd9a36a27ce53edf3ebe`  
		Last Modified: Tue, 01 Dec 2020 02:55:14 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41935ec942ff51597cbf45c3d0b818d227c620a78657ee57f15a21c9256eecb9`  
		Last Modified: Tue, 01 Dec 2020 02:55:21 GMT  
		Size: 13.8 MB (13802609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ddb59499eae5be5bbad340bb25728bec43b56cf82189033b59fda6c2d6bebd0`  
		Last Modified: Tue, 01 Dec 2020 02:55:15 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e48a6fc61a31bc8a26130dc136fcce2ec20ef29bffcad99747447b70f62b6ad`  
		Last Modified: Tue, 01 Dec 2020 02:55:15 GMT  
		Size: 16.7 KB (16745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d393120ff208a836cf3e8a8b65c426b5da0fd50af7ea8e623a9c8d4a7612a9a4`  
		Last Modified: Tue, 01 Dec 2020 02:55:14 GMT  
		Size: 8.4 KB (8415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcaefca939975f6f3833ef49a79c204c91fd3576ed031dbdc76be5573b84968`  
		Last Modified: Tue, 01 Dec 2020 03:31:13 GMT  
		Size: 10.9 MB (10868827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bb41ed11bd40f02cc6c922d62df3321be9afd4a2c82104a26d5a98852bd5d8`  
		Last Modified: Tue, 01 Dec 2020 03:31:08 GMT  
		Size: 9.0 MB (9011006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179670d64f3fb0963939186cd0e8fc6c216b4b778ef51535243f601a12c67803`  
		Last Modified: Tue, 01 Dec 2020 03:31:04 GMT  
		Size: 571.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62233d78097d91eda2100aa55c7cd3bc2437defe0b9c7de871b92e4893ae940f`  
		Last Modified: Tue, 01 Dec 2020 03:31:29 GMT  
		Size: 3.3 KB (3258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bddb40499cf34bc7011a3794cb2efad04b85a6125c91b8df0997ab6b4afcff34`  
		Last Modified: Tue, 01 Dec 2020 03:31:30 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:da3c74257a15a5f36847e34eb1d3dc13038d52c0956626bf017cd7079ff2f782
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46714071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc958229fffdf59e0c734e0ece4084c5949b5b4bba7c1c2268a6158a4802d86`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 01:58:13 GMT
ADD file:46f89172426e9f5b1d669a2ca7ab218fc2deaef1caeeab88f2b5bd443ac9773d in / 
# Thu, 22 Oct 2020 01:58:14 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 06:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 06:47:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 06:47:45 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 06:47:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 06:47:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 06:51:33 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 06:51:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:51:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 06:51:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:14:09 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Thu, 29 Oct 2020 22:26:19 GMT
ENV PHP_VERSION=7.3.24
# Thu, 29 Oct 2020 22:26:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.24.tar.xz.asc
# Thu, 05 Nov 2020 21:06:52 GMT
ENV PHP_SHA256=78b0b417a147ab7572c874334d11654e3c61ec5b3f2170098e5db02fb0c89888
# Thu, 05 Nov 2020 21:06:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Nov 2020 21:06:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Nov 2020 21:09:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Nov 2020 21:09:47 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Thu, 05 Nov 2020 21:09:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Nov 2020 21:09:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Nov 2020 21:09:52 GMT
WORKDIR /var/www/html
# Thu, 05 Nov 2020 21:09:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 05 Nov 2020 21:09:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Nov 2020 21:09:56 GMT
EXPOSE 9000
# Thu, 05 Nov 2020 21:09:56 GMT
CMD ["php-fpm"]
# Thu, 05 Nov 2020 23:51:07 GMT
RUN set -ex;     apk add --no-cache         rsync         git         msmtp         shadow         tini;
# Thu, 05 Nov 2020 23:54:04 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         pcntl         ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.3.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Thu, 05 Nov 2020 23:54:06 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 05 Nov 2020 23:54:07 GMT
VOLUME [/var/www/html]
# Thu, 05 Nov 2020 23:55:14 GMT
ENV FRIENDICA_VERSION=2020.12-dev
# Thu, 05 Nov 2020 23:55:15 GMT
ENV FRIENDICA_ADDONS=2020.12-dev
# Thu, 05 Nov 2020 23:55:16 GMT
COPY multi:79fafe1f110f1d1a4fd44f7b958b2a83de813fc7f8cfcefe662a6fa6e275cf3e in / 
# Thu, 05 Nov 2020 23:55:17 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Thu, 05 Nov 2020 23:55:18 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 05 Nov 2020 23:55:19 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f2023fd85a4e68f37fe41421fd89f30e69b98a645613521c57c01317561eee3`  
		Last Modified: Thu, 22 Oct 2020 01:58:45 GMT  
		Size: 2.4 MB (2405675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c60b50c98f8a8e2c6a27378dfa0f44df1844ac67c6981303675f138a42679f25`  
		Last Modified: Thu, 22 Oct 2020 07:35:57 GMT  
		Size: 1.2 MB (1214265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b472094d673b7c272085505c976192b9aaafa3157c99bade9755fbca18a24071`  
		Last Modified: Thu, 22 Oct 2020 07:35:56 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc39e5d916c11e7eb158e72d14ab981eb45ccc7b6451c1d6d3cb627b71cdbb6`  
		Last Modified: Thu, 22 Oct 2020 07:35:55 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a7cad05d52f9a7514074618783676125b1baa0d529fea0fffde9c2bbe46400`  
		Last Modified: Thu, 05 Nov 2020 22:28:36 GMT  
		Size: 12.2 MB (12157514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8002710a3de73a630c86febb9ff4f42ab821ae0904592228f4f6c13c926adf0f`  
		Last Modified: Thu, 05 Nov 2020 22:28:33 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a29a3ac7fb3a8686fae0987904dce14ef899c6fc55a232f3b1d7b5630b80697`  
		Last Modified: Thu, 05 Nov 2020 22:28:38 GMT  
		Size: 12.6 MB (12559587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757222ef57c2a5bd0f4e5fbd7e081e42ef9e3f16da7972663085acf3d225c205`  
		Last Modified: Thu, 05 Nov 2020 22:28:32 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4bd47f60a42549a9dbc3f940ed8999d8e34e6847a43f179d5520797d7b74544`  
		Last Modified: Thu, 05 Nov 2020 22:28:33 GMT  
		Size: 16.7 KB (16693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa25b25cde2b27543b9a1823818234f62547816203346479a7bde22c038b5bd`  
		Last Modified: Thu, 05 Nov 2020 22:28:32 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b285ff54f7fe5a1e3ab9fc12bb6e6b09f76ff4d66307f0ad0e5ed629a1026c`  
		Last Modified: Thu, 05 Nov 2020 23:56:37 GMT  
		Size: 9.8 MB (9838398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d8da6af681f5f231f67b28a610884075ec894aaca4f98eb5515a6d7141e1f`  
		Last Modified: Thu, 05 Nov 2020 23:56:52 GMT  
		Size: 8.5 MB (8504321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6c0471fe2fedeae5f66e321f2d85b5f2865fb29d1d5c75d154c26646f45be3`  
		Last Modified: Thu, 05 Nov 2020 23:56:34 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfc36cd7678c89ed7994d601ead18e6bba453e9974f87dd1aee72e9ef06987f`  
		Last Modified: Thu, 05 Nov 2020 23:57:18 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c252ce0d493c874bd2f90df5dc2a23340abe859e1e7d9b98b667a735f0ea28`  
		Last Modified: Thu, 05 Nov 2020 23:57:18 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:6cca57c06dad0b128fc264377c16d20c53aeb3012436c9cd31ea77da13f91735
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51537221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f7df233e4e18ab08cd677ff50cdd67d91bf63e0fdfc9066d22b38f7482ddab8`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:01:01 GMT
ADD file:55c4e9752146061a2b5f76027221329f423687987c0744ef577130c60ff0ba42 in / 
# Thu, 22 Oct 2020 02:01:06 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 07:18:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 07:18:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 07:18:59 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 07:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 07:19:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 07:23:16 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 07:23:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:23:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 07:23:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 07:44:56 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 01 Dec 2020 04:28:29 GMT
ENV PHP_VERSION=7.3.25
# Tue, 01 Dec 2020 04:28:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.25.tar.xz.asc
# Tue, 01 Dec 2020 04:28:31 GMT
ENV PHP_SHA256=c71c00ad03079efb78d1a6b8623ca4f725be697dbd9a46debacbcc9a2475f329
# Tue, 01 Dec 2020 04:28:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 01 Dec 2020 04:28:37 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:31:41 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 01 Dec 2020 04:31:43 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Tue, 01 Dec 2020 04:31:46 GMT
RUN docker-php-ext-enable sodium
# Tue, 01 Dec 2020 04:31:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 01 Dec 2020 04:31:47 GMT
WORKDIR /var/www/html
# Tue, 01 Dec 2020 04:31:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 01 Dec 2020 04:31:50 GMT
STOPSIGNAL SIGQUIT
# Tue, 01 Dec 2020 04:31:51 GMT
EXPOSE 9000
# Tue, 01 Dec 2020 04:31:52 GMT
CMD ["php-fpm"]
# Tue, 01 Dec 2020 05:50:52 GMT
RUN set -ex;     apk add --no-cache         rsync         git         msmtp         shadow         tini;
# Tue, 01 Dec 2020 05:54:04 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         pcntl         ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.3.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Tue, 01 Dec 2020 05:54:08 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Tue, 01 Dec 2020 05:54:09 GMT
VOLUME [/var/www/html]
# Tue, 01 Dec 2020 05:55:19 GMT
ENV FRIENDICA_VERSION=2020.12-dev
# Tue, 01 Dec 2020 05:55:20 GMT
ENV FRIENDICA_ADDONS=2020.12-dev
# Tue, 01 Dec 2020 05:55:22 GMT
COPY multi:79fafe1f110f1d1a4fd44f7b958b2a83de813fc7f8cfcefe662a6fa6e275cf3e in / 
# Tue, 01 Dec 2020 05:55:24 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Tue, 01 Dec 2020 05:55:25 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Tue, 01 Dec 2020 05:55:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f621e34cdf485f410766dc9a0fc7855d17916d0f6583b58cbdce7c28831f527`  
		Last Modified: Thu, 22 Oct 2020 02:01:38 GMT  
		Size: 2.7 MB (2706555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d57dba23203172f8fffd1379aef0307e782178b62dfc684d43c546f7e874ed`  
		Last Modified: Thu, 22 Oct 2020 08:06:21 GMT  
		Size: 1.3 MB (1342784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8414edb0c9c2f7472bb6228bf691a2ddac19ddad7bad789c7cbdc147aded711`  
		Last Modified: Thu, 22 Oct 2020 08:06:20 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d26eeef0db35b2328adae38a8490c7403844452c3606dd17fbe68216f98e82`  
		Last Modified: Thu, 22 Oct 2020 08:06:19 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacd8fb2aabf3e74c588266248e0997fa24daf33c0355981d6935d3286cd6a79`  
		Last Modified: Tue, 01 Dec 2020 04:58:26 GMT  
		Size: 12.2 MB (12155981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60eb33f1b0c04cfa57948e0410f66135bbf16433d72ff4da82baba40e8b7308`  
		Last Modified: Tue, 01 Dec 2020 04:58:23 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8d9d0267144b11834a677586c758951fd0d4dc78824da2b4341169f9fbe068`  
		Last Modified: Tue, 01 Dec 2020 04:58:27 GMT  
		Size: 14.6 MB (14594748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e62f493dca1da228c0c1d4c397061464851be5f72c59756f80a8b98f2bf973`  
		Last Modified: Tue, 01 Dec 2020 04:58:23 GMT  
		Size: 2.3 KB (2255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dac0a05df0280bc73db2cccc835cfa40acb00dfaa71cb12deb01de7ff4747b9`  
		Last Modified: Tue, 01 Dec 2020 04:58:24 GMT  
		Size: 16.8 KB (16758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08dc100d94d0dde62491349b05a450363e5741eae7494207a7061c1ef27d7deb`  
		Last Modified: Tue, 01 Dec 2020 04:58:23 GMT  
		Size: 8.4 KB (8414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec434dc0dd86ce9a152b76cdd8abc9fe1966e9463039158375f881103552cb5c`  
		Last Modified: Tue, 01 Dec 2020 05:56:41 GMT  
		Size: 11.5 MB (11494035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:295b81d9fcc019d54188f8dc04928ab7e27f4a68707ed5922cb37b3d76c6fa80`  
		Last Modified: Tue, 01 Dec 2020 05:56:37 GMT  
		Size: 9.2 MB (9208740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6238babb340ed46f8496145ba25aac4663dee5ad78f1111c53ae2521a01402a8`  
		Last Modified: Tue, 01 Dec 2020 05:56:35 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652ba0d7e0d44123d3df0e4c8b2a1c4fb108f04cd35fbf9c94c7a1915d7fd299`  
		Last Modified: Tue, 01 Dec 2020 05:57:19 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90ee19e8402ed113e59d062c731347c5540b5486e3914828c81543bdf3ab688`  
		Last Modified: Tue, 01 Dec 2020 05:57:19 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:2c6f4a9bbd89b67bc609b09211eab710be1054eee65e4078ec48af9dcb4c588f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53336458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfe136cc1f715f613cafb48e57093928a943acaf2b831c70b60e860eb9e704df`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 02:00:33 GMT
ADD file:46ad43b4984bcf49c5a888ff3628f23161f55cd1fb062f469e707100c97fa254 in / 
# Thu, 22 Oct 2020 02:00:33 GMT
CMD ["/bin/sh"]
# Thu, 22 Oct 2020 03:36:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 22 Oct 2020 03:36:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 22 Oct 2020 03:36:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 22 Oct 2020 03:36:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 22 Oct 2020 03:36:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 22 Oct 2020 03:45:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 22 Oct 2020 04:25:30 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 30 Oct 2020 01:24:24 GMT
ENV PHP_VERSION=7.3.24
# Fri, 30 Oct 2020 01:24:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.24.tar.xz.asc
# Thu, 05 Nov 2020 23:23:09 GMT
ENV PHP_SHA256=78b0b417a147ab7572c874334d11654e3c61ec5b3f2170098e5db02fb0c89888
# Thu, 05 Nov 2020 23:23:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Nov 2020 23:23:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Nov 2020 23:32:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Nov 2020 23:32:24 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Thu, 05 Nov 2020 23:32:27 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Nov 2020 23:32:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Nov 2020 23:32:27 GMT
WORKDIR /var/www/html
# Thu, 05 Nov 2020 23:32:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 05 Nov 2020 23:32:29 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Nov 2020 23:32:29 GMT
EXPOSE 9000
# Thu, 05 Nov 2020 23:32:30 GMT
CMD ["php-fpm"]
# Fri, 06 Nov 2020 03:16:33 GMT
RUN set -ex;     apk add --no-cache         rsync         git         msmtp         shadow         tini;
# Fri, 06 Nov 2020 03:18:39 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         pcntl         ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.3.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Fri, 06 Nov 2020 03:18:40 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 06 Nov 2020 03:18:40 GMT
VOLUME [/var/www/html]
# Fri, 06 Nov 2020 03:19:15 GMT
ENV FRIENDICA_VERSION=2020.12-dev
# Fri, 06 Nov 2020 03:19:15 GMT
ENV FRIENDICA_ADDONS=2020.12-dev
# Fri, 06 Nov 2020 03:19:16 GMT
COPY multi:79fafe1f110f1d1a4fd44f7b958b2a83de813fc7f8cfcefe662a6fa6e275cf3e in / 
# Fri, 06 Nov 2020 03:19:16 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Fri, 06 Nov 2020 03:19:17 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 06 Nov 2020 03:19:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d6ca64ac6f4b6382142ce9a3501652938130a6ec4bb02f3f455ee1f980834cfe`  
		Last Modified: Thu, 22 Oct 2020 02:00:57 GMT  
		Size: 2.8 MB (2791407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30be8ffd290910905a5fb7cbb70252eb0f59edb09db20bdc21f3b65456acc28f`  
		Last Modified: Thu, 22 Oct 2020 05:10:23 GMT  
		Size: 1.4 MB (1439641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d58e2433b13446c863e85b34f8e4c93ca9d5b3b93d2bac415fd9cdf77bcec4`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5729dcb8d303f82a7f8cf3df49048e34ce8ee89f79155fb08a475da46b64308`  
		Last Modified: Thu, 22 Oct 2020 05:10:21 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4dca009994b09306528d0f65315921227ddf385cc32e6d1d9938cccc48dd7d`  
		Last Modified: Fri, 06 Nov 2020 02:18:03 GMT  
		Size: 12.2 MB (12157496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fea886b296ef06204a9de1234a59d6b414d12b5120b9aaccf4b328588bcafe0`  
		Last Modified: Fri, 06 Nov 2020 02:18:00 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ae81ad06e41c46b42827fb53969de4d189eac7fda0caed4776c2a7b8f66440`  
		Last Modified: Fri, 06 Nov 2020 02:18:06 GMT  
		Size: 14.8 MB (14806988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615ac1996efaaf85344698a4bd2f9bfabb87a512538a367f5bc5d8646ed330ef`  
		Last Modified: Fri, 06 Nov 2020 02:18:00 GMT  
		Size: 2.3 KB (2260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8a09e70a99fbdcb112b704515093c262040a6c075219da66e45cbc17da1825`  
		Last Modified: Fri, 06 Nov 2020 02:18:00 GMT  
		Size: 16.7 KB (16708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d24637b7621e684a43750d37ee127c399cdda0fd8a78f934364a2011c9d4e156`  
		Last Modified: Fri, 06 Nov 2020 02:18:00 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3df5cf5ed525f01780b7b51d25a92ea83afd6102250e2265a87896dbbd8321f`  
		Last Modified: Fri, 06 Nov 2020 03:20:29 GMT  
		Size: 12.4 MB (12434297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2ae9088556be2274dd8d693a161058715ee56a4e0603cdb885c2342bf80274`  
		Last Modified: Fri, 06 Nov 2020 03:20:26 GMT  
		Size: 9.7 MB (9672440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4967f22ad59ea8c104a95e4bfa8036b087cba16d97ee38619bd96b391239f462`  
		Last Modified: Fri, 06 Nov 2020 03:20:22 GMT  
		Size: 542.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34d27212010d1b31e18f1f330756c05338cccb31d5b025cc3669273071db6a1`  
		Last Modified: Fri, 06 Nov 2020 03:20:55 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da8155bc7314b0edf5b39244b8749956fa0e037f2d94d1bee788cf4b161852b`  
		Last Modified: Fri, 06 Nov 2020 03:20:56 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:7f4222d643b560e51128a25b1b27a774d66f7fe2dd522fe2104600482c598e7b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53570013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f32d24b706ae9b5274cb350994562292deea75dd5cbf52dbb00326934d5261a1`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 22 Oct 2020 11:00:06 GMT
ADD file:176e047fab2c1828575bffa6b14773efa297b7ecf312d86103c5dd4f78ec8027 in / 
# Thu, 22 Oct 2020 11:00:17 GMT
CMD ["/bin/sh"]
# Fri, 23 Oct 2020 00:21:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 23 Oct 2020 00:21:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 23 Oct 2020 00:21:30 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 23 Oct 2020 00:21:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 23 Oct 2020 00:21:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 23 Oct 2020 00:27:50 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 23 Oct 2020 00:27:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:28:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 23 Oct 2020 00:28:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 23 Oct 2020 00:56:44 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 30 Oct 2020 00:28:36 GMT
ENV PHP_VERSION=7.3.24
# Fri, 30 Oct 2020 00:28:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.24.tar.xz.asc
# Thu, 05 Nov 2020 21:57:57 GMT
ENV PHP_SHA256=78b0b417a147ab7572c874334d11654e3c61ec5b3f2170098e5db02fb0c89888
# Thu, 05 Nov 2020 21:58:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 05 Nov 2020 21:58:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 05 Nov 2020 22:02:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 05 Nov 2020 22:02:17 GMT
COPY multi:ebc915bbde1078ce3122b918e2e4c7726858af785343ade1a8d1a94f1052a4c7 in /usr/local/bin/ 
# Thu, 05 Nov 2020 22:02:23 GMT
RUN docker-php-ext-enable sodium
# Thu, 05 Nov 2020 22:02:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 05 Nov 2020 22:02:33 GMT
WORKDIR /var/www/html
# Thu, 05 Nov 2020 22:02:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 05 Nov 2020 22:02:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Nov 2020 22:02:44 GMT
EXPOSE 9000
# Thu, 05 Nov 2020 22:02:46 GMT
CMD ["php-fpm"]
# Fri, 06 Nov 2020 04:37:10 GMT
RUN set -ex;     apk add --no-cache         rsync         git         msmtp         shadow         tini;
# Fri, 06 Nov 2020 04:40:25 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         pcntl         ldap     ;         pecl install APCu-5.1.18;     pecl install memcached-3.1.5;     pecl install redis-5.3.1;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Fri, 06 Nov 2020 04:40:51 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 06 Nov 2020 04:41:05 GMT
VOLUME [/var/www/html]
# Fri, 06 Nov 2020 04:44:09 GMT
ENV FRIENDICA_VERSION=2020.12-dev
# Fri, 06 Nov 2020 04:44:15 GMT
ENV FRIENDICA_ADDONS=2020.12-dev
# Fri, 06 Nov 2020 04:44:22 GMT
COPY multi:79fafe1f110f1d1a4fd44f7b958b2a83de813fc7f8cfcefe662a6fa6e275cf3e in / 
# Fri, 06 Nov 2020 04:44:25 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Fri, 06 Nov 2020 04:44:29 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 06 Nov 2020 04:44:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:692a9d763e196c85d79fc3e45b316b1bb557c93ba88a3c8ebf679a585d1efe73`  
		Last Modified: Thu, 22 Oct 2020 11:02:06 GMT  
		Size: 2.8 MB (2803218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285d6f06f3beb1c140c055210664c441b93dd4f2037177a5396bce94ca16ce5`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 1.4 MB (1383187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6459a3bf272daa53ff4ba97cc849676f497de9f78d8e9378ec02552293f175`  
		Last Modified: Fri, 23 Oct 2020 01:34:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16cff6064dc29d3f629d353736c1cac074caa5b50738422adb84de99a019bb32`  
		Last Modified: Fri, 23 Oct 2020 01:34:08 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4d6b156a76a585928254d76712c3b5be5eaf50dc2dd49fbabf275f4110128f`  
		Last Modified: Thu, 05 Nov 2020 23:46:38 GMT  
		Size: 12.2 MB (12157541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265ee9d171ad61dcd108e60e3a904516a8eade8acb027a04a8ba3f22e930d776`  
		Last Modified: Thu, 05 Nov 2020 23:46:34 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18f2d5e2898ecbd44f949d9b593d3cbc2d57ee9c37542fe0b548ee5d720bd14`  
		Last Modified: Thu, 05 Nov 2020 23:46:37 GMT  
		Size: 15.5 MB (15480994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c7e87a7304d96e39e7ad15d0a9c17407cf17270135e4457c155fa911a59a73`  
		Last Modified: Thu, 05 Nov 2020 23:46:34 GMT  
		Size: 2.3 KB (2255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeccced4fbb2cf41c86664d008b2b41f4b5925e22cf1813818f8997909a3b38f`  
		Last Modified: Thu, 05 Nov 2020 23:46:35 GMT  
		Size: 16.7 KB (16720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b82334c1f1d930529b089482ebcd77e3af8997322db3fce7d29cb89a4e5748d`  
		Last Modified: Thu, 05 Nov 2020 23:46:34 GMT  
		Size: 8.4 KB (8410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa8cf0793d575ae7e3280186331e4509f613467adf45809cd3f91c4bb670c3a`  
		Last Modified: Fri, 06 Nov 2020 04:48:09 GMT  
		Size: 12.1 MB (12069640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67934b38556c48ea089edfef5061282dc12d2873d6e026f3d7199f465eb6b1db`  
		Last Modified: Fri, 06 Nov 2020 04:48:05 GMT  
		Size: 9.6 MB (9641094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce65d6bf83a495fbde25ee192016956e59cf3f872a73272c5e1905f7baa7a241`  
		Last Modified: Fri, 06 Nov 2020 04:48:02 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96ecfe34014bdc6673ef0ad3faa92c5eb39b213202ef6c12aecaecc0c4b7629`  
		Last Modified: Fri, 06 Nov 2020 04:49:05 GMT  
		Size: 3.3 KB (3259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fad6c7044bc6485261be636d6a7b93a70739e0d539847ef25193d09e4b1aee69`  
		Last Modified: Fri, 06 Nov 2020 04:49:05 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
