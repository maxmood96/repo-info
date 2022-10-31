## `friendica:dev-fpm-alpine`

```console
$ docker pull friendica@sha256:c8c06a8b4e2fe57a5ad4669ef101fad52cbd293f7ec750fbf955258bfcaabe61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `friendica:dev-fpm-alpine` - linux; amd64

```console
$ docker pull friendica@sha256:7ca1e91f0fdddc5a46dd23b1e766ebfa6c307206d0f9060f4e9ad8a8722f527f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43125065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19cce8b42889e43becd1eb5c0a37376e971f3f84b619df41c27bd587c953106a`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
# Fri, 07 Oct 2022 00:34:50 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 07 Oct 2022 00:34:51 GMT
ENV PHP_VERSION=7.4.32
# Fri, 07 Oct 2022 00:34:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.32.tar.xz.asc
# Fri, 07 Oct 2022 00:34:51 GMT
ENV PHP_SHA256=323332c991e8ef30b1d219cb10f5e30f11b5f319ce4c6642a5470d75ade7864a
# Fri, 07 Oct 2022 00:34:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 07 Oct 2022 00:34:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 07 Oct 2022 00:42:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 07 Oct 2022 00:42:12 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 07 Oct 2022 00:42:13 GMT
RUN docker-php-ext-enable sodium
# Fri, 07 Oct 2022 00:42:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Oct 2022 00:42:13 GMT
WORKDIR /var/www/html
# Fri, 07 Oct 2022 00:42:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 07 Oct 2022 00:42:14 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Oct 2022 00:42:14 GMT
EXPOSE 9000
# Fri, 07 Oct 2022 00:42:14 GMT
CMD ["php-fpm"]
# Fri, 07 Oct 2022 07:36:50 GMT
RUN set -ex;     apk add --no-cache         rsync         msmtp         shadow         tini;
# Fri, 07 Oct 2022 07:36:50 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Oct 2022 07:36:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 31 Oct 2022 18:27:10 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Mon, 31 Oct 2022 18:27:10 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 31 Oct 2022 18:27:11 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 31 Oct 2022 18:27:11 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Mon, 31 Oct 2022 18:27:11 GMT
VOLUME [/var/www/html]
# Mon, 31 Oct 2022 18:27:11 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 31 Oct 2022 18:27:59 GMT
ENV FRIENDICA_VERSION=2022.12-dev
# Mon, 31 Oct 2022 18:27:59 GMT
ENV FRIENDICA_ADDONS=2022.12-dev
# Mon, 31 Oct 2022 18:28:00 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;
# Mon, 31 Oct 2022 18:28:01 GMT
COPY multi:f87d330cfcee641708f831c1e9357b18f2b0ed18bc7541fec914e00a972d58a1 in / 
# Mon, 31 Oct 2022 18:28:01 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Mon, 31 Oct 2022 18:28:01 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Mon, 31 Oct 2022 18:28:01 GMT
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
	-	`sha256:67b7efc692d42dead324b12ce34e0f64fccadcafa5452948705615cfdda9218d`  
		Last Modified: Fri, 07 Oct 2022 01:08:16 GMT  
		Size: 10.4 MB (10439218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5daa387348b1c4cdfb105127b72ba31a7a7b3966181c67c1252fec4dde6ee0`  
		Last Modified: Fri, 07 Oct 2022 01:08:15 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666f57addfdedb581772e84e3790c24d37961e53c84547f3806a16e2476903fa`  
		Last Modified: Fri, 07 Oct 2022 01:08:57 GMT  
		Size: 11.5 MB (11456381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c165b7f9f1010e25d3213849d32743547aa30b71e448ad852933e891d546c1b7`  
		Last Modified: Fri, 07 Oct 2022 01:08:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af4fb7ae1e5d539407b05307ac0b11a9f9b6b30399ff428f0881bc4fd440bad`  
		Last Modified: Fri, 07 Oct 2022 01:08:55 GMT  
		Size: 18.6 KB (18624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b2877e24a9a24fb112f128555c09d5788876c5469e9293194e8f9f38470184`  
		Last Modified: Fri, 07 Oct 2022 01:08:55 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d952180d1d8d1f30dbf94fb68046bc6e0f52bfb7b9bc2f26c0b6c46f9408f165`  
		Last Modified: Fri, 07 Oct 2022 07:40:34 GMT  
		Size: 4.0 MB (3991756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fb92daf403f4c18c725aafb6aec07c249ba24efd1cb643769767020b286a41d`  
		Last Modified: Fri, 07 Oct 2022 07:40:33 GMT  
		Size: 956.4 KB (956418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17aff61968fecd8cb4e0441daf9edfe7403dd7ad7c21a1e84c4944859211fba7`  
		Last Modified: Mon, 31 Oct 2022 18:29:21 GMT  
		Size: 8.8 MB (8849840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5a460be63d9f32759c5219e0be742c923bb071a2b5684c6e7d71b01bc8e12b`  
		Last Modified: Mon, 31 Oct 2022 18:29:19 GMT  
		Size: 638.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e8763908225c66f16f4fbc3a2fdd7d98eadff1b108e9acc185aa2458ffa98d`  
		Last Modified: Mon, 31 Oct 2022 18:30:16 GMT  
		Size: 2.9 MB (2867543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6efa824c7c1967dd7bed39b3f1618b1d3510b9d4416cfdc2cbc395a621cc65e6`  
		Last Modified: Mon, 31 Oct 2022 18:30:16 GMT  
		Size: 3.6 KB (3623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72c60ac56876bc38a8cfda41f047f15927b3542b432c391e4d160dbd5a06a85`  
		Last Modified: Mon, 31 Oct 2022 18:30:16 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:6249085255d5355b3ed2854e482db32f65ffe83ceaf2adf7f5606c934cdb73e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41433879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcdbfc1e13adca1cb07677111ab81a28156155825af28397c2029613c69a8f1`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
# Thu, 27 Oct 2022 23:33:56 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 27 Oct 2022 23:33:56 GMT
ENV PHP_VERSION=7.4.32
# Thu, 27 Oct 2022 23:33:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.32.tar.xz.asc
# Thu, 27 Oct 2022 23:33:56 GMT
ENV PHP_SHA256=323332c991e8ef30b1d219cb10f5e30f11b5f319ce4c6642a5470d75ade7864a
# Thu, 27 Oct 2022 23:34:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 27 Oct 2022 23:34:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 27 Oct 2022 23:41:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 27 Oct 2022 23:41:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 27 Oct 2022 23:41:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 27 Oct 2022 23:41:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 27 Oct 2022 23:41:04 GMT
WORKDIR /var/www/html
# Thu, 27 Oct 2022 23:41:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 27 Oct 2022 23:41:04 GMT
STOPSIGNAL SIGQUIT
# Thu, 27 Oct 2022 23:41:04 GMT
EXPOSE 9000
# Thu, 27 Oct 2022 23:41:05 GMT
CMD ["php-fpm"]
# Fri, 28 Oct 2022 01:23:13 GMT
RUN set -ex;     apk add --no-cache         rsync         msmtp         shadow         tini;
# Fri, 28 Oct 2022 01:23:13 GMT
ENV GOSU_VERSION=1.14
# Fri, 28 Oct 2022 01:23:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 31 Oct 2022 17:51:47 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Mon, 31 Oct 2022 17:51:47 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 31 Oct 2022 17:51:47 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 31 Oct 2022 17:51:48 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Mon, 31 Oct 2022 17:51:48 GMT
VOLUME [/var/www/html]
# Mon, 31 Oct 2022 17:51:48 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 31 Oct 2022 17:52:17 GMT
ENV FRIENDICA_VERSION=2022.12-dev
# Mon, 31 Oct 2022 17:52:18 GMT
ENV FRIENDICA_ADDONS=2022.12-dev
# Mon, 31 Oct 2022 17:52:19 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;
# Mon, 31 Oct 2022 17:52:19 GMT
COPY multi:f87d330cfcee641708f831c1e9357b18f2b0ed18bc7541fec914e00a972d58a1 in / 
# Mon, 31 Oct 2022 17:52:20 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Mon, 31 Oct 2022 17:52:20 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Mon, 31 Oct 2022 17:52:20 GMT
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
	-	`sha256:d81e3510fe09b6fa1d827e814c19df8be7008be84b0d6dc4761189d5f4420861`  
		Last Modified: Fri, 28 Oct 2022 00:11:46 GMT  
		Size: 10.4 MB (10439196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd9deba0698eadc656cddf72666c1e339140329e8e35ded7967c2645a966407`  
		Last Modified: Fri, 28 Oct 2022 00:11:44 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002e9dfe69b7e2f097d135c4cb8c2c64b62a46cd2e5505886e23bca0e3d175a1`  
		Last Modified: Fri, 28 Oct 2022 00:12:40 GMT  
		Size: 10.7 MB (10722888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a2155a1be1ebf0c223234fa2d3bfca70bc64b54b8b73c415bc2766ac8b4a99`  
		Last Modified: Fri, 28 Oct 2022 00:12:38 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d96c69fce9de4cdd9fd468e17ed8977043153faaea09ed450752d6812d259d`  
		Last Modified: Fri, 28 Oct 2022 00:12:38 GMT  
		Size: 18.6 KB (18640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8f4094b637ff17095fb620ef126de435cd5c67d9749989af505c023b3bd2670`  
		Last Modified: Fri, 28 Oct 2022 00:12:38 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabe60c8c1cd8214de9800db4fd85dd7df91f84dbaa9ef8b60333a89a9454bbc`  
		Last Modified: Fri, 28 Oct 2022 01:26:23 GMT  
		Size: 3.9 MB (3881576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b88c7285bd45046734bf81e98dd9b521dba4a36e5cd4c81b78b98156145fdee`  
		Last Modified: Fri, 28 Oct 2022 01:26:22 GMT  
		Size: 910.9 KB (910914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4467056eb0fbdc0ff415e9ea32eedca903da09d7df33a5b0d6f6f8bf64a5bc8c`  
		Last Modified: Mon, 31 Oct 2022 17:52:43 GMT  
		Size: 8.4 MB (8413017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfec6ac04f132ae9a0637bbddece0a1e2f9f91160781e856be4e1022577758a`  
		Last Modified: Mon, 31 Oct 2022 17:52:41 GMT  
		Size: 606.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a37630a7dd9e95b12be2456175c91598e8787b77be50e318342b930bdc7a9f`  
		Last Modified: Mon, 31 Oct 2022 17:53:09 GMT  
		Size: 2.7 MB (2707712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f418d7569629f9dd2d0f5077fb91c1ef023969eb23966a4a7e2ebc6c3e3b1b5`  
		Last Modified: Mon, 31 Oct 2022 17:53:08 GMT  
		Size: 3.6 KB (3624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded02828c76bece136e8d9a258f9907af7ece3f9a8bef1ee2940ef85b1f114ff`  
		Last Modified: Mon, 31 Oct 2022 17:53:08 GMT  
		Size: 922.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:97c47082a8066d990c65d4f1c90e2f8621917c406612e6bed732340d41e2da16
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39479219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a91a04d6b953ed8e36eb3b0b9adc2108317dfdc8e378b953d73aba76fd1e11f0`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
# Wed, 26 Oct 2022 03:02:11 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 26 Oct 2022 03:02:11 GMT
ENV PHP_VERSION=7.4.32
# Wed, 26 Oct 2022 03:02:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.32.tar.xz.asc
# Wed, 26 Oct 2022 03:02:11 GMT
ENV PHP_SHA256=323332c991e8ef30b1d219cb10f5e30f11b5f319ce4c6642a5470d75ade7864a
# Wed, 26 Oct 2022 03:02:18 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 26 Oct 2022 03:02:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 26 Oct 2022 03:08:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 26 Oct 2022 03:08:39 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 26 Oct 2022 03:08:40 GMT
RUN docker-php-ext-enable sodium
# Wed, 26 Oct 2022 03:08:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 26 Oct 2022 03:08:41 GMT
WORKDIR /var/www/html
# Wed, 26 Oct 2022 03:08:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 26 Oct 2022 03:08:41 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Oct 2022 03:08:41 GMT
EXPOSE 9000
# Wed, 26 Oct 2022 03:08:41 GMT
CMD ["php-fpm"]
# Wed, 26 Oct 2022 18:44:29 GMT
RUN set -ex;     apk add --no-cache         rsync         msmtp         shadow         tini;
# Wed, 26 Oct 2022 18:44:29 GMT
ENV GOSU_VERSION=1.14
# Wed, 26 Oct 2022 18:44:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 31 Oct 2022 18:05:37 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Mon, 31 Oct 2022 18:05:37 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 31 Oct 2022 18:05:37 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 31 Oct 2022 18:05:38 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Mon, 31 Oct 2022 18:05:38 GMT
VOLUME [/var/www/html]
# Mon, 31 Oct 2022 18:05:38 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 31 Oct 2022 18:06:39 GMT
ENV FRIENDICA_VERSION=2022.12-dev
# Mon, 31 Oct 2022 18:06:39 GMT
ENV FRIENDICA_ADDONS=2022.12-dev
# Mon, 31 Oct 2022 18:06:40 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;
# Mon, 31 Oct 2022 18:06:40 GMT
COPY multi:f87d330cfcee641708f831c1e9357b18f2b0ed18bc7541fec914e00a972d58a1 in / 
# Mon, 31 Oct 2022 18:06:40 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Mon, 31 Oct 2022 18:06:40 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Mon, 31 Oct 2022 18:06:41 GMT
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
	-	`sha256:eedc7518cef1f78d04ec639cab5e9697825dc3992eac3f9b9a7b0375e55202ea`  
		Last Modified: Wed, 26 Oct 2022 04:05:30 GMT  
		Size: 10.4 MB (10439183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4458e574210fdff978000c2c6b4dfe8917cff197644291dad35dd9e1e542c0`  
		Last Modified: Wed, 26 Oct 2022 04:05:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24f74742bc628392872465341db5e225a3b42efec42b1bbcd92d44e6c1ff6e1`  
		Last Modified: Wed, 26 Oct 2022 04:06:25 GMT  
		Size: 10.1 MB (10089390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f51fab92a47bd8cfd78d9e0628fd3d2fec9104fee53b1c8b43da0db373dc39`  
		Last Modified: Wed, 26 Oct 2022 04:06:24 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a067adefa41fa7697b7c2961d4d28eccc83f5aa73235ba3409b8b73ca9087b44`  
		Last Modified: Wed, 26 Oct 2022 04:06:23 GMT  
		Size: 18.6 KB (18619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1369a43e92271bd89f06ce3e905e36811dbd9f27ae0f211df616dc138729023`  
		Last Modified: Wed, 26 Oct 2022 04:06:23 GMT  
		Size: 8.4 KB (8442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea7b27e71f490f0a27d0b5f64531556c1d9079049e481685ea1d41a70d77242f`  
		Last Modified: Wed, 26 Oct 2022 18:49:48 GMT  
		Size: 3.6 MB (3595963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5f4101f780a6d4147b27fe058ee10daf70f4be137d58855c76a22d72c7810c`  
		Last Modified: Wed, 26 Oct 2022 18:49:48 GMT  
		Size: 910.9 KB (910882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c499d52efb78e3b4267b145b36549fafa97fd373c63a620b1a5de9b83209cfa`  
		Last Modified: Mon, 31 Oct 2022 18:08:48 GMT  
		Size: 8.0 MB (7988054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650c2e7aed50cf7bf63653829eba06d06eed519abd35735d684a447e4df445a5`  
		Last Modified: Mon, 31 Oct 2022 18:08:46 GMT  
		Size: 607.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680e3f6e13766e6c4c52d25874a0720310085e60deccaea08327f733525eaa7e`  
		Last Modified: Mon, 31 Oct 2022 18:09:51 GMT  
		Size: 2.4 MB (2426663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4a7f4f92a2326d1d3ad87d0e7961a119eff5164c89ed994cc717fdb849d1a0`  
		Last Modified: Mon, 31 Oct 2022 18:09:51 GMT  
		Size: 3.6 KB (3623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062d7aa8fae32734a6b745beec861af35b9b06159228edfdb00991a9b4833bdc`  
		Last Modified: Mon, 31 Oct 2022 18:09:51 GMT  
		Size: 916.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:cd545103e0c93240028122821e9f9fd465097d92c1b4fc73aff702ced821a83a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.4 MB (42363426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a6410e1d31904ba7aa4880f50a85ecabbe192fc0d205ad672c37eb74af0aec`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
# Tue, 25 Oct 2022 19:16:55 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Tue, 25 Oct 2022 19:16:55 GMT
ENV PHP_VERSION=7.4.32
# Tue, 25 Oct 2022 19:16:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.32.tar.xz.asc
# Tue, 25 Oct 2022 19:16:55 GMT
ENV PHP_SHA256=323332c991e8ef30b1d219cb10f5e30f11b5f319ce4c6642a5470d75ade7864a
# Tue, 25 Oct 2022 19:17:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 25 Oct 2022 19:17:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 25 Oct 2022 19:22:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 25 Oct 2022 19:22:23 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 25 Oct 2022 19:22:24 GMT
RUN docker-php-ext-enable sodium
# Tue, 25 Oct 2022 19:22:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 25 Oct 2022 19:22:24 GMT
WORKDIR /var/www/html
# Tue, 25 Oct 2022 19:22:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 25 Oct 2022 19:22:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 25 Oct 2022 19:22:25 GMT
EXPOSE 9000
# Tue, 25 Oct 2022 19:22:25 GMT
CMD ["php-fpm"]
# Wed, 26 Oct 2022 11:17:46 GMT
RUN set -ex;     apk add --no-cache         rsync         msmtp         shadow         tini;
# Wed, 26 Oct 2022 11:17:46 GMT
ENV GOSU_VERSION=1.14
# Wed, 26 Oct 2022 11:17:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 31 Oct 2022 17:46:16 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Mon, 31 Oct 2022 17:46:16 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 31 Oct 2022 17:46:16 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 31 Oct 2022 17:46:16 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Mon, 31 Oct 2022 17:46:16 GMT
VOLUME [/var/www/html]
# Mon, 31 Oct 2022 17:46:16 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 31 Oct 2022 17:46:58 GMT
ENV FRIENDICA_VERSION=2022.12-dev
# Mon, 31 Oct 2022 17:46:58 GMT
ENV FRIENDICA_ADDONS=2022.12-dev
# Mon, 31 Oct 2022 17:46:59 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;
# Mon, 31 Oct 2022 17:46:59 GMT
COPY multi:f87d330cfcee641708f831c1e9357b18f2b0ed18bc7541fec914e00a972d58a1 in / 
# Mon, 31 Oct 2022 17:47:00 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Mon, 31 Oct 2022 17:47:00 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Mon, 31 Oct 2022 17:47:00 GMT
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
	-	`sha256:664868964080c3c7ee3868f6fd862ae9dac393f3c15d3b511d813445f5cb7619`  
		Last Modified: Tue, 25 Oct 2022 20:01:01 GMT  
		Size: 10.4 MB (10439215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22ffb7a98299cdeea38dba628512187ed7b815e35488d00836e2f27852d54afb`  
		Last Modified: Tue, 25 Oct 2022 20:01:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dfa75e0306e62dfdd489f6cc09977fd7e43caf0e809015964d9687d01fe75a`  
		Last Modified: Tue, 25 Oct 2022 20:01:40 GMT  
		Size: 11.3 MB (11284539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666852b83a2af8f8fa12dd9cb41dc12efca0ea69665511fa355bb3822b24a358`  
		Last Modified: Tue, 25 Oct 2022 20:01:38 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ae3dc1fb5f0ad09f274c1122a3979adb05d43e9b8ebff1691d8d8cd52bb486`  
		Last Modified: Tue, 25 Oct 2022 20:01:38 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f8f2d896239d47e85d282760926f21786b452da85e6b01fd988c2a5bce69c1`  
		Last Modified: Tue, 25 Oct 2022 20:01:38 GMT  
		Size: 8.4 KB (8440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc521f2c4c50f8dedf618adb2e2ff40f7c47888211943292dc2cd3027e408afb`  
		Last Modified: Wed, 26 Oct 2022 11:22:04 GMT  
		Size: 3.9 MB (3895282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69ba099f018453d9e1fa0a8c7db7d60cdc81ea60073424c16baabeb9373d589`  
		Last Modified: Wed, 26 Oct 2022 11:21:25 GMT  
		Size: 882.6 KB (882586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade10ab7d4f235de7eb9d1d7ba63de1ea107218d6f966c38a88ab40a88d4a97c`  
		Last Modified: Mon, 31 Oct 2022 17:48:18 GMT  
		Size: 8.6 MB (8607726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e57ab79e1b3aa070a1056070cee94fc1c74f06720b361a82fb70aef5724113`  
		Last Modified: Mon, 31 Oct 2022 17:48:16 GMT  
		Size: 633.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1740305c84e6c69bbe99470ce187d103b08b76e93cfa3559240da4b329d710cd`  
		Last Modified: Mon, 31 Oct 2022 17:49:07 GMT  
		Size: 2.8 MB (2794093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b6624b1443f3013214b464d0503ecb91e76c5662abc7b0b04c17ea855219321`  
		Last Modified: Mon, 31 Oct 2022 17:49:06 GMT  
		Size: 3.6 KB (3624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:080b4d84d8b9b5a7d0e8d9a82fc9f0e79f6a3c22d1d09f9c607035a58b8b58fd`  
		Last Modified: Mon, 31 Oct 2022 17:49:06 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:358ca9398e53d2b08b30bc5695bcc8e146d4239178c60b033e23b49e4b51b81e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44036828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbbaddf40c9b97ee289e084ec336fac3a3a3a39c9a8f99cbf757bb4207f929e`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
# Thu, 06 Oct 2022 22:15:24 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Thu, 06 Oct 2022 22:15:25 GMT
ENV PHP_VERSION=7.4.32
# Thu, 06 Oct 2022 22:15:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.32.tar.xz.asc
# Thu, 06 Oct 2022 22:15:27 GMT
ENV PHP_SHA256=323332c991e8ef30b1d219cb10f5e30f11b5f319ce4c6642a5470d75ade7864a
# Thu, 06 Oct 2022 22:15:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Oct 2022 22:15:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Oct 2022 22:22:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Oct 2022 22:22:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Oct 2022 22:22:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Oct 2022 22:22:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Oct 2022 22:22:56 GMT
WORKDIR /var/www/html
# Thu, 06 Oct 2022 22:22:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 06 Oct 2022 22:22:58 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Oct 2022 22:22:59 GMT
EXPOSE 9000
# Thu, 06 Oct 2022 22:23:00 GMT
CMD ["php-fpm"]
# Fri, 07 Oct 2022 03:53:26 GMT
RUN set -ex;     apk add --no-cache         rsync         msmtp         shadow         tini;
# Fri, 07 Oct 2022 03:53:27 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Oct 2022 03:53:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 31 Oct 2022 17:45:57 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Mon, 31 Oct 2022 17:45:57 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 31 Oct 2022 17:45:58 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 31 Oct 2022 17:45:59 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Mon, 31 Oct 2022 17:46:00 GMT
VOLUME [/var/www/html]
# Mon, 31 Oct 2022 17:46:01 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 31 Oct 2022 17:47:05 GMT
ENV FRIENDICA_VERSION=2022.12-dev
# Mon, 31 Oct 2022 17:47:06 GMT
ENV FRIENDICA_ADDONS=2022.12-dev
# Mon, 31 Oct 2022 17:47:08 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;
# Mon, 31 Oct 2022 17:47:10 GMT
COPY multi:f87d330cfcee641708f831c1e9357b18f2b0ed18bc7541fec914e00a972d58a1 in / 
# Mon, 31 Oct 2022 17:47:11 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Mon, 31 Oct 2022 17:47:11 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Mon, 31 Oct 2022 17:47:12 GMT
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
	-	`sha256:b5458c9da6e79c236eddfb18bbdb6f1359c52e1b6da799d6382051004297fb27`  
		Last Modified: Thu, 06 Oct 2022 22:55:37 GMT  
		Size: 10.4 MB (10438969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153dbefe8df979a402078b4061e23e311c95428f1a5a4559f494ff176b4098b5`  
		Last Modified: Thu, 06 Oct 2022 22:55:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748ba659140e5e25d1cdc6da71c74e7471438f99583b03441dce6b2e50e902fa`  
		Last Modified: Thu, 06 Oct 2022 22:56:25 GMT  
		Size: 11.8 MB (11765154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c277a0508d62f8a0db2b2f9c6f09b699d848ca7ae18a638b378d22770a966b25`  
		Last Modified: Thu, 06 Oct 2022 22:56:23 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b371d2dbaa147a2563f8edfe1bcc2c4091dc8502c6c83aa28f1bb58fd20e2b8`  
		Last Modified: Thu, 06 Oct 2022 22:56:23 GMT  
		Size: 18.5 KB (18518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e94df3598c10a99b07d7b9a665a5dedc5854e07f20fed44076c7761d187244d`  
		Last Modified: Thu, 06 Oct 2022 22:56:23 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac9368f71118f9d4cfb4f9a4ede40d0e281287d86517e9f67bfaa479672a84ba`  
		Last Modified: Fri, 07 Oct 2022 03:58:36 GMT  
		Size: 4.1 MB (4059413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ff7f2d7c18a88d6c7d65c82b03b9fcfbccc5b86bd5a87c1028f9b4750c9fe2`  
		Last Modified: Fri, 07 Oct 2022 03:58:36 GMT  
		Size: 922.8 KB (922787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:637d1e06c2490c5d803f17dedc0012aeca27a1792df9f0fd4baa132cb202c0f7`  
		Last Modified: Mon, 31 Oct 2022 17:48:59 GMT  
		Size: 9.1 MB (9089815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2dace53b49bc6269a45ef43e083d81a14608d73ea6d87038589bbd5f3e38fd`  
		Last Modified: Mon, 31 Oct 2022 17:48:58 GMT  
		Size: 609.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2de3cdd92c64b14780fd8206db6fb04b4e3bab0bc0d0f0504babd19d51ae9c`  
		Last Modified: Mon, 31 Oct 2022 17:49:58 GMT  
		Size: 3.1 MB (3096577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69945cfd1d2192f8bf9360bfc44c50c2e601fd4c3ad707b96f108ae54a042d41`  
		Last Modified: Mon, 31 Oct 2022 17:49:57 GMT  
		Size: 3.6 KB (3624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da44409004eadb85095a5fb23bf5f0a376a53dfb0c81181d7a5bf03731c06eec`  
		Last Modified: Mon, 31 Oct 2022 17:49:57 GMT  
		Size: 918.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:694bfdba0d06912031311df198a2e7ccb52473a479e6270bfc5a73f2d66aad94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44331478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1aa855111bebae9c50dd254c314b5d79f445d088e65987f3e64ecdd832a126d`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
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
# Fri, 07 Oct 2022 01:34:56 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 07 Oct 2022 01:34:56 GMT
ENV PHP_VERSION=7.4.32
# Fri, 07 Oct 2022 01:34:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.32.tar.xz.asc
# Fri, 07 Oct 2022 01:34:57 GMT
ENV PHP_SHA256=323332c991e8ef30b1d219cb10f5e30f11b5f319ce4c6642a5470d75ade7864a
# Fri, 07 Oct 2022 01:35:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 07 Oct 2022 01:35:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 07 Oct 2022 01:44:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 07 Oct 2022 01:44:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 07 Oct 2022 01:44:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 07 Oct 2022 01:44:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Oct 2022 01:44:54 GMT
WORKDIR /var/www/html
# Fri, 07 Oct 2022 01:44:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 07 Oct 2022 01:44:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Oct 2022 01:44:56 GMT
EXPOSE 9000
# Fri, 07 Oct 2022 01:44:57 GMT
CMD ["php-fpm"]
# Fri, 07 Oct 2022 09:36:21 GMT
RUN set -ex;     apk add --no-cache         rsync         msmtp         shadow         tini;
# Fri, 07 Oct 2022 09:36:22 GMT
ENV GOSU_VERSION=1.14
# Fri, 07 Oct 2022 09:36:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Mon, 31 Oct 2022 18:30:19 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev         gmp-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap         gmp     ;         pecl install APCu-5.1.22;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Mon, 31 Oct 2022 18:30:20 GMT
ENV PHP_MEMORY_LIMIT=512M
# Mon, 31 Oct 2022 18:30:20 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Mon, 31 Oct 2022 18:30:21 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Mon, 31 Oct 2022 18:30:22 GMT
VOLUME [/var/www/html]
# Mon, 31 Oct 2022 18:30:22 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Mon, 31 Oct 2022 18:31:35 GMT
ENV FRIENDICA_VERSION=2022.12-dev
# Mon, 31 Oct 2022 18:31:35 GMT
ENV FRIENDICA_ADDONS=2022.12-dev
# Mon, 31 Oct 2022 18:31:38 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;
# Mon, 31 Oct 2022 18:31:39 GMT
COPY multi:f87d330cfcee641708f831c1e9357b18f2b0ed18bc7541fec914e00a972d58a1 in / 
# Mon, 31 Oct 2022 18:31:39 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Mon, 31 Oct 2022 18:31:40 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Mon, 31 Oct 2022 18:31:40 GMT
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
	-	`sha256:902409380edaa04602248d9c49d41571378d3196cd8040bf8b27c21e81b29f31`  
		Last Modified: Fri, 07 Oct 2022 02:22:37 GMT  
		Size: 10.4 MB (10439222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd07f10b3863003712c8d2dd5ca481cb2dfbfa47a99118bb064b9dc110918a02`  
		Last Modified: Fri, 07 Oct 2022 02:22:36 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4534151d08c09decc2d3855974916f7c6c3f7655027c63e94466dc155a32874`  
		Last Modified: Fri, 07 Oct 2022 02:23:34 GMT  
		Size: 12.2 MB (12218160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3753da4da74febf8788b8a76d49a3a96a87f400afbf47b6f504a8235e5e8c12b`  
		Last Modified: Fri, 07 Oct 2022 02:23:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015e138157a7ded140b725117cc3eca053e10d946744d49cb14e2b5144ce74c8`  
		Last Modified: Fri, 07 Oct 2022 02:23:31 GMT  
		Size: 18.6 KB (18623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dc66123967f9bbc1000db8a8e2579862b594957d0a86fe3c12642f86571566`  
		Last Modified: Fri, 07 Oct 2022 02:23:31 GMT  
		Size: 8.4 KB (8442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720554dcba827c38b7ab9da2c213fc14ef6405741169b72c78b8373978ff8358`  
		Last Modified: Fri, 07 Oct 2022 09:45:58 GMT  
		Size: 4.1 MB (4104493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8860f1da879bd4fb64393707f3294752d740a9f6a4089b7c15996142e9d67eb`  
		Last Modified: Fri, 07 Oct 2022 09:45:57 GMT  
		Size: 857.3 KB (857261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51202b92c842702d4291be39097fe9231eb09f1ec08e36c87fad3ca03a2350a9`  
		Last Modified: Mon, 31 Oct 2022 18:33:44 GMT  
		Size: 9.1 MB (9072569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea539dd22d434f7f00f64956d6e39a2ec809da9e5cce92776b5041aa6f324b41`  
		Last Modified: Mon, 31 Oct 2022 18:33:41 GMT  
		Size: 638.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439b4baccad7bd22e159faa854cc17f3fd539730a08626a9d97f33f454228a48`  
		Last Modified: Mon, 31 Oct 2022 18:34:51 GMT  
		Size: 3.0 MB (3027408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3800a3ba11132d0d5cf05963f037660ee69039ad382eb2d36e4599cde33461`  
		Last Modified: Mon, 31 Oct 2022 18:34:50 GMT  
		Size: 3.6 KB (3624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1169b979e3abac32ce0358654e6d052d5757f77b4274846a8ee3f65aaf7754a6`  
		Last Modified: Mon, 31 Oct 2022 18:34:50 GMT  
		Size: 947.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
