## `composer:latest`

```console
$ docker pull composer@sha256:401afc656a993cd2bfa9a0d808bbc60a212bfb4d296a894b67d5d2993a8d2d96
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

### `composer:latest` - linux; amd64

```console
$ docker pull composer@sha256:f98117535d7e937ee0bb2b8563f94d335e453b94532fa879e4e40e9514bd0a65
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63241868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7582e1592f800ec54de78f4be567a86ed92095c698b1f055db5a0dde430a4aef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 15 Jun 2021 22:19:37 GMT
ADD file:f278386b0cef68136129f5f58c52445590a417b624d62bca158d4dc926c340df in / 
# Tue, 15 Jun 2021 22:19:37 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 23:32:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Jun 2021 23:32:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 16 Jun 2021 23:32:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 16 Jun 2021 23:32:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Jun 2021 23:32:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 16 Jun 2021 23:32:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Jun 2021 23:32:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Jun 2021 23:32:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Jun 2021 23:35:57 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 16 Jun 2021 23:35:57 GMT
ENV PHP_VERSION=8.0.7
# Wed, 16 Jun 2021 23:35:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.7.tar.xz.asc
# Wed, 16 Jun 2021 23:35:58 GMT
ENV PHP_SHA256=d5fc2e4fc780a32404d88c360e3e0009bc725d936459668e9c2ac992f2d83654
# Mon, 28 Jun 2021 20:57:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 28 Jun 2021 20:57:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 28 Jun 2021 21:06:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 28 Jun 2021 21:06:20 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Mon, 28 Jun 2021 21:06:23 GMT
RUN docker-php-ext-enable sodium
# Mon, 28 Jun 2021 21:06:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 28 Jun 2021 21:06:23 GMT
CMD ["php" "-a"]
# Tue, 29 Jun 2021 03:40:17 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Tue, 29 Jun 2021 03:40:28 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Tue, 29 Jun 2021 03:40:29 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Tue, 29 Jun 2021 03:40:29 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 29 Jun 2021 03:40:29 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 29 Jun 2021 03:40:29 GMT
ENV COMPOSER_VERSION=2.1.3
# Tue, 29 Jun 2021 03:40:33 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer   ;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Tue, 29 Jun 2021 03:40:33 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Tue, 29 Jun 2021 03:40:34 GMT
WORKDIR /app
# Tue, 29 Jun 2021 03:40:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Jun 2021 03:40:34 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5843afab387455b37944e709ee8c78d7520df80f8d01cf7f861aae63beeddb6b`  
		Last Modified: Tue, 15 Jun 2021 22:20:04 GMT  
		Size: 2.8 MB (2811478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfcf566573f3f708d78b43786614663e55d9a9d02621f3dab2127292efbbacab`  
		Last Modified: Fri, 25 Jun 2021 21:36:24 GMT  
		Size: 1.7 MB (1707289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ff9828d9544109bb07a2fa8308b1ed77b75738fa50300d61284755c126426a`  
		Last Modified: Fri, 25 Jun 2021 21:36:24 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165b10189b0ff16bb4ac114562bc55a25c753c9fc11999774fc42e9979feef99`  
		Last Modified: Fri, 25 Jun 2021 21:36:23 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c0992b46bfe8602a0b527cd82280cf25f28e7f6455720e222a4b4ef4bfd9f2`  
		Last Modified: Tue, 29 Jun 2021 00:43:16 GMT  
		Size: 10.8 MB (10788793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8841f9c80d654287e11a6cae98541af23eb0cd8bf7e6a0840ca1fbbf0079e1e1`  
		Last Modified: Tue, 29 Jun 2021 00:43:15 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:468506ccfa873b12e75a39c4cd5d3d25775e543afe72fe77b59f93fbeebf0ec0`  
		Last Modified: Tue, 29 Jun 2021 00:43:18 GMT  
		Size: 15.0 MB (14955456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217e520e9c7fab93043ccffeff15e5a8fba25e0d7581b29bd22cb7e5308e0ac8`  
		Last Modified: Tue, 29 Jun 2021 00:43:15 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb2542db89195f55254c847ea5671fcffc6b2cf5857a85878375c7624cfb690`  
		Last Modified: Tue, 29 Jun 2021 00:43:15 GMT  
		Size: 17.8 KB (17780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4855455770675c16f2f9747072bf608b1a713ccb788c8a09d6d407277b6e9c80`  
		Last Modified: Tue, 29 Jun 2021 03:41:05 GMT  
		Size: 32.2 MB (32200525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b193b96f894d9c861e3471ff44bf3853d73076749890d5b87de901865609d9a3`  
		Last Modified: Tue, 29 Jun 2021 03:40:56 GMT  
		Size: 200.9 KB (200946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:089514ab53ed474d51085b2dd16c12ce1b658a2ac32284e2e92bcf6e6d441d87`  
		Last Modified: Tue, 29 Jun 2021 03:40:56 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1690379808b1d570dffcda5fe35411d27c22f8b45e21bd62f5734d1829ec7383`  
		Last Modified: Tue, 29 Jun 2021 03:40:56 GMT  
		Size: 554.5 KB (554518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6643a0e23032ceee23c52a338c288e73fbacc6e0da8b2e5dd399e97bb35b09`  
		Last Modified: Tue, 29 Jun 2021 03:40:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed07b47743bbacb4486977fe9b6ccf6d78d44d61a7528fa70d705f4861ddf78f`  
		Last Modified: Tue, 29 Jun 2021 03:40:56 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:719e75b1726cc15b80fd4ee381bab6e0b1ec03ab115512bf43b7e60b613913db
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59419828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b68c5d19793703dd0d0f259ac35a9eda5b88758960b1607b30ce181067e8b99`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:26 GMT
ADD file:c80bc2b093cbc0fc466582ef21cbed377de9fa874aedbf320079525ddacd1200 in / 
# Tue, 15 Jun 2021 22:57:26 GMT
CMD ["/bin/sh"]
# Fri, 25 Jun 2021 20:24:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 25 Jun 2021 20:24:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 25 Jun 2021 20:24:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 25 Jun 2021 20:24:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 25 Jun 2021 20:24:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 25 Jun 2021 20:24:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Jun 2021 20:24:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 25 Jun 2021 20:24:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 25 Jun 2021 20:46:27 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 25 Jun 2021 20:46:27 GMT
ENV PHP_VERSION=8.0.7
# Fri, 25 Jun 2021 20:46:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.7.tar.xz.asc
# Fri, 25 Jun 2021 20:46:28 GMT
ENV PHP_SHA256=d5fc2e4fc780a32404d88c360e3e0009bc725d936459668e9c2ac992f2d83654
# Mon, 28 Jun 2021 19:28:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 28 Jun 2021 19:28:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 28 Jun 2021 19:32:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 28 Jun 2021 19:32:35 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Mon, 28 Jun 2021 19:32:37 GMT
RUN docker-php-ext-enable sodium
# Mon, 28 Jun 2021 19:32:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 28 Jun 2021 19:32:38 GMT
CMD ["php" "-a"]
# Tue, 29 Jun 2021 00:18:21 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Tue, 29 Jun 2021 00:18:47 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Tue, 29 Jun 2021 00:18:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Tue, 29 Jun 2021 00:18:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 29 Jun 2021 00:18:50 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 29 Jun 2021 00:18:50 GMT
ENV COMPOSER_VERSION=2.1.3
# Tue, 29 Jun 2021 00:18:54 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer   ;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Tue, 29 Jun 2021 00:18:54 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Tue, 29 Jun 2021 00:18:55 GMT
WORKDIR /app
# Tue, 29 Jun 2021 00:18:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Jun 2021 00:18:56 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b4c9a0924271af3466de27804af26420eb58da1466e7eaaba127d178b380fea3`  
		Last Modified: Tue, 15 Jun 2021 22:58:47 GMT  
		Size: 2.6 MB (2624382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411dc0806d54beedd45c3e6d1814db7830a94745ded590fddb5eec612eb4ce56`  
		Last Modified: Fri, 25 Jun 2021 22:14:45 GMT  
		Size: 1.7 MB (1696498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fe090960562d5408f115030d7f6a3f8ad309e80bee624bae2c5892430223742`  
		Last Modified: Fri, 25 Jun 2021 22:14:44 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32badd5b1b231457cca8294bb037ac5934d05179796d1eb08a6495f69ad56cab`  
		Last Modified: Fri, 25 Jun 2021 22:14:44 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c961d06010437d11428a067ed6039260a428e97078c1c1c3ca450a41016307c8`  
		Last Modified: Mon, 28 Jun 2021 21:03:53 GMT  
		Size: 10.8 MB (10788802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45610323e4ff5ac409cebe8de21d49ee446fabbc8ad7eb828385922e6d2e6e9b`  
		Last Modified: Mon, 28 Jun 2021 21:03:51 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bec539358dfdfa52455d81158ddaf2754ba312477cf40fbcf241ce9512e626`  
		Last Modified: Mon, 28 Jun 2021 21:03:59 GMT  
		Size: 13.6 MB (13602931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8006ae5abe31605d33ad4f5e21f09939deb351b66d0b42f4c77bd3a3a32ba805`  
		Last Modified: Mon, 28 Jun 2021 21:03:51 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da3df8b8e177d415814aeede9a2d4d754be5206bb4dcbab24c8b2a10948f7e0`  
		Last Modified: Mon, 28 Jun 2021 21:03:51 GMT  
		Size: 17.8 KB (17794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae18b5eb4525fac45365e8e0f94c75bb179ad4a35d8534cb15c2c163ddd47be3`  
		Last Modified: Tue, 29 Jun 2021 00:20:22 GMT  
		Size: 29.9 MB (29933762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8e8905d5760a84963a369c7dabea42e9f0f187c13b66712e706240eca54cf9`  
		Last Modified: Tue, 29 Jun 2021 00:19:57 GMT  
		Size: 196.1 KB (196064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800fb0ce310df06e33834fe1d8e01740ee7aceab6ca4d79c0af10250ff44795a`  
		Last Modified: Tue, 29 Jun 2021 00:19:57 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca924d979fe3f9b8edb798e39875c27c2963d9c373534265a1a0cabf32824cd`  
		Last Modified: Tue, 29 Jun 2021 00:19:58 GMT  
		Size: 554.5 KB (554510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfb09399bebf9ec214637c48e85959b4edf9ed474c5e761c9e4db7b20dd09dd`  
		Last Modified: Tue, 29 Jun 2021 00:19:57 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc7671888b419e1beb7e30b11f355e69f498bd19fd4daafb949e4393a84933d`  
		Last Modified: Tue, 29 Jun 2021 00:19:57 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:65db4e4221fda909dc743ed0d15b4af7a06907ec14972bc7d8d6fb5df808d072
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56790722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f350074f90a9add4279bcdf9ea481cec58630d5c6fb10a4ea4b74ca57d54ad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 15 Jun 2021 23:15:05 GMT
ADD file:416a8b507abdc6bdcb22997a4be0a4170796c3f9f77e315b2dbff2b0a212bc68 in / 
# Tue, 15 Jun 2021 23:15:06 GMT
CMD ["/bin/sh"]
# Wed, 23 Jun 2021 08:42:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 23 Jun 2021 08:42:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 23 Jun 2021 08:42:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 23 Jun 2021 08:42:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 23 Jun 2021 08:42:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 23 Jun 2021 08:42:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Jun 2021 08:42:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 23 Jun 2021 08:42:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 23 Jun 2021 09:22:06 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 23 Jun 2021 09:22:07 GMT
ENV PHP_VERSION=8.0.7
# Wed, 23 Jun 2021 09:22:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.7.tar.xz.asc
# Wed, 23 Jun 2021 09:22:08 GMT
ENV PHP_SHA256=d5fc2e4fc780a32404d88c360e3e0009bc725d936459668e9c2ac992f2d83654
# Mon, 28 Jun 2021 20:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 28 Jun 2021 20:53:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 28 Jun 2021 20:57:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 28 Jun 2021 20:57:31 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Mon, 28 Jun 2021 20:57:33 GMT
RUN docker-php-ext-enable sodium
# Mon, 28 Jun 2021 20:57:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 28 Jun 2021 20:57:34 GMT
CMD ["php" "-a"]
# Tue, 29 Jun 2021 05:27:16 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Tue, 29 Jun 2021 05:27:40 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Tue, 29 Jun 2021 05:27:42 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Tue, 29 Jun 2021 05:27:42 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 29 Jun 2021 05:27:42 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 29 Jun 2021 05:27:43 GMT
ENV COMPOSER_VERSION=2.1.3
# Tue, 29 Jun 2021 05:27:47 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer   ;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Tue, 29 Jun 2021 05:27:47 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Tue, 29 Jun 2021 05:27:48 GMT
WORKDIR /app
# Tue, 29 Jun 2021 05:27:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Jun 2021 05:27:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:136482bf81d1fa351b424ebb8c7e34d15f2c5ed3fc0b66b544b8312bda3d52d9`  
		Last Modified: Tue, 15 Jun 2021 23:16:40 GMT  
		Size: 2.4 MB (2427917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1185f00838acc4bd6c4bfdbfdd1b3b8b68fc8500c1d8393fdcc5bd8846c452da`  
		Last Modified: Fri, 25 Jun 2021 21:25:06 GMT  
		Size: 1.6 MB (1564529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5362957231a188851bc9f0b7a86718fd0561376062ac2198e3d325660d73168`  
		Last Modified: Fri, 25 Jun 2021 21:25:05 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b284c21ad15282e61562b8098064c462bfe0395c2e3de85a1b7f5fa6394e9474`  
		Last Modified: Fri, 25 Jun 2021 21:25:05 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e52e67bb46ca22bd547e228246ce43a44d932010cc5370b639b26d27cfb435a`  
		Last Modified: Mon, 28 Jun 2021 23:36:17 GMT  
		Size: 10.8 MB (10788799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d1cbb6918216cc829b71debd911f7dc05404a38e5b8ae5d85c4235bea7fa356`  
		Last Modified: Mon, 28 Jun 2021 23:36:14 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad90bb74f8801071e5a4c009f167bef6cc921283bb870f0467ba74dc1cd9666d`  
		Last Modified: Mon, 28 Jun 2021 23:36:24 GMT  
		Size: 12.7 MB (12738286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36fb1fabc683a2a81951637df8abcebb4cb6f8e69f93090b8642997e0dfdf14`  
		Last Modified: Mon, 28 Jun 2021 23:36:14 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0229d058663c9510dc70b63ae077ba5959197091f23d49de3c3c63efe7534436`  
		Last Modified: Mon, 28 Jun 2021 23:36:14 GMT  
		Size: 17.8 KB (17786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380eb9e9d97fdca0788d55e71f1d2a2c3277976c6d0fd2abe958a100ac507028`  
		Last Modified: Tue, 29 Jun 2021 05:29:14 GMT  
		Size: 28.5 MB (28505050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e507436fb109d24329f202332a3c92abbf165b5f1cb6dfcea56624162feb7e08`  
		Last Modified: Tue, 29 Jun 2021 05:28:51 GMT  
		Size: 188.8 KB (188755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0cff1e398053e001fffdc8cee5d35d290b614ddb66397c63a506fa8a086808`  
		Last Modified: Tue, 29 Jun 2021 05:28:51 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12cb3fb530feeabf0b9f2ed4533c5990609c80fcdb044fe7f9bf3e1707e5d7a`  
		Last Modified: Tue, 29 Jun 2021 05:28:51 GMT  
		Size: 554.5 KB (554519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8b52dcf5f92ce9c573632d24428df2a1dec9b52a760b3d4a3cce8a9a6712f7`  
		Last Modified: Tue, 29 Jun 2021 05:28:51 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7548fe867947de7a8feffb593ed58b1fb213f05aca722ff14cb13496cc19a7`  
		Last Modified: Tue, 29 Jun 2021 05:28:51 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:c5d9d847f9e72a6c50f321589a0dd2e7a5abf18b062e57c1335299fef1071e35
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (61027344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6c1beea82b620b2eeed13bb1bdec7e867c0d2122efef5aa3cc38bf8c9e7cb3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 15 Jun 2021 21:44:56 GMT
ADD file:6797caacbfe41bfe44000b39ed017016c6fcc492b3d6557cdaba88536df6c876 in / 
# Tue, 15 Jun 2021 21:44:56 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 22:42:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Jun 2021 22:42:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 16 Jun 2021 22:42:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 16 Jun 2021 22:42:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Jun 2021 22:42:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 16 Jun 2021 22:42:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Jun 2021 22:42:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Jun 2021 22:42:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Jun 2021 22:46:39 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 16 Jun 2021 22:46:40 GMT
ENV PHP_VERSION=8.0.7
# Wed, 16 Jun 2021 22:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.7.tar.xz.asc
# Wed, 16 Jun 2021 22:46:40 GMT
ENV PHP_SHA256=d5fc2e4fc780a32404d88c360e3e0009bc725d936459668e9c2ac992f2d83654
# Mon, 28 Jun 2021 20:46:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 28 Jun 2021 20:46:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 28 Jun 2021 20:50:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 28 Jun 2021 20:50:55 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Mon, 28 Jun 2021 20:50:57 GMT
RUN docker-php-ext-enable sodium
# Mon, 28 Jun 2021 20:50:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 28 Jun 2021 20:50:57 GMT
CMD ["php" "-a"]
# Tue, 29 Jun 2021 00:50:41 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Tue, 29 Jun 2021 00:50:51 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Tue, 29 Jun 2021 00:50:52 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Tue, 29 Jun 2021 00:50:52 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 29 Jun 2021 00:50:53 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 29 Jun 2021 00:50:53 GMT
ENV COMPOSER_VERSION=2.1.3
# Tue, 29 Jun 2021 00:50:56 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer   ;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Tue, 29 Jun 2021 00:50:56 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Tue, 29 Jun 2021 00:50:56 GMT
WORKDIR /app
# Tue, 29 Jun 2021 00:50:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 29 Jun 2021 00:50:57 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:58ab47519297212468320b23b8100fc1b2b96e8d342040806ae509a778a0a07a`  
		Last Modified: Tue, 15 Jun 2021 21:46:03 GMT  
		Size: 2.7 MB (2709626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1dbb31d082d4e4f90933b28b4719802e03a2261dafc489b60e4c94dd8f4e56a`  
		Last Modified: Fri, 25 Jun 2021 20:47:47 GMT  
		Size: 1.7 MB (1709425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:681ea156e05a3343d484d4b75ca6196085b59763b04185e7a76b8c4a5b355568`  
		Last Modified: Fri, 25 Jun 2021 20:47:47 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19e1c9b66e33460d7ebc60517e350c7107ee8977e3f6b05d2be0a44b4758d1c6`  
		Last Modified: Fri, 25 Jun 2021 20:47:46 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0618f95dc30e115563a2f797004f51b504754ceef3bb67eeef0aa34e50dbf8`  
		Last Modified: Mon, 28 Jun 2021 22:58:32 GMT  
		Size: 10.8 MB (10788801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb51af703e51f2ca3406bd505f9664ab29fa8c61b960ff4c8caae933f2d4f417`  
		Last Modified: Mon, 28 Jun 2021 22:58:31 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5c54f00a9cb8d892a8105ee63cd434e4955ff433ebb9b7a97c7b39759a7c20`  
		Last Modified: Mon, 28 Jun 2021 22:58:34 GMT  
		Size: 14.4 MB (14394468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0630b0e6004b51aab9aa0a598b2ec5d6a0edaac92f7edbf757d755d658e44950`  
		Last Modified: Mon, 28 Jun 2021 22:58:32 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed0e6a9a155e3b92047cdb47d1e78528189db8b2a4dd038e623f2fab61a34d1`  
		Last Modified: Mon, 28 Jun 2021 22:58:31 GMT  
		Size: 17.8 KB (17789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f3409bbbaae1a18486bc600f4f004561a567127503fd5b3b91e7900c0a8e3b`  
		Last Modified: Tue, 29 Jun 2021 00:51:41 GMT  
		Size: 30.6 MB (30649366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff66da4166dc9aba72885da1f6509f6fa0348551d31e3f6dc551926339952fc`  
		Last Modified: Tue, 29 Jun 2021 00:51:32 GMT  
		Size: 198.3 KB (198266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbdd0eae47ca2899a6f2a0a552c5f49b321e6a5df00f0a98efbec3b7ca987e7a`  
		Last Modified: Tue, 29 Jun 2021 00:51:32 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc047999b0b793987d0c32df3e7b823f02d81537f1d2eb55d74fa679e4af3940`  
		Last Modified: Tue, 29 Jun 2021 00:51:32 GMT  
		Size: 554.5 KB (554520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880997176492b13fbd7f1412ba98d87711b83bb45fdd86c840c1afc3836e3ae3`  
		Last Modified: Tue, 29 Jun 2021 00:51:32 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e7738d6ff54b8ab07a7a35f0119657f1c1d98168d8bfb2ce4083a5435df979`  
		Last Modified: Tue, 29 Jun 2021 00:51:32 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:4e02e46ed491da94fe6208449f23bbe2e2c1e2a1b9133b66d659313ac2ec6735
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64112372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b774738d9ed1e3b862eb23e484734c85512fb40e0f82e8b7e8640d514edaca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:38:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Apr 2021 03:38:46 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Apr 2021 03:38:47 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Apr 2021 03:38:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Apr 2021 03:38:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 15 Apr 2021 03:38:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 03:38:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Apr 2021 03:38:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Apr 2021 03:38:49 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 04 Jun 2021 19:14:53 GMT
ENV PHP_VERSION=8.0.7
# Fri, 04 Jun 2021 19:14:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.7.tar.xz.asc
# Fri, 04 Jun 2021 19:14:53 GMT
ENV PHP_SHA256=d5fc2e4fc780a32404d88c360e3e0009bc725d936459668e9c2ac992f2d83654
# Fri, 04 Jun 2021 19:15:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Jun 2021 19:15:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Jun 2021 19:25:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Jun 2021 19:25:19 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 04 Jun 2021 19:25:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Jun 2021 19:25:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Jun 2021 19:25:22 GMT
CMD ["php" "-a"]
# Fri, 04 Jun 2021 20:42:45 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 04 Jun 2021 20:42:56 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Fri, 04 Jun 2021 20:42:57 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 04 Jun 2021 20:42:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 04 Jun 2021 20:42:57 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 10 Jun 2021 17:38:29 GMT
ENV COMPOSER_VERSION=2.1.3
# Thu, 10 Jun 2021 17:38:32 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer   ;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Thu, 10 Jun 2021 17:38:32 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Thu, 10 Jun 2021 17:38:33 GMT
WORKDIR /app
# Thu, 10 Jun 2021 17:38:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 10 Jun 2021 17:38:33 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3818e7e8eb8d9c0ab0e377e89ed7df3037ec2c0d4c4c89bd3a2abedc459366c`  
		Last Modified: Thu, 15 Apr 2021 05:57:45 GMT  
		Size: 1.8 MB (1799274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274cbc3732aca6ca32c0ba51f7504eb2d19d4fd52d0f89f9ff2597a673484be8`  
		Last Modified: Thu, 15 Apr 2021 05:57:43 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32aa0b7923dc47bd54c1e8cc895686f0638c3a28a9a40f8ed831545df00ce891`  
		Last Modified: Thu, 15 Apr 2021 05:57:46 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c11bf4cbd32494a063621f918fa784556315a314c6d78e5d19dbfc8bd942ab0`  
		Last Modified: Fri, 04 Jun 2021 19:58:41 GMT  
		Size: 10.8 MB (10788550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7825c7bdb9d266701c9228b54056b249ead9c87bb7c598cc697b4e9129cacaae`  
		Last Modified: Fri, 04 Jun 2021 19:58:39 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fc4bd5e9a72405e0b9d3bcdbe0b7262e762c791870713d50bef19042426075`  
		Last Modified: Fri, 04 Jun 2021 19:58:44 GMT  
		Size: 15.6 MB (15569700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909ee12d174e4a1b14451096ba719a4ee697691d0d87bca3bbc007780ac8b9d1`  
		Last Modified: Fri, 04 Jun 2021 19:58:39 GMT  
		Size: 2.3 KB (2264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0db7581e2c6a9e29181306bc72b568bcd37d34d86e82848ab39e9339e1402e8`  
		Last Modified: Fri, 04 Jun 2021 19:58:40 GMT  
		Size: 17.6 KB (17588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a68082e643a7fc161f84cc28dc2bf16a7887e2d4308bd28ecc6fe8b8629886`  
		Last Modified: Fri, 04 Jun 2021 20:43:48 GMT  
		Size: 32.3 MB (32344854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a803220d3be252a04d891ac0da77a9f2ea0f49316dcace07e32952ece50fa6`  
		Last Modified: Fri, 04 Jun 2021 20:43:38 GMT  
		Size: 213.9 KB (213906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03742a6d31e0579e49ad310eef763db9a43325091247f01681d12fb81eccc71`  
		Last Modified: Fri, 04 Jun 2021 20:43:38 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd3b7f2db5bc1d340325eeb496287221d43e4ca8251f3bb179744bf7d8cf603a`  
		Last Modified: Thu, 10 Jun 2021 17:39:01 GMT  
		Size: 554.5 KB (554520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63498ecde104628b29fe215bb8920fba90808cbcbe53ae3509376ba3f7319ba3`  
		Last Modified: Thu, 10 Jun 2021 17:39:01 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c476d4a236204c45b6b1aad0808d984df1ec4a7410c75ae462adfc04487296eb`  
		Last Modified: Thu, 10 Jun 2021 17:39:01 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:d6b54ebb2e8fa6bb533ec411f0d83331940ff6c2abec1618f11b5b41d6977aea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64517569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1fd25998deb6c63fcb1615dbdd87eee42b799ad52c82adaf8246f2acc20091e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 14 Apr 2021 19:30:57 GMT
ADD file:52162c4413e3597dad4ccb790c379b67ef40d50c0d0659e8b6c65d833886b3af in / 
# Wed, 14 Apr 2021 19:31:02 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:15:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Apr 2021 20:15:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Apr 2021 20:16:09 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Apr 2021 20:16:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Apr 2021 20:16:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 14 Apr 2021 20:16:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 20:16:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 20:16:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Apr 2021 20:16:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 04 Jun 2021 18:51:21 GMT
ENV PHP_VERSION=8.0.7
# Fri, 04 Jun 2021 18:51:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.7.tar.xz.asc
# Fri, 04 Jun 2021 18:51:35 GMT
ENV PHP_SHA256=d5fc2e4fc780a32404d88c360e3e0009bc725d936459668e9c2ac992f2d83654
# Fri, 04 Jun 2021 18:52:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Jun 2021 18:52:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Jun 2021 18:57:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Jun 2021 18:57:15 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 04 Jun 2021 18:57:27 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Jun 2021 18:57:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Jun 2021 18:57:34 GMT
CMD ["php" "-a"]
# Sun, 27 Jun 2021 10:23:12 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Sun, 27 Jun 2021 10:23:48 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Sun, 27 Jun 2021 10:23:57 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Sun, 27 Jun 2021 10:24:00 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sun, 27 Jun 2021 10:24:03 GMT
ENV COMPOSER_HOME=/tmp
# Sun, 27 Jun 2021 10:24:05 GMT
ENV COMPOSER_VERSION=2.1.3
# Sun, 27 Jun 2021 10:24:18 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer   ;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Sun, 27 Jun 2021 10:24:20 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Sun, 27 Jun 2021 10:24:22 GMT
WORKDIR /app
# Sun, 27 Jun 2021 10:24:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 27 Jun 2021 10:24:31 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:771d2590aa602a0d4a922e322f02b22cc9d193f8cd159d9d1a140cadf1f8b4d4`  
		Last Modified: Wed, 14 Apr 2021 19:32:33 GMT  
		Size: 2.8 MB (2813141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18b4999d98214ab55ea75ff5caca694bebb5bb07f5c23e9a6f4ce900ce4c2c6`  
		Last Modified: Wed, 14 Apr 2021 22:01:00 GMT  
		Size: 1.7 MB (1748637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8118faf424e03fa2a7d0df76aa1813928f5598c3bdd1b390629452fd95766a66`  
		Last Modified: Wed, 14 Apr 2021 22:00:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc86fc5a1b429a1fd2c88a0a1f7506b2543ae32ff0ba83f0ba697a84dafa2ded`  
		Last Modified: Wed, 14 Apr 2021 22:00:59 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47dd0c0035f66b942fab95a9bff27bbaa9ccf2143e86a55115a98567409c0158`  
		Last Modified: Fri, 04 Jun 2021 19:23:19 GMT  
		Size: 10.8 MB (10788562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6047a06cd7e51c04e58caeaf149ac3a88ef059b697207aae09c60572d1f10ebd`  
		Last Modified: Fri, 04 Jun 2021 19:23:17 GMT  
		Size: 500.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8668b02c0671faa2d1441782a8bc0bd19680d34260439004c5f9d7d46a03e4f`  
		Last Modified: Fri, 04 Jun 2021 19:23:22 GMT  
		Size: 15.9 MB (15937483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea043a8677f6d6d714cd12528a1799539ea77b319d9bbe41f7155afd182d41d`  
		Last Modified: Fri, 04 Jun 2021 19:23:17 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52406ae5896026414e86ec12df77e36d4c86dabe2cd7b4f851bffa64c9d28f27`  
		Last Modified: Fri, 04 Jun 2021 19:23:17 GMT  
		Size: 17.6 KB (17608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134e7ac0974cc16fde6ea96b8d246c22107c38c1045515bdd2a65648e7238c2c`  
		Last Modified: Sun, 27 Jun 2021 10:25:46 GMT  
		Size: 32.1 MB (32055069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9904504c24d0ef48bd22dd0c862649d4740545ed23eec549f60992536c8af1af`  
		Last Modified: Sun, 27 Jun 2021 10:25:37 GMT  
		Size: 597.5 KB (597467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71ac70e50f639b82efba1975e35c23c8bdb5aaf6eafe77b4bb1b530b9fc5263`  
		Last Modified: Sun, 27 Jun 2021 10:25:36 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55efb487c49510be7dbed642cf8617f3314be1dafa44d58748993941e9ca441a`  
		Last Modified: Sun, 27 Jun 2021 10:25:37 GMT  
		Size: 554.5 KB (554515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2f24f2cddd751030a0310cea305da2a2f09f2b6f4d569d45014d900ccee95e`  
		Last Modified: Sun, 27 Jun 2021 10:25:36 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32091b86632617172bb5971051aab18fd573b1c5dfd6705285271f1b4bef7eb`  
		Last Modified: Sun, 27 Jun 2021 10:25:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:601a2eb4c847d729af5221f5afe8e27f65c8461b6a66e4eae8441c4cbf34a003
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61999266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d145c4e5d7d842baecbaaac2a6c65c4911894a104e27bdd35cd4ac23125d60a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:35 GMT
ADD file:c715fef757fe2b022ae1bbff71dbc58bddf5a858deb0aac5a6fbcf10d5f3111c in / 
# Wed, 14 Apr 2021 18:41:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:00:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Apr 2021 19:00:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Apr 2021 19:00:56 GMT
RUN set -eux; 	addgroup -g 82 -S www-data; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Apr 2021 19:00:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Apr 2021 19:00:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 14 Apr 2021 19:00:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 19:00:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Apr 2021 19:00:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Apr 2021 19:00:59 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 04 Jun 2021 19:04:59 GMT
ENV PHP_VERSION=8.0.7
# Fri, 04 Jun 2021 19:04:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.7.tar.xz.asc
# Fri, 04 Jun 2021 19:04:59 GMT
ENV PHP_SHA256=d5fc2e4fc780a32404d88c360e3e0009bc725d936459668e9c2ac992f2d83654
# Fri, 04 Jun 2021 19:05:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 04 Jun 2021 19:05:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 04 Jun 2021 19:10:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 04 Jun 2021 19:10:36 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 04 Jun 2021 19:10:39 GMT
RUN docker-php-ext-enable sodium
# Fri, 04 Jun 2021 19:10:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 04 Jun 2021 19:10:40 GMT
CMD ["php" "-a"]
# Sun, 27 Jun 2021 13:10:04 GMT
RUN set -eux;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Sun, 27 Jun 2021 13:10:20 GMT
RUN set -eux;   apk add --no-cache --virtual .build-deps     libzip-dev     zlib-dev   ;   docker-php-ext-install -j "$(nproc)"     zip   ;   runDeps="$(     scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions       | tr ',' '\n'       | sort -u       | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }'     )";   apk add --no-cache --virtual .composer-phpext-rundeps $runDeps;   apk del .build-deps
# Sun, 27 Jun 2021 13:10:21 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Sun, 27 Jun 2021 13:10:21 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sun, 27 Jun 2021 13:10:22 GMT
ENV COMPOSER_HOME=/tmp
# Sun, 27 Jun 2021 13:10:22 GMT
ENV COMPOSER_VERSION=2.1.3
# Sun, 27 Jun 2021 13:10:24 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/cb19f2aa3aeaa2006c0cd69a7ef011eb31463067/web/installer   ;   php -r "     \$signature = '48e3236262b34d30969dca3c37281b3b4bbe3221bda826ac6a9a62d6444cdb0dcd0615698a5cbe587c3f0fe57a54d8f5';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Sun, 27 Jun 2021 13:10:24 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Sun, 27 Jun 2021 13:10:25 GMT
WORKDIR /app
# Sun, 27 Jun 2021 13:10:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sun, 27 Jun 2021 13:10:25 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:afadee6ad6a38d3172beeeca818219604c782efbe93201ef4d39512f289b05ae`  
		Last Modified: Wed, 14 Apr 2021 18:42:16 GMT  
		Size: 2.6 MB (2602650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d300c94e92b07eb0727117362a4c02c33a3af45a2c84e27e191b18fd64537ff2`  
		Last Modified: Wed, 14 Apr 2021 20:01:05 GMT  
		Size: 1.8 MB (1760701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c222b785aeace308f4ae843bd963ab89b5e43b40c39e44819a79a97ab65ffd`  
		Last Modified: Wed, 14 Apr 2021 20:01:04 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdca579f326f21cb64727b7a043ef139e61e18d78e009c7aaa0d00c8787d500`  
		Last Modified: Wed, 14 Apr 2021 20:01:04 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe6e68029a9d4aa3de94bcd1c7351e4d7e3ba199bbaf9266b32c85a95413ba1`  
		Last Modified: Fri, 04 Jun 2021 19:31:01 GMT  
		Size: 10.8 MB (10788566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eea44cf0ed3b67e9363eeba2ea08f57d69eac8f4bf27e04f949a3df344064e4`  
		Last Modified: Fri, 04 Jun 2021 19:31:00 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6caee3485f44f47a6f791419c9a45426bffc883a41a816b98317146bf013fbf`  
		Last Modified: Fri, 04 Jun 2021 19:31:03 GMT  
		Size: 14.2 MB (14233345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c03406abb4d60276c7555e3a655d2173e889fc8bc056e64dbaa70cfbca28dcc`  
		Last Modified: Fri, 04 Jun 2021 19:31:00 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec95014943a4afed7accb8e6f39dde96d0ebdf27de094f6657275119c232f7e`  
		Last Modified: Fri, 04 Jun 2021 19:31:00 GMT  
		Size: 17.6 KB (17601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f96847f9e73930bd8dda67dc55b8ce3d6cdae893861aa09d0cd62c9a43218909`  
		Last Modified: Sun, 27 Jun 2021 13:11:08 GMT  
		Size: 31.4 MB (31440522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba7b46eda83254b5a1afe337796979dbfcf0f75a9e34172db1839a3626c8aa0`  
		Last Modified: Sun, 27 Jun 2021 13:11:02 GMT  
		Size: 596.3 KB (596288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1396ff83b2ac97142e0c045955e32c10498e563905107e3a11e6978ce82a23`  
		Last Modified: Sun, 27 Jun 2021 13:11:02 GMT  
		Size: 259.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8fa9c58a007225c49162943c93d73a00c77218d84b47b8308fcee681a283b3`  
		Last Modified: Sun, 27 Jun 2021 13:11:03 GMT  
		Size: 554.5 KB (554512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc86302054c3e5310c3784fb2537bf2462d3bf0590471ad88e27df7e54421aca`  
		Last Modified: Sun, 27 Jun 2021 13:11:02 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd8e38b7197c6705d28a4e909a8508b53f499281dd0a28f45797a6d3429dd26`  
		Last Modified: Sun, 27 Jun 2021 13:11:02 GMT  
		Size: 124.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
