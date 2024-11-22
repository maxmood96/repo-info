## `postfixadmin:fpm-alpine`

```console
$ docker pull postfixadmin@sha256:a5519f6d7f007bc45582c4979ced512fc8d9a0d1971b8a526cdc147679247bfd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `postfixadmin:fpm-alpine` - linux; amd64

```console
$ docker pull postfixadmin@sha256:42957ecd5a9004db91d2544bdfcbda2ac01e56b5f161d4b2826f6448bfdc7e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (36955612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52bfda1ed1a923d1b8ec12cc8de28e55200de8bcd9db90905f6615335fda0938`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 10 Nov 2023 16:38:27 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["/bin/sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Nov 2023 16:38:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_VERSION=8.1.31
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Nov 2023 16:38:27 GMT
WORKDIR /var/www/html
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Nov 2023 16:38:27 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
# Fri, 10 Nov 2023 16:38:27 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.13 POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d213cb6f35098fd4c620a84e1d005528ec8e7cb5739b129509ec9ad3ae254c69`  
		Last Modified: Thu, 21 Nov 2024 18:06:57 GMT  
		Size: 5.6 MB (5583580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa34f0068d1c975f894d11757883bb4df3f088907117157676cf9026a618e620`  
		Last Modified: Thu, 21 Nov 2024 18:06:57 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a8a4855290b28992553ed7da6a5b6cc136730295621f09ba8d9cd2f8416f00`  
		Last Modified: Thu, 21 Nov 2024 18:06:57 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab0c0477f7d054654efd4adfdb1b8ae89649b4247a0bdbe4fc7eaad8a508cba9`  
		Last Modified: Thu, 21 Nov 2024 18:06:57 GMT  
		Size: 11.9 MB (11937850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79b33c462e118ad49c81498b1f8bc2a173212c4455dbd7f94c0fc9985a28310`  
		Last Modified: Thu, 21 Nov 2024 18:06:57 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b1259e7ccc694e6076f2cb5ef68519d9eae82f06f4b304ff41cadec5c8ab61`  
		Last Modified: Thu, 21 Nov 2024 18:06:58 GMT  
		Size: 12.6 MB (12613874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e546bcfd6890b39282c82ab2456773bcfe83eb1aad1b796f1d77f2fb5e46fb5`  
		Last Modified: Thu, 21 Nov 2024 18:06:58 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db51b497b456ab414327e84619e9e47d8950da5e06568be4654ff145dfff4fd1`  
		Last Modified: Thu, 21 Nov 2024 18:06:58 GMT  
		Size: 19.7 KB (19663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d160193d423d3ad1efc0464a1b75cbf6c29873aa5b30ed7876e6ab998e588236`  
		Last Modified: Thu, 21 Nov 2024 18:06:58 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e0ffeaeb9984ae1d856c4d45577c8f5d1dfa9e11a2a05aad5af17742368037`  
		Last Modified: Thu, 21 Nov 2024 19:27:46 GMT  
		Size: 484.1 KB (484121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f421be3a7c9a02420a1b11ae1f89051f240064f83eef73b5697f2f94deaf46cb`  
		Last Modified: Thu, 21 Nov 2024 19:27:46 GMT  
		Size: 815.5 KB (815486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97db30eb4c6ce8b1f23fe0f5dc7cfd360b502f60f511338b45628e68a6ca26c`  
		Last Modified: Thu, 21 Nov 2024 19:27:46 GMT  
		Size: 1.9 MB (1862481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3580113569bc98a2bba4745a15ead37e011db02a3cfee34bb527a1bff144811a`  
		Last Modified: Thu, 21 Nov 2024 19:27:46 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:f23ea98d85265dc7991f74d8879ed4b6f0defb916775a9004e96fb60d188794c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadc922c976f7c5d79f6689905ce2a27d078525a6ef8aa907aff72fbd13f17b4`

```dockerfile
```

-	Layers:
	-	`sha256:f3898d575b90895581f38f29d35254659ae651e0c83cb78aa489f795377f73bb`  
		Last Modified: Thu, 21 Nov 2024 19:27:46 GMT  
		Size: 25.3 KB (25258 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; arm variant v6

```console
$ docker pull postfixadmin@sha256:13d08f64fc143df188c32ac203436e47f09829e5523c63dcd16cf92542eccc24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.2 MB (35157174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b6c4bca1477073c0910932b9c74098cd8df3820129791bd177676bd0c7629d`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 10 Nov 2023 16:38:27 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["/bin/sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Nov 2023 16:38:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_VERSION=8.1.31
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Nov 2023 16:38:27 GMT
WORKDIR /var/www/html
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Nov 2023 16:38:27 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
# Fri, 10 Nov 2023 16:38:27 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.13 POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a18e02044ab158842ecb75dac63ac5cf32b9b51d4ed81bdef360dedc465376a`  
		Last Modified: Thu, 21 Nov 2024 19:04:07 GMT  
		Size: 11.9 MB (11937847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af14855b94371cf79b1b05d5170f73117c488ec79d12f733e9c330fd37f46eb`  
		Last Modified: Thu, 21 Nov 2024 19:04:07 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e6b5911f56b3fa21ba06db3103fb7feee7e8bb0e5baf664a2a84a2647abe89`  
		Last Modified: Thu, 21 Nov 2024 19:07:25 GMT  
		Size: 11.4 MB (11438502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234533c66d9dc0c7f0cfa78218968806dc0d6c04bb9b109e318ae939f217d965`  
		Last Modified: Thu, 21 Nov 2024 19:07:25 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8c5f50e3e423c15de3cb8b4a6e7557dbe5dcfc2a4bb3a9cd685fb12ce1cf77`  
		Last Modified: Thu, 21 Nov 2024 19:07:25 GMT  
		Size: 19.4 KB (19435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6d04b0aa58843ed99c4dd969466749cbba0ad3be68c1917085c396d22c236c`  
		Last Modified: Thu, 21 Nov 2024 19:07:25 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695ec493ef42105c02b39a1b011eb0871ba34051ce7736083f10065e19da15e0`  
		Last Modified: Thu, 21 Nov 2024 19:30:40 GMT  
		Size: 484.0 KB (484024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e21c36659e88062399a9cd6ebb6e7e612022e6b59272c46e527974adfb9c691`  
		Last Modified: Thu, 21 Nov 2024 19:30:40 GMT  
		Size: 797.6 KB (797609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb250fd589db3101eb2f65693485b57d4330c175cd117860897f376fe1d4797`  
		Last Modified: Thu, 21 Nov 2024 19:30:40 GMT  
		Size: 1.9 MB (1862492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe021db9332f4d6bb8d001c5a3474718ce7b40733f0cd84727b60d2cc1b63e03`  
		Last Modified: Thu, 21 Nov 2024 19:30:40 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:99909d0a8f691902f0579abc879a19ac063d8f385d3d8560dde8ddeea54ae037
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9198ab0ceececec918faae674774039d1f21d20676b46423bdc8499ff622e95`

```dockerfile
```

-	Layers:
	-	`sha256:dbd702ea8c10effd8b01501dbefcfc6f6090c47a071a3bba805967a714c3cae4`  
		Last Modified: Thu, 21 Nov 2024 19:30:40 GMT  
		Size: 25.4 KB (25361 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:e48070a1d8fdd132d1ff32e0df5f75aa4a4b5b821aa79518e847acfa27ad363a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.7 MB (33738038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4ee6463b093db061ba874e60d41b6fed659b27689b46960f6892839beb8cff8`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 10 Nov 2023 16:38:27 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["/bin/sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Nov 2023 16:38:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_VERSION=8.1.31
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Nov 2023 16:38:27 GMT
WORKDIR /var/www/html
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Nov 2023 16:38:27 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
# Fri, 10 Nov 2023 16:38:27 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.13 POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab2e36daa6ef455eb354604a5ebc803469dbd1143dbd0185167a483178f9638`  
		Last Modified: Thu, 21 Nov 2024 21:16:47 GMT  
		Size: 11.9 MB (11937847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe52dcf7d7a536da57e3fc7a238e6a1b218c5ed086dbcfd899d3a57c5490c05b`  
		Last Modified: Thu, 21 Nov 2024 21:16:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1beab169fa1808c7d1a531ffe295804889bf0156ea7ffe136fe7bafa91508b`  
		Last Modified: Thu, 21 Nov 2024 21:23:53 GMT  
		Size: 10.7 MB (10724548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9feb93de021ab57d313d1e9c5c0208083cc430f26e5f93470fd412ce58f8a5b`  
		Last Modified: Thu, 21 Nov 2024 21:23:52 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89112100c7ac5b59284fac5a281e75440b9104f61b72f4a0979892c04ded5eb8`  
		Last Modified: Thu, 21 Nov 2024 21:23:52 GMT  
		Size: 19.5 KB (19454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb3075d4b15f44fee1575d1c5de6c1b7e5523bf63ceafc1e693cfd220d0ae9e`  
		Last Modified: Thu, 21 Nov 2024 21:23:52 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72df0d15bb983c22d23fdb4229e1b0bb0bedbb743c0a94ca663b998b0f7ca75`  
		Last Modified: Fri, 22 Nov 2024 03:58:19 GMT  
		Size: 444.1 KB (444093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834583d77e0f1b2e325626dd761fc2868052d2492cf16c46a8a48467b4ec31fb`  
		Last Modified: Fri, 22 Nov 2024 03:58:19 GMT  
		Size: 745.0 KB (744975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89c9a101499d052380f66d8f2ef02b63fbb4573a90c58afadd31b972742f643c`  
		Last Modified: Fri, 22 Nov 2024 03:58:19 GMT  
		Size: 1.9 MB (1862480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc65b20a002036bb23f11543c3511a77ca0371b20371ffe3766d3249906f87b7`  
		Last Modified: Fri, 22 Nov 2024 03:58:19 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:5952548d434923720e2ea8f3f0a2bae418fdcb4450ab35a4c90700d9ad700294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82a1bdb34982e7cdbbef462918a4730a1422dac94b9ddc2c4102ed4cfa80e6c`

```dockerfile
```

-	Layers:
	-	`sha256:ed1bae19d9ff820ac1113348ce20ace4a3af481901553dc60df4056c5cd77824`  
		Last Modified: Fri, 22 Nov 2024 03:58:18 GMT  
		Size: 25.4 KB (25361 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:382b70edc8ff151d301deb264b01e5704bfd406e9af1947eb7f54191e0ced394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (38002127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbde62c7d9ca81c23177e51cebe30bcf12f2e4ea98e50ff0778c7d564de2f696`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 10 Nov 2023 16:38:27 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["/bin/sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Nov 2023 16:38:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_VERSION=8.1.31
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Nov 2023 16:38:27 GMT
WORKDIR /var/www/html
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Nov 2023 16:38:27 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
# Fri, 10 Nov 2023 16:38:27 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.13 POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8484336630ebb870b45fd46b300831768da17cae91aa6a615fe97d849bf7d9`  
		Last Modified: Thu, 21 Nov 2024 18:25:41 GMT  
		Size: 6.0 MB (6047382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f0bf50f7dfd6864235893d3a770f2748c511f29a319b959cd61ab88719f191`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4094551f517548ba326fd9610784089231cb5fe7b32fb0fd484b4ef62a06ec4e`  
		Last Modified: Thu, 21 Nov 2024 18:25:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19797cf6ce6819c9730e57f097318306ed362a6402a69e5f13dee90c466ab4ef`  
		Last Modified: Thu, 21 Nov 2024 21:15:19 GMT  
		Size: 11.9 MB (11937843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bd015df81384bd6d79964b7f4f45cc9d6ee984b442934a9dfe6239f0f0fc87d`  
		Last Modified: Thu, 21 Nov 2024 21:15:18 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e89b2737597d7ee8c1418193fa7505762432e98f30950d53d220a4396de34e`  
		Last Modified: Thu, 21 Nov 2024 21:19:47 GMT  
		Size: 12.7 MB (12665270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571dc17cda90e37619fc36298e42a276a73aaa6ab3b21c4c5bf2696ed9ec514`  
		Last Modified: Thu, 21 Nov 2024 21:19:46 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5469d532aa9b49a84f57ea7fe0d5cc78e7072dd941d4d84385217349bdaa02b`  
		Last Modified: Thu, 21 Nov 2024 21:19:46 GMT  
		Size: 19.4 KB (19418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90efd9e67f0de933aa0da5fda3448c383b59d8dd03335649918dc443c46d118`  
		Last Modified: Thu, 21 Nov 2024 21:19:46 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46076c660390e7bd27c71a74ed9a4aa95f2b8a957bdc0eb616f8b33c0bce6195`  
		Last Modified: Thu, 21 Nov 2024 21:46:49 GMT  
		Size: 548.0 KB (547975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc668f58da450dbe802eadd892bb14f92fdb00b008e2467b58e452519b6390f6`  
		Last Modified: Thu, 21 Nov 2024 21:46:49 GMT  
		Size: 819.4 KB (819368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5e50661a9b512a70eaff7cb6ca369047d61c66de9837c5082c06adbc67c9c3`  
		Last Modified: Thu, 21 Nov 2024 21:46:49 GMT  
		Size: 1.9 MB (1862485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922d70a3e2f1a9124306858fcd40287fcc7f848a903a7672bbcc34a2ba56f115`  
		Last Modified: Thu, 21 Nov 2024 21:46:49 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:4156d166501fa2cbb391981098fe1df0fa53c70cca711ddc9893d271f42b31ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a4b55986942158611a59e46184eec1746be3180bff09d1fb2b0a09a414d534d`

```dockerfile
```

-	Layers:
	-	`sha256:30ef7b661707a98f46e9a1f8dfd9f204d45d721fa499f50e6b3b7a08bd3ff037`  
		Last Modified: Thu, 21 Nov 2024 21:46:48 GMT  
		Size: 25.4 KB (25393 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; 386

```console
$ docker pull postfixadmin@sha256:7f1b2bde2c0b138064f32aa5d8b906399aa18d1dfd95c5c7b657d44f86efd0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.1 MB (37059430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180f68eefad1e1b4c2db65364b2240400ddbc0a24713f335f9430215d1f48728`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 10 Nov 2023 16:38:27 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["/bin/sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Nov 2023 16:38:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_VERSION=8.1.31
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Nov 2023 16:38:27 GMT
WORKDIR /var/www/html
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Nov 2023 16:38:27 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
# Fri, 10 Nov 2023 16:38:27 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.13 POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9876669c5e6cf2326481936a518b77826aa555d22e99effa3f4ebf64ee1273ab`  
		Last Modified: Thu, 21 Nov 2024 18:07:02 GMT  
		Size: 5.5 MB (5468348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe538e073048d9d7a1f8093a3e6b97152e67534112f8fdecb309736253990ce`  
		Last Modified: Thu, 21 Nov 2024 18:07:01 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b6ee5ca50bd1b78bb17208dc0489ec0742c2236b5863864d8dc5daacd10c05`  
		Last Modified: Thu, 21 Nov 2024 18:07:01 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d54d8f0e40c8a5e4fce64e171b1819d449fc3b227d6e151d35c4759ddcf2cb`  
		Last Modified: Thu, 21 Nov 2024 18:07:02 GMT  
		Size: 11.9 MB (11937842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20585b788004ad16d84494c31a573b7c9b7ec53a9205e2b447fa147272a85b`  
		Last Modified: Thu, 21 Nov 2024 18:07:02 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64830f6d31741d3b55dc25efaaebd65fef01f800184600c16ada24cdc865337e`  
		Last Modified: Thu, 21 Nov 2024 18:07:03 GMT  
		Size: 12.9 MB (12946024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245d083aaf18329310803466fb4e9c437d02ee912d8c0f39086de152e65b3a8e`  
		Last Modified: Thu, 21 Nov 2024 18:07:03 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752754c62cc4cb95f36681627f64f621e945ff60114b87dc848e67d4012d20dc`  
		Last Modified: Thu, 21 Nov 2024 18:07:03 GMT  
		Size: 19.6 KB (19643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35636f89c61ed7822074d3376a781fe01c563f876cd243a0e54c10e149e43eb3`  
		Last Modified: Thu, 21 Nov 2024 18:07:04 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0e370a70e54a8c8c388a05271d55f81a03797397bcb4aa17946b2271aa18cd`  
		Last Modified: Thu, 21 Nov 2024 19:27:43 GMT  
		Size: 491.8 KB (491809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d05ca04d5386efb2c3a23495d891d43d0103aa5ced86a946f40df58b6522f5`  
		Last Modified: Thu, 21 Nov 2024 19:27:43 GMT  
		Size: 849.4 KB (849414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b289e7b16eda284b8f2245687d98faea33065dcdc27f7ef5fcb05632221cea`  
		Last Modified: Thu, 21 Nov 2024 19:27:43 GMT  
		Size: 1.9 MB (1862481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec62e304390a11eb3cad32a671a3a94c92eedb5e777fa855942602db19fe5e1f`  
		Last Modified: Thu, 21 Nov 2024 19:27:42 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:9f163a7823d45ba61e97e33397e602be00a60ff5a851f1ac8b4746437c27ecbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa701f3316cf467c4e2dba60397f1dc23df19a753768afb5f67c4cd5f574fe6`

```dockerfile
```

-	Layers:
	-	`sha256:688aad0c6cdd0438734fb5785b3a7fad7965bd6db593e909f1cb3e8b9323b78d`  
		Last Modified: Thu, 21 Nov 2024 19:27:42 GMT  
		Size: 25.2 KB (25223 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:ab03b4a24d93dead1ca12e03e0c62195994eca2b05a60902c1ac9ddf497bfc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.5 MB (37472885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21876610a2a627c911a7b04077b669ab0d56598ac54a7340e85964f8de62d1f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 10 Nov 2023 16:38:27 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["/bin/sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Nov 2023 16:38:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_VERSION=8.1.31
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Nov 2023 16:38:27 GMT
WORKDIR /var/www/html
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Nov 2023 16:38:27 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
# Fri, 10 Nov 2023 16:38:27 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.13 POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2473147d3bc2923a26c8ba560c425ef2674fbae2edbc29833bb5790c2c94db2`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 5.6 MB (5572572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53975073457162c05af82756884811d86cf52d05953b0589749a216a80864431`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58037573bd03f9687676a3398cb715ac628a3bc280f63aa990e8171ef59ce1c9`  
		Last Modified: Tue, 12 Nov 2024 03:38:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e46e43e6d8057861c96a021303d5d0c4219c291ea695cf8e4ee47baa6a0438d`  
		Last Modified: Thu, 21 Nov 2024 20:07:51 GMT  
		Size: 11.9 MB (11937849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:658a8fc4b19e1811f54dc686c4114321a23783ec80af62e0e1767557c3863497`  
		Last Modified: Thu, 21 Nov 2024 20:07:50 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b14ea65f2f59d82e968bd688c8926a67686dc8f6223e54491109219851685ab5`  
		Last Modified: Thu, 21 Nov 2024 20:11:18 GMT  
		Size: 13.1 MB (13058440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351e9347dedc9f47b45b017dbb8aeb2dfe0850142ec4df6c3a0341ae251d197c`  
		Last Modified: Thu, 21 Nov 2024 20:11:17 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701580745268556140d76eea5b39c91c3472d7af2c31cb13fab3a0183c9dabe9`  
		Last Modified: Thu, 21 Nov 2024 20:11:18 GMT  
		Size: 19.4 KB (19426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec672315fbc5e0eeb2b0f6506edf5e86be439e030b04ddbf06e825a5264471b8`  
		Last Modified: Thu, 21 Nov 2024 20:11:18 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa844b4354f13300e3caa13d914c2cb076793f745ae7d65c82ba73994e1a98a2`  
		Last Modified: Fri, 22 Nov 2024 00:55:50 GMT  
		Size: 551.1 KB (551091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a09cd3380ea8f4c1c9a823eb8dd1c7d96773d35f78b6029cde3bb8047ac5aa`  
		Last Modified: Fri, 22 Nov 2024 00:55:50 GMT  
		Size: 883.9 KB (883883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db0a98e9bfc90dbaaac4f446683f88c56693d4c34ae9396c5aa8f0de40e52ce`  
		Last Modified: Fri, 22 Nov 2024 00:55:50 GMT  
		Size: 1.9 MB (1862489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38443d9224bd4757c36864f6515941f86d70841e881324a9fb024fab985046d`  
		Last Modified: Fri, 22 Nov 2024 00:55:50 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:c1c0185a1767387f83d5da6f4b7f99ee8e3f3376c9f8e679dd7340595101e287
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b7f9fa7024f25f915d6a672a797729c79e2edb2bce464e333167a5ab1a3862`

```dockerfile
```

-	Layers:
	-	`sha256:faccbe7a76a12c79d4ffeac5cced799ab558e9ec724bda41121c953b65192b2d`  
		Last Modified: Fri, 22 Nov 2024 00:55:50 GMT  
		Size: 25.3 KB (25307 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; riscv64

```console
$ docker pull postfixadmin@sha256:0c1dc74588651f568e08342d31ce4f3bad55ac32cf4271ab79e2684d99dceb24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36346485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dda03fedc3db16a908870113b9cb4f98420704a8cb3a7f3ced2a78bb9518b4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 10 Nov 2023 16:38:27 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["/bin/sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Nov 2023 16:38:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_VERSION=8.1.31
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Nov 2023 16:38:27 GMT
WORKDIR /var/www/html
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Nov 2023 16:38:27 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
# Fri, 10 Nov 2023 16:38:27 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.13 POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9ea701a0e6dade687d4558cd4a6ca78c5358d1bc6fde5ba327f2283f6a7bde`  
		Last Modified: Fri, 22 Nov 2024 02:05:35 GMT  
		Size: 11.9 MB (11937856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e1dd72cb8a9fa8bbf8d3831c89ce08fcfe654cef81dac92990d05bea51238f`  
		Last Modified: Fri, 22 Nov 2024 02:05:33 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7eda5fb922780adf3876bb2aca5197905ab0ad8177880dda6cc9211fbc7f6f5`  
		Last Modified: Fri, 22 Nov 2024 02:48:11 GMT  
		Size: 12.4 MB (12421655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0198d07856649aaddc987520f0cc1c554287ef974be77fd7e01ad562991de60`  
		Last Modified: Fri, 22 Nov 2024 02:48:09 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d32f2d435262eea68a1ace42b4b90b33c0aa2287f7ba4df1b3a580dc4e0c16`  
		Last Modified: Fri, 22 Nov 2024 02:48:09 GMT  
		Size: 19.4 KB (19441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00c0c276d5c71bd83fbf7a9c2db6f4f20d286f89cc6386d60ca2876ae4e51c0`  
		Last Modified: Fri, 22 Nov 2024 02:48:09 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037368cbf2ac1a7e9f8738d737780f77372b61164ab6e09ad550a8881fe483f7`  
		Last Modified: Fri, 22 Nov 2024 03:40:21 GMT  
		Size: 496.6 KB (496630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c926ca1ba50a7ac15076b58d2fdfa7e69399d151fd9e507404b205e412a58a`  
		Last Modified: Fri, 22 Nov 2024 03:40:21 GMT  
		Size: 840.1 KB (840081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5ac8afbd5d0ecc8c6353a62134c0aec461e3d7dacfe9ad590dc56225ace73`  
		Last Modified: Fri, 22 Nov 2024 03:40:21 GMT  
		Size: 1.9 MB (1862490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88160bde8c4502037ae5f72c22cea1968e6c3a8ddb33392328b620ed638f6bae`  
		Last Modified: Fri, 22 Nov 2024 03:40:20 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:c0961bb2abdc021914eece1a4bc9629a4f5752a4edec068e8ac44f8292456251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3e422ae65d48bf022bfbbc9aab1b56b9c5f9fbcf011285d5f971437258a1c7`

```dockerfile
```

-	Layers:
	-	`sha256:581ff6b6ab40b259898b2cfb9cb1dcdb0e675ff69844ccc8eb09b3acb3c78b7f`  
		Last Modified: Fri, 22 Nov 2024 03:40:20 GMT  
		Size: 25.3 KB (25307 bytes)  
		MIME: application/vnd.in-toto+json

### `postfixadmin:fpm-alpine` - linux; s390x

```console
$ docker pull postfixadmin@sha256:a42f4fc91cfb9601a808f6444aef035f5bcee2630f2a09b805611d711ba5b7f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.7 MB (36739240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ee0e6f78b18e81443f3b7ab1777840c694548198768b83a8c16cbe5a8454ab`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 10 Nov 2023 16:38:27 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["/bin/sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 10 Nov 2023 16:38:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_VERSION=8.1.31
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Fri, 10 Nov 2023 16:38:27 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Nov 2023 16:38:27 GMT
WORKDIR /var/www/html
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Nov 2023 16:38:27 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
# Fri, 10 Nov 2023 16:38:27 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Fri, 10 Nov 2023 16:38:27 GMT
RUN apk add --no-cache 		bash 		su-exec # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		imap-dev 		krb5-dev 		postgresql-dev 		sqlite-dev 	; 	docker-php-ext-configure 		imap --with-imap-ssl --with-kerberos 	; 	docker-php-ext-install -j "$(nproc)" 		imap 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .postfixadmin-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ARG POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_VERSION=3.3.13
# Fri, 10 Nov 2023 16:38:27 GMT
ENV POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
# Fri, 10 Nov 2023 16:38:27 GMT
# ARGS: POSTFIXADMIN_VERSION=3.3.13 POSTFIXADMIN_SHA512=bf7daaa089ee3adc4b557f1a7d0509d78979ef688fb725bab795f5c9d81e8774296245fde0cb184db51e9185cad381682c3ecc0bfadf852388b499a0a95cca64
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 10 Nov 2023 16:38:27 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Fri, 10 Nov 2023 16:38:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26915a92034b18e2de9232a415d1ad92dc1c7a9f9e2b5bb9c590ce4c503ab73e`  
		Last Modified: Tue, 12 Nov 2024 03:39:27 GMT  
		Size: 5.5 MB (5532119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4041b6d620078267a8ee6dd6b9c31735d82dee5f22aa96467865a8134d616c`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5555efb309fc5275c2fd44eabaaf4ca859f01b510ef24cbad6009d7ed6dc4696`  
		Last Modified: Tue, 12 Nov 2024 03:39:26 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b559ab5315872526ac0ff6db4c779545710e456d323ec2712b45db490a8e7899`  
		Last Modified: Thu, 21 Nov 2024 20:40:33 GMT  
		Size: 11.9 MB (11937848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f0214f1860126ac08019959b55270fa455b89d7d0d2ce6f0aa2dd0efacf19d`  
		Last Modified: Thu, 21 Nov 2024 20:40:33 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26225bf7b65ff4b28693c71fc0fa639be97ed6f722cc01c54ce3be00a76a9b26`  
		Last Modified: Thu, 21 Nov 2024 20:44:14 GMT  
		Size: 12.5 MB (12549753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6089e6ee733c9b1ff51e5cf192163552c26ac4a717f434221cbd26f7fecec6c`  
		Last Modified: Thu, 21 Nov 2024 20:44:13 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea4b687cccc9bab1dc12822a8dc34dd32aa6de8cc720df11100ec1f2e6f6436`  
		Last Modified: Thu, 21 Nov 2024 20:44:13 GMT  
		Size: 19.4 KB (19436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a01bb377a1eeb5185a61593c40f64e701eff225d9fb8af10a48258bf2783df`  
		Last Modified: Thu, 21 Nov 2024 20:44:14 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736182126653afd3e164c1d1d9e7c0b2d2db045ab7030073672666f6d1c20b8c`  
		Last Modified: Fri, 22 Nov 2024 02:02:37 GMT  
		Size: 513.9 KB (513871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bee37ec5c4e7b04bb102c38435bcf30e78f942369dbb34897a0d04c4826801`  
		Last Modified: Fri, 22 Nov 2024 02:02:37 GMT  
		Size: 847.5 KB (847459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815bb2739f4e164713b584b70d100988d9d3970a97f7d55364097082c9800095`  
		Last Modified: Fri, 22 Nov 2024 02:02:37 GMT  
		Size: 1.9 MB (1862485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7d64a91971e87dc379ebd1e49e9e1b32f1c879fed7412bad8fcbef1c33fb23`  
		Last Modified: Fri, 22 Nov 2024 02:02:37 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `postfixadmin:fpm-alpine` - unknown; unknown

```console
$ docker pull postfixadmin@sha256:1585f73f3ecddefe4a5289300698f9c92439112cb0b0f0e5683a2901641dd720
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7f49a643b18c8fac4d16e4045888842603ab883d5588fc6066e60f9eac06a78`

```dockerfile
```

-	Layers:
	-	`sha256:76718bfa122ec4666a8f94dd86473bf34376b00e13c0787f0d7ef96c145ac7fe`  
		Last Modified: Fri, 22 Nov 2024 02:02:36 GMT  
		Size: 25.3 KB (25259 bytes)  
		MIME: application/vnd.in-toto+json
