## `php:alpine`

```console
$ docker pull php@sha256:0997a6c2fe80f8eb1375c7ab4732632389a0ed3710d56707fc47a118a8025a3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `php:alpine` - linux; amd64

```console
$ docker pull php@sha256:ef40f8849d022ec4231789ac1081d93eb18b6389a7991499e5f2afd0bb3849eb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.7 MB (29701979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34e49dbb09fc658324acef2eae9900bb40bb559029a03c1f371699fe966ee0d7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 08:41:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Dec 2020 08:41:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 17 Dec 2020 08:41:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 17 Dec 2020 08:41:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Dec 2020 08:41:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 17 Dec 2020 08:41:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 08:41:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 08:41:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Dec 2020 08:41:57 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 07 Jan 2021 21:13:41 GMT
ENV PHP_VERSION=8.0.1
# Thu, 07 Jan 2021 21:13:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Thu, 07 Jan 2021 21:13:41 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Thu, 07 Jan 2021 21:13:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 07 Jan 2021 21:13:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Jan 2021 21:20:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Jan 2021 21:20:33 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Thu, 07 Jan 2021 21:20:35 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Jan 2021 21:20:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Jan 2021 21:20:35 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e2096094279456885c5847855bddf4d9ac3b5c4f7f0ff73ef92fa69821ff86`  
		Last Modified: Thu, 17 Dec 2020 11:05:30 GMT  
		Size: 1.3 MB (1340903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:320f26ee9b1c7b4c2ce0b67550a066ea859fb8796c0ff8de576f7e1b330342da`  
		Last Modified: Thu, 17 Dec 2020 11:05:30 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4612e05a72cfb0fde0de7565baa2660900747122288141d8dba25482f4983fe0`  
		Last Modified: Thu, 17 Dec 2020 11:05:30 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32008435a870a53c266d820886f1e0f7478a6b05bb70e1379f7869fcd0b432e2`  
		Last Modified: Thu, 07 Jan 2021 21:36:27 GMT  
		Size: 10.7 MB (10661148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462ac2134599ea707a9900c84255e73a0103396a92e14e3de262a686f6f68b3c`  
		Last Modified: Thu, 07 Jan 2021 21:36:27 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a936ffa0dc56e2359d1d39d9c1e1d1e03a620747e37d58c8ac0f49167dbca447`  
		Last Modified: Thu, 07 Jan 2021 21:36:29 GMT  
		Size: 14.9 MB (14879769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1d6b80228b9a30729577a7dbeda22b66fa1814fae19ac9a97f4317a200825b`  
		Last Modified: Thu, 07 Jan 2021 21:36:27 GMT  
		Size: 2.3 KB (2258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a767aca8974e430fc2b978d952cdb00c89e050f10f4e099b45977dd4d863f936`  
		Last Modified: Thu, 07 Jan 2021 21:36:27 GMT  
		Size: 16.9 KB (16881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine` - linux; arm variant v6

```console
$ docker pull php@sha256:d767c13319ec96499588506fb9ed51cd323b8fd4df432886859f429b31191a39
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.2 MB (28152325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2ad09a3e0221553b42da22b418f1d9800ecde33fa006af77caa2282055cd399`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 04:02:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Dec 2020 04:02:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 17 Dec 2020 04:02:27 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 17 Dec 2020 04:02:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Dec 2020 04:02:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 17 Dec 2020 04:02:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 04:02:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 04:02:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Dec 2020 04:02:36 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 07 Jan 2021 21:45:06 GMT
ENV PHP_VERSION=8.0.1
# Thu, 07 Jan 2021 21:45:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Thu, 07 Jan 2021 21:45:09 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Thu, 07 Jan 2021 21:45:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 07 Jan 2021 21:45:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Jan 2021 21:49:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Jan 2021 21:49:02 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Thu, 07 Jan 2021 21:49:07 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Jan 2021 21:49:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Jan 2021 21:49:10 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16035da780bb4f74637b8f27602f05d4a81886aeea06f603ea7e46dd84d57b6d`  
		Last Modified: Thu, 17 Dec 2020 05:38:57 GMT  
		Size: 1.3 MB (1310288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfae7d4501031aa09e0c64be274eb95df5740b32cde16be0182bcea9d8a4845`  
		Last Modified: Thu, 17 Dec 2020 05:38:57 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6384065388d88752c6562c2bb76398ecc59f1a03a1c5e4601dc75d768117919`  
		Last Modified: Thu, 17 Dec 2020 05:38:56 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f9039db074e269d9978ef8b86ba1ad88708f8af98d5ef1d09658c5f10b2442`  
		Last Modified: Thu, 07 Jan 2021 21:56:02 GMT  
		Size: 10.7 MB (10661176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7488dc7128c612534b6d69831276a3af50f1164c922f575654d874843056456`  
		Last Modified: Thu, 07 Jan 2021 21:56:01 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd0063fd4481ec51be4af984e94d9effad02923292731f40bb55cde186cea96`  
		Last Modified: Thu, 07 Jan 2021 21:56:07 GMT  
		Size: 13.6 MB (13555529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e5168a13bcdb514dc00ed5a211abbcfcf8316fc751a28d817225f04e32317f`  
		Last Modified: Thu, 07 Jan 2021 21:56:01 GMT  
		Size: 2.3 KB (2261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031a874237d0b0846cf6ca34599738dbe25adde71a414f713f3011de99235edb`  
		Last Modified: Thu, 07 Jan 2021 21:56:01 GMT  
		Size: 16.9 KB (16884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine` - linux; arm variant v7

```console
$ docker pull php@sha256:c04ab06790f2c36964534ea739c1bab82059937f1d855152fa54d8304d085348
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27005251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b85153357b5815a24d98036c19839e47d2316e30af2c29c1ed051e0c760769f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 16 Dec 2020 23:58:14 GMT
ADD file:bd07f77a2b2741ca6bda80d9203be9c7274cf73145bff778cf000db0d8d4e903 in / 
# Wed, 16 Dec 2020 23:58:15 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 03:59:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Dec 2020 03:59:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 17 Dec 2020 03:59:49 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 17 Dec 2020 03:59:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Dec 2020 03:59:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 17 Dec 2020 03:59:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 03:59:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 03:59:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Dec 2020 03:59:55 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 07 Jan 2021 23:19:24 GMT
ENV PHP_VERSION=8.0.1
# Thu, 07 Jan 2021 23:19:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Thu, 07 Jan 2021 23:19:25 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Thu, 07 Jan 2021 23:19:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 07 Jan 2021 23:19:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Jan 2021 23:22:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Jan 2021 23:22:06 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Thu, 07 Jan 2021 23:22:08 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Jan 2021 23:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Jan 2021 23:22:10 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:c58e8a26a8407acc3ead776f6526efa889fda03270a8d05109208d9f59159420`  
		Last Modified: Wed, 16 Dec 2020 23:58:59 GMT  
		Size: 2.4 MB (2407555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb43bb12dd6693d888e6501fba59948c3e894b068d539fbf968aac1638f58847`  
		Last Modified: Thu, 17 Dec 2020 05:28:25 GMT  
		Size: 1.2 MB (1214517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c593d596abc28364a253c99118c3080eec76e91bf5db463e2a66804da18dfa`  
		Last Modified: Thu, 17 Dec 2020 05:28:23 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145a8f86ceab4a34dedf8d4173439cf517eec5c52b3074dea204dce67da7f3ad`  
		Last Modified: Thu, 17 Dec 2020 05:28:23 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21da298c25d5a1429ec981f4073fa30f759bd96b4c725a825e94f50f38b5b344`  
		Last Modified: Thu, 07 Jan 2021 23:33:01 GMT  
		Size: 10.7 MB (10661166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed9bfe8d6457b9fc318e9b0f7ae6e0e4e2f938c4f9b39b8225274f9c889fa82`  
		Last Modified: Thu, 07 Jan 2021 23:32:59 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b43159b72ada7e2901832354942c3353d338c88dfe20c8776c7b65ef4cb6940f`  
		Last Modified: Thu, 07 Jan 2021 23:33:06 GMT  
		Size: 12.7 MB (12700876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de6e3c2d704f368919e91e2557debcc70fa5a77064f9638d7970cd48bc6255a`  
		Last Modified: Thu, 07 Jan 2021 23:33:02 GMT  
		Size: 2.3 KB (2259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b8c3972bdcbd8826d391e3be9096bd118e015d60e49792c87ecae4e451edc0`  
		Last Modified: Thu, 07 Jan 2021 23:33:00 GMT  
		Size: 16.9 KB (16850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine` - linux; arm64 variant v8

```console
$ docker pull php@sha256:08385df4efe0a99e6fdeec5315431aa581e79c6f02ff42bb12b574390a4eb963
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29084277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c25acb02ff55b72bb5d116ba1939dfe817f5d43b670fae3052183c28a3e92ab`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 05:46:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Dec 2020 05:46:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 17 Dec 2020 05:46:55 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 17 Dec 2020 05:46:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Dec 2020 05:47:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 17 Dec 2020 05:47:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 05:47:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 05:47:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Dec 2020 05:47:15 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 08 Jan 2021 00:18:56 GMT
ENV PHP_VERSION=8.0.1
# Fri, 08 Jan 2021 00:18:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Fri, 08 Jan 2021 00:18:58 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Fri, 08 Jan 2021 00:19:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 08 Jan 2021 00:19:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 08 Jan 2021 00:22:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 08 Jan 2021 00:22:24 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Fri, 08 Jan 2021 00:22:26 GMT
RUN docker-php-ext-enable sodium
# Fri, 08 Jan 2021 00:22:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 Jan 2021 00:22:28 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349511631cc12dc049249fd94f9012c505ccb000f16147091cb84874846fb9b1`  
		Last Modified: Thu, 17 Dec 2020 07:10:16 GMT  
		Size: 1.3 MB (1342931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053bd098149c8419c2b9b5a2702c5d9c4e9de3b2131447e18aacde4047de2d88`  
		Last Modified: Thu, 17 Dec 2020 07:10:15 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00122640c7f935b33a14c9e88b946165e75935d6cd28f9b2d20d783d43c21423`  
		Last Modified: Thu, 17 Dec 2020 07:10:15 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede74f71ccdef249765a4b6b08900533eba4fb777a60a37d91a049132f326ef6`  
		Last Modified: Fri, 08 Jan 2021 00:34:11 GMT  
		Size: 10.7 MB (10661184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e824794dd9514f893b336694964533dd9bc00b8ff444a30a859528c17c20fc`  
		Last Modified: Fri, 08 Jan 2021 00:34:09 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db6b6a2a79f5766dfbd793de1003466963521d315bff134d2a53981c9c53d399`  
		Last Modified: Fri, 08 Jan 2021 00:34:17 GMT  
		Size: 14.3 MB (14349933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c3503c7fd5e07a3b2cd1dd768b3bd0912135fea8512c5a1522af175bab64651`  
		Last Modified: Fri, 08 Jan 2021 00:34:09 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:062942a7cd0bc47875fcc1ef5cb29db126b7d17dc268841d0c017fcc1fb5ff67`  
		Last Modified: Fri, 08 Jan 2021 00:34:09 GMT  
		Size: 16.9 KB (16897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine` - linux; 386

```console
$ docker pull php@sha256:304981e879b4924e73f173cd22d13c534f141c132a53b7dcced92f9a0539316d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.8 MB (29834641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaa514a979fa608841fa92fac036b54ee79e1182df655e2472d148e7b598d8cb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 17 Dec 2020 00:38:32 GMT
ADD file:de33fda50a142403e842620d20bc4404e66fc4ace16edc6946c4539e8a797458 in / 
# Thu, 17 Dec 2020 00:38:32 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 03:34:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Dec 2020 03:34:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 17 Dec 2020 03:34:06 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 17 Dec 2020 03:34:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Dec 2020 03:34:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 17 Dec 2020 03:34:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 03:34:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 03:34:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Dec 2020 03:34:08 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 07 Jan 2021 21:56:37 GMT
ENV PHP_VERSION=8.0.1
# Thu, 07 Jan 2021 21:56:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Thu, 07 Jan 2021 21:56:37 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Thu, 07 Jan 2021 21:56:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 07 Jan 2021 21:56:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Jan 2021 22:03:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Jan 2021 22:03:56 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Thu, 07 Jan 2021 22:03:57 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Jan 2021 22:03:58 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Jan 2021 22:03:58 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:455793c72b878001f0905634ed52a2524ba51796e7377bf00683a85123f7dce9`  
		Last Modified: Thu, 17 Dec 2020 00:39:18 GMT  
		Size: 2.8 MB (2794130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94d120997ac65664d4944fb3d9d4551e8e118f43c788aa67591c2cb54010aed`  
		Last Modified: Thu, 17 Dec 2020 05:43:55 GMT  
		Size: 1.4 MB (1439814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657c96696eb3a101b3148ccc28a870e751ee94e39bb2f3cc1745bdec7655b033`  
		Last Modified: Thu, 17 Dec 2020 05:43:55 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25357089a74d7e4f4ee1bc77cd180c431537e393399785f113a7f2fe4ac7614`  
		Last Modified: Thu, 17 Dec 2020 05:43:52 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e5a682f5af04c3cc10b717a6e8a5a845fea167b7b5490c3994a6bb7274bf7a`  
		Last Modified: Thu, 07 Jan 2021 22:19:05 GMT  
		Size: 10.7 MB (10661145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026d9067ced70bebaf357e9dfcd772212bcf24ddc27d5676774e0d1de6d67f5a`  
		Last Modified: Thu, 07 Jan 2021 22:19:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301c55333777846199f4a44e59b133eab4400343817ea2867f12d910ab65956c`  
		Last Modified: Thu, 07 Jan 2021 22:19:09 GMT  
		Size: 14.9 MB (14918473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8405ffe542cd6db3ce92049365426e737ad7ac88dd4ef9942b8e5b1155ab287e`  
		Last Modified: Thu, 07 Jan 2021 22:19:05 GMT  
		Size: 2.3 KB (2257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9efedcef6efd9606b7ff1bb336d88d7a157265f391d9746e6d06df04bb21d7`  
		Last Modified: Thu, 07 Jan 2021 22:19:04 GMT  
		Size: 16.9 KB (16874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine` - linux; ppc64le

```console
$ docker pull php@sha256:fdf53d69282214e1754759ea3a9d9904bd1b8a42e8e847bd45d921663986ef34
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 MB (30507486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53d58e3413aa38500e20a91bf4ce3b8f87789e5930305660edd115f29c543117`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Thu, 17 Dec 2020 00:20:42 GMT
ADD file:0a38c9b4955f8faa79627c166fca80ef342e443a16ce2925a30eeae317bbd786 in / 
# Thu, 17 Dec 2020 00:20:48 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:02:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Dec 2020 06:02:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 17 Dec 2020 06:03:11 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 17 Dec 2020 06:03:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Dec 2020 06:03:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 17 Dec 2020 06:03:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 06:04:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 06:04:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Dec 2020 06:04:07 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 17 Dec 2020 06:04:12 GMT
ENV PHP_VERSION=8.0.0
# Thu, 17 Dec 2020 06:04:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.0.tar.xz.asc
# Thu, 17 Dec 2020 06:04:24 GMT
ENV PHP_SHA256=b5278b3eef584f0c075d15666da4e952fa3859ee509d6b0cc2ed13df13f65ebb
# Thu, 17 Dec 2020 06:04:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 17 Dec 2020 06:04:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Dec 2020 06:08:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Dec 2020 06:09:05 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Thu, 17 Dec 2020 06:09:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Dec 2020 06:09:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Dec 2020 06:09:20 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:a9d343b7bcc225fe7ac17d96a81329510ab7f31a50472311cafe7168d3107317`  
		Last Modified: Thu, 17 Dec 2020 00:21:33 GMT  
		Size: 2.8 MB (2805226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4878c44618050313be4a5ac046d572683a6e0d371586c31a768e1768423df9a3`  
		Last Modified: Thu, 17 Dec 2020 08:04:10 GMT  
		Size: 1.4 MB (1383302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577c712c96426aadbf75437b4aae5841ed84ba25ee142ec3aaaf86802464d6f9`  
		Last Modified: Thu, 17 Dec 2020 08:04:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a10ca736025b1646c79fbd378c22773ccb82df4aadc2cb960dea6eacb8bbb16`  
		Last Modified: Thu, 17 Dec 2020 08:04:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe5c405f90aa31a02b0a9e3ea283928ce356c4a471f73dab20286d62c6f6eaa`  
		Last Modified: Thu, 17 Dec 2020 08:04:06 GMT  
		Size: 10.7 MB (10745619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:effaa3096da7c0c3dacc293a169c75042cb06f11de914e099e4f60d8100c8c27`  
		Last Modified: Thu, 17 Dec 2020 08:04:04 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbca319951a1e637ed427f46cce217bd77b465f3bb8f887514e23332b009b49`  
		Last Modified: Thu, 17 Dec 2020 08:04:08 GMT  
		Size: 15.6 MB (15552126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28726803a617f555f37681d0efaf3057e7082f90941199313b01140fe06d959`  
		Last Modified: Thu, 17 Dec 2020 08:04:04 GMT  
		Size: 2.3 KB (2261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3608a877faf61d02ea62044d3b2f4fc31d96541df7c0b82783c3ceafe3e04f0f`  
		Last Modified: Thu, 17 Dec 2020 08:04:04 GMT  
		Size: 16.9 KB (16932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `php:alpine` - linux; s390x

```console
$ docker pull php@sha256:a740755ee6e65d2b599df6f69abf170f99328eb5a04d7adf17a91d33de933d0e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.5 MB (28478506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78eca1488f92a37b626fdbcb2de598ec75b61c399642fd7eab8c4e713806f71f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php","-a"]`

```dockerfile
# Wed, 16 Dec 2020 23:41:37 GMT
ADD file:3ad3856d165e8760af85574a8ffa75ca44b7e1b97b64d1d6d4608445efa4b860 in / 
# Wed, 16 Dec 2020 23:41:37 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 06:11:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 17 Dec 2020 06:11:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 17 Dec 2020 06:11:33 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 17 Dec 2020 06:11:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Dec 2020 06:11:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 17 Dec 2020 06:11:36 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 06:11:37 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Dec 2020 06:11:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Dec 2020 06:11:38 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 07 Jan 2021 22:21:34 GMT
ENV PHP_VERSION=8.0.1
# Thu, 07 Jan 2021 22:21:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.1.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.1.tar.xz.asc
# Thu, 07 Jan 2021 22:21:34 GMT
ENV PHP_SHA256=208b3330af881b44a6a8c6858d569c72db78dab97810332978cc65206b0ec2dc
# Thu, 07 Jan 2021 22:21:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 07 Jan 2021 22:21:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 07 Jan 2021 22:26:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 07 Jan 2021 22:26:14 GMT
COPY multi:afab483600631d4d87fe030871bbb016f1c2b73c0b72609d857bace419af7f5d in /usr/local/bin/ 
# Thu, 07 Jan 2021 22:26:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 07 Jan 2021 22:26:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 Jan 2021 22:26:17 GMT
CMD ["php" "-a"]
```

-	Layers:
	-	`sha256:ee52640a49e15b8b7c8edb66c2d048b26abdee8d828d6e5ef4e10a28cb15a84f`  
		Last Modified: Wed, 16 Dec 2020 23:42:15 GMT  
		Size: 2.6 MB (2567018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b33a1a773ad25f9d9c6930913defa3b9196c1fdcd8d5a2d592215cda11cf944`  
		Last Modified: Thu, 17 Dec 2020 08:07:32 GMT  
		Size: 1.4 MB (1382756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4721c450aa935167d123ebc6322a5f753171e457cd26615b6c8cea6dcc8648`  
		Last Modified: Thu, 17 Dec 2020 08:07:31 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17cb6f51130bdca075886a326b2ea4010f9a422c82d02cdb21ff7fb1bcd6936`  
		Last Modified: Thu, 17 Dec 2020 08:07:31 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4eb1b744f48b63b2822cd789c6f4a27112a754311b4ee8a0fe4e85c865a4845`  
		Last Modified: Thu, 07 Jan 2021 22:36:22 GMT  
		Size: 10.7 MB (10661182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30607f3919b220034c4788b87c5462f4f352f4f599b33504bef62edf16504254`  
		Last Modified: Thu, 07 Jan 2021 22:36:21 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc4f9527809c2fe14411715553e37bd3404dd57442e411e8d6776ddf8e90e04`  
		Last Modified: Thu, 07 Jan 2021 22:36:23 GMT  
		Size: 13.8 MB (13846388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5006a125e06c873a612b118cfaf927f0f748c2f4e6f3d8d54fec9cda62c5c555`  
		Last Modified: Thu, 07 Jan 2021 22:36:21 GMT  
		Size: 2.3 KB (2254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d83f87f3d0c5a7f96503d6edffc6140b949550c39f6d07d26d835b7ea8f25e`  
		Last Modified: Thu, 07 Jan 2021 22:36:21 GMT  
		Size: 16.9 KB (16885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
