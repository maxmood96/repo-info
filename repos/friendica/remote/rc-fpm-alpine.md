## `friendica:rc-fpm-alpine`

```console
$ docker pull friendica@sha256:88176d739e3410d0d93ebfeb8a4dbe75242b76cd121fc3c022a2758b7bb90dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `friendica:rc-fpm-alpine` - linux; amd64

```console
$ docker pull friendica@sha256:8316fe51be95d3c44597e9023c6ba4f76c031825bd4e7763c7353066fb15ab4f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43061724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816bb17069da6266c3427a3ee1a634b18c594be53f2602b2e17cecc3ebb69a2c`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 May 2022 19:19:30 GMT
ADD file:8e81116368669ed3dd361bc898d61bff249f524139a239fdaf3ec46869a39921 in / 
# Mon, 23 May 2022 19:19:31 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 19:48:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 May 2022 19:48:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 25 May 2022 19:48:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 May 2022 19:48:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 May 2022 19:48:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 25 May 2022 19:48:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 19:48:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 19:48:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 May 2022 20:13:28 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 25 May 2022 20:13:28 GMT
ENV PHP_VERSION=7.4.29
# Wed, 25 May 2022 20:13:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.29.tar.xz.asc
# Wed, 25 May 2022 20:13:28 GMT
ENV PHP_SHA256=7d0f07869f33311ff3fe1138dc0d6c0d673c37fcb737eaed2c6c10a949f1aed6
# Wed, 25 May 2022 20:13:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 May 2022 20:13:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 May 2022 20:20:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 May 2022 20:20:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 25 May 2022 20:20:36 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 May 2022 20:20:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 May 2022 20:20:36 GMT
WORKDIR /var/www/html
# Wed, 25 May 2022 20:20:37 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 25 May 2022 20:20:37 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 20:20:37 GMT
EXPOSE 9000
# Wed, 25 May 2022 20:20:37 GMT
CMD ["php-fpm"]
# Wed, 25 May 2022 23:53:05 GMT
RUN set -ex;     apk add --no-cache         rsync         msmtp         shadow         tini;
# Wed, 25 May 2022 23:53:06 GMT
ENV GOSU_VERSION=1.14
# Wed, 25 May 2022 23:53:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Wed, 25 May 2022 23:54:57 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Wed, 25 May 2022 23:54:57 GMT
ENV PHP_MEMORY_LIMIT=512M
# Wed, 25 May 2022 23:54:57 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Wed, 25 May 2022 23:54:58 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Wed, 25 May 2022 23:54:58 GMT
VOLUME [/var/www/html]
# Wed, 25 May 2022 23:54:58 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Wed, 25 May 2022 23:56:29 GMT
ENV FRIENDICA_VERSION=2022.05-rc
# Wed, 25 May 2022 23:56:29 GMT
ENV FRIENDICA_ADDONS=2022.05-rc
# Wed, 25 May 2022 23:56:32 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;
# Wed, 25 May 2022 23:56:32 GMT
COPY multi:505a567dd8f292b590b99a423591dc3d4e2e3b8210cca89d51e9b207c9128e37 in / 
# Wed, 25 May 2022 23:56:32 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Wed, 25 May 2022 23:56:32 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Wed, 25 May 2022 23:56:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2408cc74d12b6cd092bb8b516ba7d5e290f485d3eb9672efc00f0583730179e8`  
		Last Modified: Mon, 23 May 2022 19:09:38 GMT  
		Size: 2.8 MB (2798889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde5ea1cb188409ac6276c7e55f3a6f6b0dfe9e3bd72711881e32183f03e8d99`  
		Last Modified: Wed, 25 May 2022 20:28:12 GMT  
		Size: 1.7 MB (1704858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3935ba60366aecf1bc3d1f0c663cb07711d490232ffa0ddde876eb4ebc40e469`  
		Last Modified: Wed, 25 May 2022 20:28:11 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4712e34f1d293d5afd1871939afc2d84d672bf03d6c4ef9c9558c720f40e5195`  
		Last Modified: Wed, 25 May 2022 20:28:11 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38485f657c58ee91f6c189b3bdea5474a8b422a345a873d02f1396365d89661e`  
		Last Modified: Wed, 25 May 2022 20:31:43 GMT  
		Size: 10.4 MB (10438817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a057edf730b8f519da35397ff5ac709dcf1510cb864654b4b01027aa7a800`  
		Last Modified: Wed, 25 May 2022 20:31:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a807c9e52ca2fa74c8e47488491871e72349e2d9eede098686df8a3c1d3436`  
		Last Modified: Wed, 25 May 2022 20:32:24 GMT  
		Size: 11.5 MB (11456109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739d534fe3d2562599fd67e81bd7a08fb68730961265104663ff3e4282813204`  
		Last Modified: Wed, 25 May 2022 20:32:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bbf04586c85ad49f30a1723bfed8282119a852d09ec742810d62527f2574c6`  
		Last Modified: Wed, 25 May 2022 20:32:22 GMT  
		Size: 18.4 KB (18361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a5c3c60b568f02c603d4af0daea625842e819f74cab44015714f61a2387a28`  
		Last Modified: Wed, 25 May 2022 20:32:22 GMT  
		Size: 8.4 KB (8444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac159542f343db425fe657d0fe7bf06f817cbfb6bbab99516bdd41a94434eca`  
		Last Modified: Wed, 25 May 2022 23:57:16 GMT  
		Size: 4.0 MB (3986393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85eea7fa87d56cb0c9bdd6ee67a09a11766e7564991e40169f16be16817725a`  
		Last Modified: Wed, 25 May 2022 23:57:15 GMT  
		Size: 956.1 KB (956098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe0d0b78af63641402994ff5c5f184d3c2d80586725ed6d4e9ffb3af0d7f942`  
		Last Modified: Wed, 25 May 2022 23:57:14 GMT  
		Size: 8.8 MB (8816289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cf1e6749b82a677fc223f07d949f9c8a09f821d5320985cbc3fa99b0d389a5`  
		Last Modified: Wed, 25 May 2022 23:57:13 GMT  
		Size: 634.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09546d6ccb5cc30220a286b98148f8b6924579ba9b0f6176f93238e4e37b19a`  
		Last Modified: Wed, 25 May 2022 23:58:18 GMT  
		Size: 2.9 MB (2867832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891653c3ac6d2cb0adfea83f22a0129a550bad50b466dc70b6afb26ecd0cbbed`  
		Last Modified: Wed, 25 May 2022 23:58:18 GMT  
		Size: 3.6 KB (3587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6912319f578b53e224e097b7bacda47b92b44e11b3df374653f409c4ffddfa09`  
		Last Modified: Wed, 25 May 2022 23:58:18 GMT  
		Size: 946.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm-alpine` - linux; arm variant v6

```console
$ docker pull friendica@sha256:1301ac1415fdf21326dec78f453a7aa849a798dc75d051e2e310d3453c361bdc
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41368171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247fc860b561cfb3c41c71cd368289d220c8817e5cc80aed106f1146682e30e5`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 May 2022 19:49:32 GMT
ADD file:f7cee617575b5e5a7672d298a519bb8d8b5098efb90aa2a5d7b0510003457d52 in / 
# Mon, 23 May 2022 19:49:33 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 21:50:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 May 2022 21:50:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 25 May 2022 21:50:08 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 May 2022 21:50:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 May 2022 21:50:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 25 May 2022 21:50:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 21:50:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 21:50:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 May 2022 22:22:58 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 25 May 2022 22:22:58 GMT
ENV PHP_VERSION=7.4.29
# Wed, 25 May 2022 22:22:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.29.tar.xz.asc
# Wed, 25 May 2022 22:22:59 GMT
ENV PHP_SHA256=7d0f07869f33311ff3fe1138dc0d6c0d673c37fcb737eaed2c6c10a949f1aed6
# Wed, 25 May 2022 22:23:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 May 2022 22:23:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 May 2022 22:33:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 May 2022 22:33:11 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 25 May 2022 22:33:14 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 May 2022 22:33:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 May 2022 22:33:15 GMT
WORKDIR /var/www/html
# Wed, 25 May 2022 22:33:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 25 May 2022 22:33:16 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 22:33:17 GMT
EXPOSE 9000
# Wed, 25 May 2022 22:33:17 GMT
CMD ["php-fpm"]
# Thu, 26 May 2022 02:46:30 GMT
RUN set -ex;     apk add --no-cache         rsync         msmtp         shadow         tini;
# Thu, 26 May 2022 02:46:30 GMT
ENV GOSU_VERSION=1.14
# Thu, 26 May 2022 02:46:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 26 May 2022 02:51:29 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Thu, 26 May 2022 02:51:30 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 May 2022 02:51:30 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 May 2022 02:51:31 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 26 May 2022 02:51:32 GMT
VOLUME [/var/www/html]
# Thu, 26 May 2022 02:51:32 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 May 2022 02:54:10 GMT
ENV FRIENDICA_VERSION=2022.05-rc
# Thu, 26 May 2022 02:54:11 GMT
ENV FRIENDICA_ADDONS=2022.05-rc
# Thu, 26 May 2022 02:54:14 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;
# Thu, 26 May 2022 02:54:15 GMT
COPY multi:505a567dd8f292b590b99a423591dc3d4e2e3b8210cca89d51e9b207c9128e37 in / 
# Thu, 26 May 2022 02:54:16 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Thu, 26 May 2022 02:54:16 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 May 2022 02:54:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:79a25ccaf940855872635c06e7614d9b27dd38ffb5a8adfdb9274dfdc0ea0d87`  
		Last Modified: Mon, 23 May 2022 19:08:47 GMT  
		Size: 2.6 MB (2606142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e7eae6d0293087d982d321125f6f132894675f6acb732427528058758d6ae3`  
		Last Modified: Wed, 25 May 2022 22:46:23 GMT  
		Size: 1.7 MB (1693282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ad96c7e3fdd13c53c906a10fab89b0dc599bf1746acd163f9648f8f9ec949de`  
		Last Modified: Wed, 25 May 2022 22:46:21 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1acccbd45290b92307c479937198ace1c187e0fd49d5e1ea72c1f5d7d5e1705`  
		Last Modified: Wed, 25 May 2022 22:46:21 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565e6f0900611b82fca2264581cfa8cd1be132fce451e14c0dd3414e84fd65cc`  
		Last Modified: Wed, 25 May 2022 22:51:15 GMT  
		Size: 10.4 MB (10438819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2729e4e3fa668bd502bc0816e52da82193f24ea9256236c8407d0b3fdc909e59`  
		Last Modified: Wed, 25 May 2022 22:51:12 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b816feba81971f4e8c5f26ed963acd42caa8c2daf9fe23f80b31e48f1aa02d57`  
		Last Modified: Wed, 25 May 2022 22:52:22 GMT  
		Size: 10.7 MB (10723463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:732702e5498a6706fc797b8ea7c56ad1cb8ebc205c115b498fb3bedc70549da8`  
		Last Modified: Wed, 25 May 2022 22:52:14 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a089c3391facba55e8eca3ecd62d47e6f46d715e09148791056ff9a12af51cf8`  
		Last Modified: Wed, 25 May 2022 22:52:14 GMT  
		Size: 18.4 KB (18364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147e0b4dfb4264cb1e96a5c4d81da9ffe20edefc2fbafd5a2f91bbe0ba9bb037`  
		Last Modified: Wed, 25 May 2022 22:52:14 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87dbaf4ff0d845caff2ba9fc016555040a41a4593a4e938e41b3a7d92bf1ff1`  
		Last Modified: Thu, 26 May 2022 02:55:12 GMT  
		Size: 3.9 MB (3870385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b31065d310e51d5bfb706609a063b93d52051babe3c398bffdef89209561ea57`  
		Last Modified: Thu, 26 May 2022 02:55:10 GMT  
		Size: 910.8 KB (910832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c984f4d46e6176a8c2f2f18e9d159ca2b64e34301e22dadb8d893701d94cb4a`  
		Last Modified: Thu, 26 May 2022 02:55:13 GMT  
		Size: 8.4 MB (8380614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16390208aae2ad1f5de730765f988789072f53ac787ec8ea47c19008e3a1da8`  
		Last Modified: Thu, 26 May 2022 02:55:08 GMT  
		Size: 633.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1a6930488b38ab963ab02721d86f4b778ec0fd99386a8dd4d31dab947a12c2`  
		Last Modified: Thu, 26 May 2022 02:57:29 GMT  
		Size: 2.7 MB (2708189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b7a193de2f5ff1da91fe409c441eba1c6e77d963e0a918ba08b1efb0c1745d`  
		Last Modified: Thu, 26 May 2022 02:57:27 GMT  
		Size: 3.6 KB (3590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d1340dbc19191898e825ef2fb3554cefb00a173cc8d8b1353cb1f64a7335b4`  
		Last Modified: Thu, 26 May 2022 02:57:27 GMT  
		Size: 945.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm-alpine` - linux; arm variant v7

```console
$ docker pull friendica@sha256:66011250997fe1195b54f54f9ab8691ed72a80e1d33108a26c5f9f73e9e3e909
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39426286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b427287308be41ae870b120268fe0ecba829cb92b7a3deab585bd6a052a7cf5f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 May 2022 18:57:46 GMT
ADD file:72698cc08524b911ebaacf992490707e5a951ddd2fe6edb3fb598e9dc7155049 in / 
# Mon, 23 May 2022 18:57:47 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 19:01:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 May 2022 19:01:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 25 May 2022 19:01:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 May 2022 19:01:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 May 2022 19:01:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 25 May 2022 19:01:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 19:01:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 19:01:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 May 2022 19:36:20 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 25 May 2022 19:36:20 GMT
ENV PHP_VERSION=7.4.29
# Wed, 25 May 2022 19:36:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.29.tar.xz.asc
# Wed, 25 May 2022 19:36:21 GMT
ENV PHP_SHA256=7d0f07869f33311ff3fe1138dc0d6c0d673c37fcb737eaed2c6c10a949f1aed6
# Wed, 25 May 2022 19:36:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 May 2022 19:36:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 May 2022 19:46:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 May 2022 19:46:05 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 25 May 2022 19:46:07 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 May 2022 19:46:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 May 2022 19:46:08 GMT
WORKDIR /var/www/html
# Wed, 25 May 2022 19:46:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 25 May 2022 19:46:10 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 19:46:11 GMT
EXPOSE 9000
# Wed, 25 May 2022 19:46:11 GMT
CMD ["php-fpm"]
# Thu, 26 May 2022 03:15:05 GMT
RUN set -ex;     apk add --no-cache         rsync         msmtp         shadow         tini;
# Thu, 26 May 2022 03:15:05 GMT
ENV GOSU_VERSION=1.14
# Thu, 26 May 2022 03:15:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 26 May 2022 03:19:50 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Thu, 26 May 2022 03:19:51 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 May 2022 03:19:51 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 May 2022 03:19:53 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 26 May 2022 03:19:53 GMT
VOLUME [/var/www/html]
# Thu, 26 May 2022 03:19:53 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 May 2022 03:23:52 GMT
ENV FRIENDICA_VERSION=2022.05-rc
# Thu, 26 May 2022 03:23:52 GMT
ENV FRIENDICA_ADDONS=2022.05-rc
# Thu, 26 May 2022 03:23:55 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;
# Thu, 26 May 2022 03:23:56 GMT
COPY multi:505a567dd8f292b590b99a423591dc3d4e2e3b8210cca89d51e9b207c9128e37 in / 
# Thu, 26 May 2022 03:23:57 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Thu, 26 May 2022 03:23:57 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 May 2022 03:23:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6366ba92f08e2418e90171f1e34bd86ecd50fdc95953b3f33b8943c143518eca`  
		Last Modified: Mon, 23 May 2022 18:59:17 GMT  
		Size: 2.4 MB (2411648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68c4c667bd6865eca9aa9f496ecc527223b3162b260cad2e40c45ad49edc479`  
		Last Modified: Wed, 25 May 2022 20:09:19 GMT  
		Size: 1.6 MB (1560829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6bb9188dd796f59353a38be6412d00920f7c1da1effa359dc5c9a5724c0fb0`  
		Last Modified: Wed, 25 May 2022 20:09:18 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbde557014a2ec2c7a2e22a836cdf6978cf4aaea9b738859980a1d98c9b1282`  
		Last Modified: Wed, 25 May 2022 20:09:18 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02954cc670b8f5240fd2c85d77660674e7b2b47ed0fd55e4b5f967b7020fa768`  
		Last Modified: Wed, 25 May 2022 20:15:58 GMT  
		Size: 10.4 MB (10438808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61272aa02c2af4b15db30085c8e6ca18d250a7d5f61a21118e6e12413420d940`  
		Last Modified: Wed, 25 May 2022 20:15:56 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bc9cdf26b7873e8dcae3795c8b5c051569822a35c3065c7359843c0197e36`  
		Last Modified: Wed, 25 May 2022 20:17:03 GMT  
		Size: 10.1 MB (10089758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d64db602bc2640a74d8e1d596834e697242912a29f8b2d4045522961c6fbea1`  
		Last Modified: Wed, 25 May 2022 20:16:56 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922690085ee34bb8ef6468d2232dec76fe98c0c9000e25f8468aa3259e9102f2`  
		Last Modified: Wed, 25 May 2022 20:16:56 GMT  
		Size: 18.3 KB (18335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca53ed35885b2d353e752bfc5f0cb6cbe18e6133cd599dbb4e8a48e055283427`  
		Last Modified: Wed, 25 May 2022 20:16:56 GMT  
		Size: 8.4 KB (8447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321a4ba589f1e597ad472d26866bd7e19fcf52283f29e3263b22d2b872006e73`  
		Last Modified: Thu, 26 May 2022 03:26:42 GMT  
		Size: 3.6 MB (3589659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a760056f558e501fd170e69d3af06c97932eb84dd8d26489be356a4726bedd44`  
		Last Modified: Thu, 26 May 2022 03:26:41 GMT  
		Size: 910.8 KB (910812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9ec271a1e7d0a8ffb08d59d219c8cc5f5355ee5600ab73a8affebf946ef230`  
		Last Modified: Thu, 26 May 2022 03:26:43 GMT  
		Size: 8.0 MB (7961815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee4b6b94b3bf40e34e64dc1f7862b2287b28d7757ebdf3b5580d77684a649fd`  
		Last Modified: Thu, 26 May 2022 03:26:39 GMT  
		Size: 636.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610b778e88acafbe89c47c4e7b262c80f78b0aaecd0af7079658c75cd5408386`  
		Last Modified: Thu, 26 May 2022 03:29:33 GMT  
		Size: 2.4 MB (2426528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788aead7f0e07e50d64ad2155e09821168dbd836f9c8948a5170d62ea7702d4`  
		Last Modified: Thu, 26 May 2022 03:29:32 GMT  
		Size: 3.6 KB (3587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63068aaacd64ce674e6a6767740435a27f7521c14b1425594054a25d2bb71ce2`  
		Last Modified: Thu, 26 May 2022 03:29:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:77c498f1cb39f492ce8ae126ed70f730b1d25cbb961c882bf581a3b92e72ce27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42301239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e8f709504ddf1173d3c3b4cfd60e1f92d4504555a271ae1e12d973ac51c84f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 May 2022 19:39:22 GMT
ADD file:3ae36c6c4a1fc43157692da97c6c4fa6c3d0189ba82e2bef7f5aaf4a5e083f18 in / 
# Mon, 23 May 2022 19:39:22 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 20:06:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 May 2022 20:06:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 25 May 2022 20:06:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 May 2022 20:06:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 May 2022 20:06:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 25 May 2022 20:06:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 20:06:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 20:06:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 May 2022 21:02:56 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 25 May 2022 21:02:56 GMT
ENV PHP_VERSION=7.4.29
# Wed, 25 May 2022 21:02:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.29.tar.xz.asc
# Wed, 25 May 2022 21:02:58 GMT
ENV PHP_SHA256=7d0f07869f33311ff3fe1138dc0d6c0d673c37fcb737eaed2c6c10a949f1aed6
# Wed, 25 May 2022 21:03:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 May 2022 21:03:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 May 2022 21:15:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 May 2022 21:15:15 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 25 May 2022 21:15:15 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 May 2022 21:15:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 May 2022 21:15:17 GMT
WORKDIR /var/www/html
# Wed, 25 May 2022 21:15:18 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 25 May 2022 21:15:19 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 21:15:20 GMT
EXPOSE 9000
# Wed, 25 May 2022 21:15:21 GMT
CMD ["php-fpm"]
# Thu, 26 May 2022 00:45:18 GMT
RUN set -ex;     apk add --no-cache         rsync         msmtp         shadow         tini;
# Thu, 26 May 2022 00:45:18 GMT
ENV GOSU_VERSION=1.14
# Thu, 26 May 2022 00:45:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 26 May 2022 00:47:24 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Thu, 26 May 2022 00:47:24 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 May 2022 00:47:25 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 May 2022 00:47:26 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 26 May 2022 00:47:27 GMT
VOLUME [/var/www/html]
# Thu, 26 May 2022 00:47:28 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 May 2022 00:49:50 GMT
ENV FRIENDICA_VERSION=2022.05-rc
# Thu, 26 May 2022 00:49:51 GMT
ENV FRIENDICA_ADDONS=2022.05-rc
# Thu, 26 May 2022 00:49:53 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;
# Thu, 26 May 2022 00:49:55 GMT
COPY multi:505a567dd8f292b590b99a423591dc3d4e2e3b8210cca89d51e9b207c9128e37 in / 
# Thu, 26 May 2022 00:49:56 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Thu, 26 May 2022 00:49:56 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 May 2022 00:49:57 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b3c136eddcbf2003d3180787cef00f39d46b9fd9e4623178282ad6a8d63ad3b0`  
		Last Modified: Mon, 23 May 2022 19:08:34 GMT  
		Size: 2.7 MB (2694464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a240d0a51bf6100803c8ce9f1ce769377fd09a2824a580ad991fb1a8a64610`  
		Last Modified: Wed, 25 May 2022 21:26:48 GMT  
		Size: 1.7 MB (1703255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d989eb157716fb2e84408b95764324504b7dd9aac628dd9a66a7f15eeb43a66`  
		Last Modified: Wed, 25 May 2022 21:26:48 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940028d0e55a77f4d9df2de18c1a76fa1058bdb66dee66fa6309f9337e500d6e`  
		Last Modified: Wed, 25 May 2022 21:26:48 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79204fbd3f89c75048ba1f710c653426630d4f42fe5c43440ade502f24df49a`  
		Last Modified: Wed, 25 May 2022 21:31:03 GMT  
		Size: 10.4 MB (10438582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ef3bf440ec26105084aed8908902a0536f16fd590a7db56fc1cc32802b4007`  
		Last Modified: Wed, 25 May 2022 21:31:02 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c428a2c9f0656f509527ad7cda74d6da82f5beb7a26b676223dabd239105e8`  
		Last Modified: Wed, 25 May 2022 21:31:48 GMT  
		Size: 11.3 MB (11284103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb69e98fda850c8e4ff1c67afdc455eea522d087fae14f3930ef222089f62c6`  
		Last Modified: Wed, 25 May 2022 21:31:46 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039937e24cc43eb48fb4bf0901d45bd7a89e534f43cf567158b8ffd308f7992a`  
		Last Modified: Wed, 25 May 2022 21:31:46 GMT  
		Size: 18.3 KB (18253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7c5fa133d62d63605d9307c3159f95e4b407536d6fdf65b89a286ea4ff4c2f`  
		Last Modified: Wed, 25 May 2022 21:31:47 GMT  
		Size: 8.4 KB (8440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f74dc1b46a0cbcb441889e0105a2fb806b28afa6afedc912f2e0887f42f7901a`  
		Last Modified: Thu, 26 May 2022 00:51:14 GMT  
		Size: 3.9 MB (3890882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb29d3accefbd4fe892aad86b213f93ff083ec1ace35b6a7b302e1694f45ebe`  
		Last Modified: Thu, 26 May 2022 00:51:13 GMT  
		Size: 881.9 KB (881942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b077a6e5747938bc0760b8b25c9ea6c11b21ca1778f9672851c97be7c83833d3`  
		Last Modified: Thu, 26 May 2022 00:51:12 GMT  
		Size: 8.6 MB (8577727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3683ea9fad16ef5978fb2541de9772a27f4f1e20e580085a3d8d8bb8d0caabd1`  
		Last Modified: Thu, 26 May 2022 00:51:11 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fbd15ece35f944f02698d4740b3d88aae2f1553e79df9715eb5ee8e1130784`  
		Last Modified: Thu, 26 May 2022 00:52:33 GMT  
		Size: 2.8 MB (2794086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dccf19f4f1b6aeb410b8f237d7200045f6d97fb33decd0134adcc8fcc3aea8b0`  
		Last Modified: Thu, 26 May 2022 00:52:33 GMT  
		Size: 3.6 KB (3590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d836a5e8ae41c10652926fcb0d43d3998e523f10cbce48577c911212999c25`  
		Last Modified: Thu, 26 May 2022 00:52:33 GMT  
		Size: 915.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm-alpine` - linux; 386

```console
$ docker pull friendica@sha256:a48ab7f8d49e2855a56e97b464e78aa9d4024e694984ea9dcccd41cfd663c79e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (43983734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987b8a403078dd6b9814461d081dadb739c3d2d62d9c2aa6c09049431cb4bc05`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 May 2022 19:38:20 GMT
ADD file:1750ccfabfe93636015070d51a6e824cbd738056223421c69d8aaabc38041b18 in / 
# Mon, 23 May 2022 19:38:20 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 19:56:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 May 2022 19:56:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 25 May 2022 19:56:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 May 2022 19:56:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 May 2022 19:56:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 25 May 2022 19:56:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 19:56:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 19:56:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 May 2022 20:23:45 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 25 May 2022 20:23:46 GMT
ENV PHP_VERSION=7.4.29
# Wed, 25 May 2022 20:23:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.29.tar.xz.asc
# Wed, 25 May 2022 20:23:48 GMT
ENV PHP_SHA256=7d0f07869f33311ff3fe1138dc0d6c0d673c37fcb737eaed2c6c10a949f1aed6
# Wed, 25 May 2022 20:23:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 May 2022 20:23:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 May 2022 20:31:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 May 2022 20:31:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 25 May 2022 20:31:14 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 May 2022 20:31:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 May 2022 20:31:16 GMT
WORKDIR /var/www/html
# Wed, 25 May 2022 20:31:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 25 May 2022 20:31:18 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 20:31:19 GMT
EXPOSE 9000
# Wed, 25 May 2022 20:31:20 GMT
CMD ["php-fpm"]
# Thu, 26 May 2022 00:12:18 GMT
RUN set -ex;     apk add --no-cache         rsync         msmtp         shadow         tini;
# Thu, 26 May 2022 00:12:19 GMT
ENV GOSU_VERSION=1.14
# Thu, 26 May 2022 00:12:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 26 May 2022 00:14:15 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Thu, 26 May 2022 00:14:15 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 May 2022 00:14:16 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 May 2022 00:14:17 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 26 May 2022 00:14:18 GMT
VOLUME [/var/www/html]
# Thu, 26 May 2022 00:14:19 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 May 2022 00:16:43 GMT
ENV FRIENDICA_VERSION=2022.05-rc
# Thu, 26 May 2022 00:16:44 GMT
ENV FRIENDICA_ADDONS=2022.05-rc
# Thu, 26 May 2022 00:16:46 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;
# Thu, 26 May 2022 00:16:48 GMT
COPY multi:505a567dd8f292b590b99a423591dc3d4e2e3b8210cca89d51e9b207c9128e37 in / 
# Thu, 26 May 2022 00:16:49 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Thu, 26 May 2022 00:16:49 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 May 2022 00:16:50 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bb638a3869eed698f88775c7a48f36f8e22e7c6bbaa98fa1d5678966b619b859`  
		Last Modified: Mon, 23 May 2022 19:09:25 GMT  
		Size: 2.8 MB (2801887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97eb700ff81c1dbea3f8e204a809be7b7431ba817b16c87c1efe84972e2fe6c1`  
		Last Modified: Wed, 25 May 2022 20:43:18 GMT  
		Size: 1.8 MB (1807504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaabb95698f746340e8771d50f4e356e03ad67347638c9d30dc7d3d7cdb3359`  
		Last Modified: Wed, 25 May 2022 20:43:18 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f127678bc84e9717b47e929fd82c70e9bc39b96e731eb561d466d4373561cd1`  
		Last Modified: Wed, 25 May 2022 20:43:17 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da884c158fed7b912ee52594f4f88d3eafe6744a7e66904b6bc4f57e59306c06`  
		Last Modified: Wed, 25 May 2022 20:47:44 GMT  
		Size: 10.4 MB (10438567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9802c8814d43788b8b51cc934a29da5fdbeff14e342219f19c0b84f875d15c`  
		Last Modified: Wed, 25 May 2022 20:47:41 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4074de331469ea4bbf9f3d265aa54ef345ff3b93324d009558f6a395fe4d8710`  
		Last Modified: Wed, 25 May 2022 20:48:28 GMT  
		Size: 11.8 MB (11764487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09af158595ec60196fd004aa8b29063b9b5e472c492ac77a767b40441c4589d8`  
		Last Modified: Wed, 25 May 2022 20:48:26 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c2674c8c0fc6ec334dca9d4a16523139c87fee4dff4a72516f8a511099a637`  
		Last Modified: Wed, 25 May 2022 20:48:26 GMT  
		Size: 18.3 KB (18258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a234743a1f339033602f97a5278a786870f674985c4972a678030af976345b64`  
		Last Modified: Wed, 25 May 2022 20:48:27 GMT  
		Size: 8.4 KB (8440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d13cccbf362d1bd454409f408502ac60e73dc931b669f103ede578660756ad`  
		Last Modified: Thu, 26 May 2022 00:18:09 GMT  
		Size: 4.1 MB (4057490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cf8c45b3f505e360175c2aa980882c6aac987967a57794223697df6dab5fce`  
		Last Modified: Thu, 26 May 2022 00:18:08 GMT  
		Size: 922.6 KB (922551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0542294a96cd69ee3780b742b2d1c29793fe8acafcf3fb2807e3189bef6667`  
		Last Modified: Thu, 26 May 2022 00:18:07 GMT  
		Size: 9.1 MB (9058149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b26df885036dbbe982e8ef20311c9433b7f6c526bd97f7e75fe697827065ca`  
		Last Modified: Thu, 26 May 2022 00:18:06 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfe6ed1a5fb26922c97c68cc5b5030bbc01e3fd59100497ebcd7b80402cfa84`  
		Last Modified: Thu, 26 May 2022 00:19:35 GMT  
		Size: 3.1 MB (3096898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3d4f2ee269604e41b249c4cb497a0098619919474295617ecec1b2c2b859c5`  
		Last Modified: Thu, 26 May 2022 00:19:34 GMT  
		Size: 3.6 KB (3587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0657e3289e2a7bc950dffbce667395baaf011d3d6d1715c54049d9a7480e7bf9`  
		Last Modified: Thu, 26 May 2022 00:19:34 GMT  
		Size: 918.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:rc-fpm-alpine` - linux; ppc64le

```console
$ docker pull friendica@sha256:77d035c1407d95efdfa80efc6498fa267675a800ad6b16995f16479a711fa420
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44267082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad613d5835d919301a020c04dd1ec9bf4eec667e6fecb6fad4498ec318f60054`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 23 May 2022 19:16:51 GMT
ADD file:6a5450c8a7cee3ceda59e7cb350c54df4139b0f7b7cf49c8b31bb9c01646c3cd in / 
# Mon, 23 May 2022 19:16:53 GMT
CMD ["/bin/sh"]
# Wed, 25 May 2022 19:57:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 25 May 2022 19:57:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 25 May 2022 19:57:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 25 May 2022 19:57:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 25 May 2022 19:57:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 25 May 2022 19:57:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 19:57:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 25 May 2022 19:57:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 25 May 2022 20:39:29 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Wed, 25 May 2022 20:39:33 GMT
ENV PHP_VERSION=7.4.29
# Wed, 25 May 2022 20:39:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.29.tar.xz.asc
# Wed, 25 May 2022 20:39:39 GMT
ENV PHP_SHA256=7d0f07869f33311ff3fe1138dc0d6c0d673c37fcb737eaed2c6c10a949f1aed6
# Wed, 25 May 2022 20:43:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 25 May 2022 20:43:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 25 May 2022 20:54:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 	ln -sv /usr/include/gnu-libiconv/*.h /usr/include/; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 25 May 2022 20:54:20 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 25 May 2022 20:54:27 GMT
RUN docker-php-ext-enable sodium
# Wed, 25 May 2022 20:54:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 25 May 2022 20:54:32 GMT
WORKDIR /var/www/html
# Wed, 25 May 2022 20:54:37 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 25 May 2022 20:54:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 May 2022 20:54:42 GMT
EXPOSE 9000
# Wed, 25 May 2022 20:54:45 GMT
CMD ["php-fpm"]
# Thu, 26 May 2022 03:52:05 GMT
RUN set -ex;     apk add --no-cache         rsync         msmtp         shadow         tini;
# Thu, 26 May 2022 03:52:11 GMT
ENV GOSU_VERSION=1.14
# Thu, 26 May 2022 03:52:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .gosu-deps 		ca-certificates 		dpkg 		gnupg 	; 		dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 		export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	command -v gpgconf && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 		apk del --no-network .gosu-deps; 		chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Thu, 26 May 2022 03:57:00 GMT
RUN set -ex;         apk add --no-cache --virtual .build-deps         mariadb-client         bash         $PHPIZE_DEPS         libpng-dev         libjpeg-turbo-dev         imagemagick-dev         libtool         libmemcached-dev         cyrus-sasl-dev         libjpeg-turbo-dev         freetype-dev         libwebp-dev         librsvg         pcre-dev         libzip-dev         icu-dev         openldap-dev     ;         docker-php-ext-configure gd         --with-freetype         --with-jpeg         --with-webp     ;         docker-php-ext-install -j "$(nproc)"         pdo_mysql         exif         gd         zip         opcache         pcntl         ldap     ;         pecl install APCu-5.1.21;     pecl install memcached-3.2.0RC2;     pecl install redis-5.3.7;     pecl install imagick-3.7.0;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         runDeps="$(         scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions             | tr ',' '\n'             | sort -u             | awk 'system("[ -e /usr/local/lib" $1 " ]") == 0 { next } { print "so:" $1 }'     )";     apk add --no-network --virtual .friendica-phpext-rundeps $runDeps;     apk del --no-network .build-deps;
# Thu, 26 May 2022 03:57:05 GMT
ENV PHP_MEMORY_LIMIT=512M
# Thu, 26 May 2022 03:57:10 GMT
ENV PHP_UPLOAD_LIMIT=512M
# Thu, 26 May 2022 03:57:22 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         {         echo 'memory_limit=${PHP_MEMORY_LIMIT}';         echo 'upload_max_filesize=${PHP_UPLOAD_LIMIT}';         echo 'post_max_size=${PHP_UPLOAD_LIMIT}';     } > /usr/local/etc/php/conf.d/friendica.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Thu, 26 May 2022 03:57:27 GMT
VOLUME [/var/www/html]
# Thu, 26 May 2022 03:57:32 GMT
ENV FRIENDICA_SYSLOG_FLAGS=39
# Thu, 26 May 2022 04:29:18 GMT
ENV FRIENDICA_VERSION=2022.05-rc
# Thu, 26 May 2022 04:29:26 GMT
ENV FRIENDICA_ADDONS=2022.05-rc
# Thu, 26 May 2022 04:29:42 GMT
RUN set -ex;      apk add --no-cache --virtual .fetch-deps             gnupg         ;
# Thu, 26 May 2022 04:29:45 GMT
COPY multi:505a567dd8f292b590b99a423591dc3d4e2e3b8210cca89d51e9b207c9128e37 in / 
# Thu, 26 May 2022 04:29:46 GMT
COPY multi:201dba5df7e408009a8882797a28095a47753a2db673a80c99e898e88501c42e in /usr/src/friendica/config/ 
# Thu, 26 May 2022 04:29:50 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Thu, 26 May 2022 04:29:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d3deabf2a506ef6f5fa7c2a68bf27047574cef9908b30a97ff2d01ae539b089a`  
		Last Modified: Mon, 23 May 2022 19:09:13 GMT  
		Size: 2.8 MB (2789745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1091cbad9101b41d3fd65de74d3265b02346722f13f77c4a456e33979dd226da`  
		Last Modified: Wed, 25 May 2022 21:08:36 GMT  
		Size: 1.8 MB (1759345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570e34510ef12ed73f2ed4ab7167c3408a7a0c69498928d0be0c6d46e2250ea3`  
		Last Modified: Wed, 25 May 2022 21:08:35 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcbd0bbe87c55d5c71424cd10832856ec6580b2de2bf35112f9a41f574cef70f`  
		Last Modified: Wed, 25 May 2022 21:08:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:782b33dbbd3bb1ce9d9a9f2c8631a1fb15a99edb0550457afb10267afa47b9f3`  
		Last Modified: Wed, 25 May 2022 21:13:20 GMT  
		Size: 10.4 MB (10438821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30069aee361914d9f9fd340a64b28541bdb4f5ba17c50a7bd07445e0f930a030`  
		Last Modified: Wed, 25 May 2022 21:13:19 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f779e4206091950579168e34b7c331b69389cfb6d7f4e9ad6551b4c635cba381`  
		Last Modified: Wed, 25 May 2022 21:14:13 GMT  
		Size: 12.2 MB (12216252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cb07921867d8afdb49f4d544e8570627e5e1823c48c67a86b7a3c8f62d49636`  
		Last Modified: Wed, 25 May 2022 21:14:11 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c732eca29eb26e2c5f38434403262d4e12de5433940641b4dcde22d9651c133`  
		Last Modified: Wed, 25 May 2022 21:14:11 GMT  
		Size: 18.3 KB (18347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85595200d280a23deb9d36dfd2923ba4a6ce9c8253d0be121912e316a78218cd`  
		Last Modified: Wed, 25 May 2022 21:14:11 GMT  
		Size: 8.4 KB (8443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656b845368c8c4e1efea1a778c593193add95c509a108d87dcc6453bb754731a`  
		Last Modified: Thu, 26 May 2022 04:31:28 GMT  
		Size: 4.1 MB (4100150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34db80bc44de6b8dd6e49e9833d4b252ec11459a1594a3f9933640e60aae193`  
		Last Modified: Thu, 26 May 2022 04:31:27 GMT  
		Size: 857.0 KB (856993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fa3bdc8b4b7524d5d0934fd92835a17aef73dea93244d6c2b6d7de9255db9b`  
		Last Modified: Thu, 26 May 2022 04:31:26 GMT  
		Size: 9.0 MB (9041743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfbdeaf578e4b2494ee44b4055ae75469069737e651f561e95a4d2b013831e3`  
		Last Modified: Thu, 26 May 2022 04:31:24 GMT  
		Size: 639.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d843b6a0c6208036254ee2affedfb89b0e00d4a3a22d602ab4bdbcc6224de0`  
		Last Modified: Thu, 26 May 2022 04:32:58 GMT  
		Size: 3.0 MB (3027587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ed66d9cbe1d60399e8696658a5d379c956d16d7db6821a679ee2a76bbd6f69`  
		Last Modified: Thu, 26 May 2022 04:32:57 GMT  
		Size: 3.6 KB (3587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f21d6c7600720e001d827de81d5bfb2da06062e968cff9391af5396f455ab928`  
		Last Modified: Thu, 26 May 2022 04:32:57 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
