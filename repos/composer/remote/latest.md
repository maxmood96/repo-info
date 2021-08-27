## `composer:latest`

```console
$ docker pull composer@sha256:960bddac10e31cddaaecfc95a746489c582cf8da0d798b5b6cf761746908bd96
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

### `composer:latest` - linux; amd64

```console
$ docker pull composer@sha256:1ec3ac1304d9b5b09ecc727491e58d2d07d1429c16c9d70d948700068cf85a8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67177181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0e160b773437a6dab7eb418edc381e8d5ee1264c700a5e7fa20745ba7ef7576`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Aug 2021 17:19:45 GMT
ADD file:34eb5c40aa00028921a224d1764ae1b1f3ef710d191e4dfc7df55e0594aa7217 in / 
# Fri, 06 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 22:50:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 22:50:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 22:50:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 22:50:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 22:50:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 22:50:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 22:50:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 22:50:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 23:09:01 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 26 Aug 2021 22:44:55 GMT
ENV PHP_VERSION=8.0.10
# Thu, 26 Aug 2021 22:44:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Thu, 26 Aug 2021 22:44:55 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Thu, 26 Aug 2021 22:45:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Aug 2021 22:45:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 22:54:47 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 22:54:47 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 26 Aug 2021 22:54:49 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 22:54:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 22:54:49 GMT
CMD ["php" "-a"]
# Fri, 27 Aug 2021 04:55:06 GMT
RUN set -eux;   apk upgrade --no-cache;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Aug 2021 04:55:07 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/edf2c4d40de3b86cc1a6e1877eaede05be016389/install-php-extensions;   echo 2c3e48c01d5346be2c6cdd8d6f0a754f107d1119960b3f9d7cad0cae3ac663fb3646eab890310f89aeb3066460fee712034c0f5537608996f9a9f5f413992528 /usr/local/bin/install-php-extensions | sha512sum --strict --check;   chmod +x /usr/local/bin/install-php-extensions
# Fri, 27 Aug 2021 04:55:37 GMT
RUN set -eux;   install-php-extensions     bz2     zip
# Fri, 27 Aug 2021 04:55:38 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Aug 2021 04:55:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Aug 2021 04:55:38 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Aug 2021 04:55:39 GMT
ENV COMPOSER_VERSION=2.1.6
# Fri, 27 Aug 2021 04:55:41 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   php -r "     \$signature = '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Aug 2021 04:55:42 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 27 Aug 2021 04:55:42 GMT
WORKDIR /app
# Fri, 27 Aug 2021 04:55:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Aug 2021 04:55:42 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:29291e31a76a7e560b9b7ad3cada56e8c18d50a96cca8a2573e4f4689d7aca77`  
		Last Modified: Thu, 05 Aug 2021 15:56:25 GMT  
		Size: 2.8 MB (2813006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40df5ce4894c4fe544404fe34e6bb75518b0ae8c6b90819795e09750e8023bc5`  
		Last Modified: Sat, 07 Aug 2021 00:01:43 GMT  
		Size: 1.7 MB (1707767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42904e0b354067c595d0b768fd0ec45eb21ec15058a815b60ade71ee430d732`  
		Last Modified: Sat, 07 Aug 2021 00:01:43 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49b0bef73260aa884024d4812378dc7458a626d07690e51be1b680ac2ae2dcb4`  
		Last Modified: Sat, 07 Aug 2021 00:01:43 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fda387c57f2da2b07f40d366d26f9a081adc0a4e212de33b35ef3169f38cc5`  
		Last Modified: Fri, 27 Aug 2021 03:20:08 GMT  
		Size: 10.7 MB (10722812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b290d8ba05dea009b3aec7842f841320e5ca7ebfdcb475ad2b6d32d43f027ee6`  
		Last Modified: Fri, 27 Aug 2021 03:20:07 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f449028f4c98267d02ace8528e8abdc3eaf05aef3e26598b45ed1e49b4cd21`  
		Last Modified: Fri, 27 Aug 2021 03:20:11 GMT  
		Size: 16.6 MB (16608978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc29acf46b9dec7f9c7717291bba5a43ec37d43a4534cacf41d05764b88599f0`  
		Last Modified: Fri, 27 Aug 2021 03:20:06 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60480898d1f83a06e245755081c2d8b78d4b7a13f19b4a9125fb58100c57185`  
		Last Modified: Fri, 27 Aug 2021 03:20:07 GMT  
		Size: 17.8 KB (17839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1990f98c616a1cc8dd5df1bc7cbcb098769ee341d75fd5a73341743bc2a6fa4`  
		Last Modified: Fri, 27 Aug 2021 04:56:17 GMT  
		Size: 34.5 MB (34513685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e896ecb33b3d3706c10326ce4a2e71b58ab2040d8d8e0abe99b579b6722f63cd`  
		Last Modified: Fri, 27 Aug 2021 04:56:11 GMT  
		Size: 19.3 KB (19334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ec31d9b6bca12ee8fd0aeb6ae963ca8dad5229433413d533a5991acfa4094c8`  
		Last Modified: Fri, 27 Aug 2021 04:56:08 GMT  
		Size: 213.0 KB (212951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0932f5b24f1144a1e3c315fe5dd939d6c44ca6e3590f9bf5597f3b1bd099e5`  
		Last Modified: Fri, 27 Aug 2021 04:56:08 GMT  
		Size: 255.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff25658f745b8ec9355e9882a9551d92c65a23f9bc546d2bd71a9c8b7e00228`  
		Last Modified: Fri, 27 Aug 2021 04:56:08 GMT  
		Size: 555.7 KB (555732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b6af13ffe224db22d53fc811ef90c7e298ce0f366edb27b0cf8549bd7be326`  
		Last Modified: Fri, 27 Aug 2021 04:56:08 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6d3a57133cc10d960c54c166f2b31809ca6a1189006aaf308f2b7d1b1e550c`  
		Last Modified: Fri, 27 Aug 2021 04:56:08 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:9024871a5b4d5f6197bc3ca876ec47d722193cdfb7437a3777029e65cb4fe1ef
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62822924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0d60f14d06a7cf85a44c6c8072fa8a39e60b70b570bdfe7ea20b2268eba9978`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Aug 2021 17:49:32 GMT
ADD file:7f2c7deda009eabdcbbdccb11e854043d32c498e64e7e1ca02165d7bb4261d39 in / 
# Fri, 06 Aug 2021 17:49:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 20:25:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 20:25:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 20:25:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 20:25:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 20:25:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 20:25:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 20:25:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 20:25:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 20:35:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 26 Aug 2021 21:37:36 GMT
ENV PHP_VERSION=8.0.10
# Thu, 26 Aug 2021 21:37:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Thu, 26 Aug 2021 21:37:37 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Thu, 26 Aug 2021 21:37:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Aug 2021 21:37:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:42:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 21:42:27 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 26 Aug 2021 21:42:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 21:42:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 21:42:31 GMT
CMD ["php" "-a"]
# Fri, 27 Aug 2021 01:37:29 GMT
RUN set -eux;   apk upgrade --no-cache;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Aug 2021 01:37:31 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/edf2c4d40de3b86cc1a6e1877eaede05be016389/install-php-extensions;   echo 2c3e48c01d5346be2c6cdd8d6f0a754f107d1119960b3f9d7cad0cae3ac663fb3646eab890310f89aeb3066460fee712034c0f5537608996f9a9f5f413992528 /usr/local/bin/install-php-extensions | sha512sum --strict --check;   chmod +x /usr/local/bin/install-php-extensions
# Fri, 27 Aug 2021 01:38:27 GMT
RUN set -eux;   install-php-extensions     bz2     zip
# Fri, 27 Aug 2021 01:38:29 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Aug 2021 01:38:30 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Aug 2021 01:38:30 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Aug 2021 01:38:31 GMT
ENV COMPOSER_VERSION=2.1.6
# Fri, 27 Aug 2021 01:38:35 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   php -r "     \$signature = '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Aug 2021 01:38:36 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 27 Aug 2021 01:38:36 GMT
WORKDIR /app
# Fri, 27 Aug 2021 01:38:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Aug 2021 01:38:37 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f465bb3e9fcd0c42f936ecc566c6e40353c00f3089b2b2c2ea1663c30f89d3ab`  
		Last Modified: Fri, 06 Aug 2021 17:51:00 GMT  
		Size: 2.6 MB (2626350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c308e0cc29c44fbd995ee591fe7289bde1e488176fb402318132d40caa05c299`  
		Last Modified: Fri, 06 Aug 2021 21:25:23 GMT  
		Size: 1.7 MB (1696670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983c92fbbed0d3241e2a4aa8f6ec320484791f6923f18c795878fea03971b8bd`  
		Last Modified: Fri, 06 Aug 2021 21:25:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1f89139d48debd7c21fa5272e8bb4a983181e2f8d1f37a9f65ee5c99086cd7c`  
		Last Modified: Fri, 06 Aug 2021 21:25:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80ec4769f82ce3367d73237dbdf73660e5b378e979d1ad37c5547da846d1249f`  
		Last Modified: Thu, 26 Aug 2021 23:12:55 GMT  
		Size: 10.7 MB (10722828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8d5f7bceeb387f192db3ff0941fee44d2e21fa34cc5b13624a7136839a95b1`  
		Last Modified: Thu, 26 Aug 2021 23:12:52 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b668aac95432f50545c3ef68f159d0aab1d131c1519c9a85ce31dde26bee9fd8`  
		Last Modified: Thu, 26 Aug 2021 23:13:03 GMT  
		Size: 15.0 MB (15017066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:354bed15e1d4666170b80cd35659fa482dfd187e8274e8073ec6e2ae9750c171`  
		Last Modified: Thu, 26 Aug 2021 23:12:52 GMT  
		Size: 2.3 KB (2269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7493dd89e93ccd4d8bfcefb097eb43551e469901cd13e27e77dafce9b46b73df`  
		Last Modified: Thu, 26 Aug 2021 23:12:52 GMT  
		Size: 17.9 KB (17859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5f154a95262a8681c11c9ed7140d97a0cdb343dd830cad6961bf4e0a7498bd`  
		Last Modified: Fri, 27 Aug 2021 01:40:02 GMT  
		Size: 32.0 MB (31955913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e255df132cc5e3cb549c7c109467f58ce4686674b236b5b720da602357b07ed`  
		Last Modified: Fri, 27 Aug 2021 01:39:39 GMT  
		Size: 19.3 KB (19333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff571f0990a81ceec47f9765b9cccd67292ecb3ff2d3c114308bb642da946cb`  
		Last Modified: Fri, 27 Aug 2021 01:39:37 GMT  
		Size: 206.1 KB (206101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe5d82b0d18071140dcd74c426bed634193cdb59a81e2c894253b9c9bb340bb`  
		Last Modified: Fri, 27 Aug 2021 01:39:37 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a292ad00c5c194b8661fa41a6b02c71b2ecf6dad68f8b788fbfd247b30d244ad`  
		Last Modified: Fri, 27 Aug 2021 01:39:38 GMT  
		Size: 555.7 KB (555720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2871da3de4a15fcf2350fb1685751b466710e0bfac5c5e24c08a3d620e115f65`  
		Last Modified: Fri, 27 Aug 2021 01:39:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c06e89562bb6a1bc0de60e97887f423eb3e60e5b0e49e1eb0946dfce0188c8`  
		Last Modified: Fri, 27 Aug 2021 01:39:37 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:c5f3e0f1f0f29e8d6f5fdcca12cb7fc7d849a65f9b020b17ddfa1f1fb6dc049f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59902449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd526fa92c9e2ec776456c23822f9a0028fc94bb3c4e91f7c230e39435c5b88a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Aug 2021 17:57:32 GMT
ADD file:3a35ff3ac0d80289d419a4d6d8319610c38e1936d296addafb9aaf506946230f in / 
# Fri, 06 Aug 2021 17:57:32 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 20:54:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 20:54:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 20:54:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 20:54:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 20:54:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 20:54:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 20:54:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 20:54:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 21:05:21 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 26 Aug 2021 23:16:18 GMT
ENV PHP_VERSION=8.0.10
# Thu, 26 Aug 2021 23:16:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Thu, 26 Aug 2021 23:16:19 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Thu, 26 Aug 2021 23:16:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Aug 2021 23:16:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:20:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 23:20:40 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 26 Aug 2021 23:20:43 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 23:20:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 23:20:44 GMT
CMD ["php" "-a"]
# Fri, 27 Aug 2021 06:42:25 GMT
RUN set -eux;   apk upgrade --no-cache;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Aug 2021 06:42:27 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/edf2c4d40de3b86cc1a6e1877eaede05be016389/install-php-extensions;   echo 2c3e48c01d5346be2c6cdd8d6f0a754f107d1119960b3f9d7cad0cae3ac663fb3646eab890310f89aeb3066460fee712034c0f5537608996f9a9f5f413992528 /usr/local/bin/install-php-extensions | sha512sum --strict --check;   chmod +x /usr/local/bin/install-php-extensions
# Fri, 27 Aug 2021 06:43:20 GMT
RUN set -eux;   install-php-extensions     bz2     zip
# Fri, 27 Aug 2021 06:43:21 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Aug 2021 06:43:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Aug 2021 06:43:22 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Aug 2021 06:43:23 GMT
ENV COMPOSER_VERSION=2.1.6
# Fri, 27 Aug 2021 06:43:27 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   php -r "     \$signature = '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Aug 2021 06:43:27 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 27 Aug 2021 06:43:28 GMT
WORKDIR /app
# Fri, 27 Aug 2021 06:43:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Aug 2021 06:43:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:4ee0caa23b369b04827640a4be298bf4ff7bacd030c77e915f5d7fb8f987594a`  
		Last Modified: Fri, 06 Aug 2021 17:58:57 GMT  
		Size: 2.4 MB (2429359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60e2d83b5c992b22cef3665b0ab131088923cffff86634ff4237393a231b13d`  
		Last Modified: Fri, 06 Aug 2021 22:04:23 GMT  
		Size: 1.6 MB (1564630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d851eb12a849920c3886c6a5cc4c6ff6340be6574eae5478f604b4428ab1dc3`  
		Last Modified: Fri, 06 Aug 2021 22:04:22 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7635ae9ae7b01f3f897bee725eb55f2ee4ea71056d85205467700b3d753efc`  
		Last Modified: Fri, 06 Aug 2021 22:04:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a419917ed80d278180e45865ca3c05601f8c595aa79adabcc74a892900c4da`  
		Last Modified: Fri, 27 Aug 2021 02:28:53 GMT  
		Size: 10.7 MB (10722821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f018045dfa17deeb6380de799a802c711a09a9a09f8d624421e8ecd542dacd4f`  
		Last Modified: Fri, 27 Aug 2021 02:28:49 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0982e6b1956df0317ba81e1b65fff8e13b0a2366d8e715c855a279e96ca40886`  
		Last Modified: Fri, 27 Aug 2021 02:28:59 GMT  
		Size: 14.1 MB (14078407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46744e18f05d15369a028fe8a2195000cab93fc7a6b40ea55e9a3c5e40f36d05`  
		Last Modified: Fri, 27 Aug 2021 02:28:49 GMT  
		Size: 2.3 KB (2266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04607153d9d74a4702b891c6c46764510ac44dad6ae195bcfbe1bdf4a9e738e`  
		Last Modified: Fri, 27 Aug 2021 02:28:49 GMT  
		Size: 17.8 KB (17838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cf80e905f02cc927d8a9f3ef708f9f4adc87129bd36e4945dd211244f955801`  
		Last Modified: Fri, 27 Aug 2021 06:44:58 GMT  
		Size: 30.3 MB (30310878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a42a6f53c655fafbf893d027bf95366b748690822da2fd27be25dd047ff38b6`  
		Last Modified: Fri, 27 Aug 2021 06:44:37 GMT  
		Size: 19.3 KB (19333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6526cd86e8b7ddff0f4b6caa21cff8e172971cea4a6dde2c35c67224bb2e18ca`  
		Last Modified: Fri, 27 Aug 2021 06:44:35 GMT  
		Size: 198.4 KB (198368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad56ab22a6a1b023e46ae07477b242754769fd584cbe89e62bf9532e7f60636e`  
		Last Modified: Fri, 27 Aug 2021 06:44:35 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cba0ecba4db628380a04666d53a8bee1c365bd56ace7cbd69df9113a77fbef3`  
		Last Modified: Fri, 27 Aug 2021 06:44:36 GMT  
		Size: 555.7 KB (555732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f305d29f40b7e9052aa8da4281e1f1249a480d56b3c253dcfc7647de0dfc46`  
		Last Modified: Fri, 27 Aug 2021 06:44:35 GMT  
		Size: 409.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e19f926ae3a7294f77b551174c8b1d575109d8dd9918e2f23924d79c0a5a76ab`  
		Last Modified: Fri, 27 Aug 2021 06:44:35 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:67e5b1a9272c75e5a056939eae5cb22d5e580a7a6807a5450735e743f522b101
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64707322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7628fceb119149f365ff91f24df3f11cf5f2845e0e47ba78f4838e15ddf1eb4e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Aug 2021 17:39:26 GMT
ADD file:1a8fd1066485e1261462e689c1a072f010c1d3be904b73ef2b84128fac652951 in / 
# Fri, 06 Aug 2021 17:39:27 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 22:13:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 22:13:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 22:13:46 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 22:13:46 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 22:13:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 22:13:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 22:13:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 22:13:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 22:29:25 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 27 Aug 2021 00:14:18 GMT
ENV PHP_VERSION=8.0.10
# Fri, 27 Aug 2021 00:14:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Fri, 27 Aug 2021 00:14:18 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Fri, 27 Aug 2021 00:14:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 00:14:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:19:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 00:19:18 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 27 Aug 2021 00:19:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 00:19:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 00:19:20 GMT
CMD ["php" "-a"]
# Fri, 27 Aug 2021 04:53:08 GMT
RUN set -eux;   apk upgrade --no-cache;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Aug 2021 04:53:09 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/edf2c4d40de3b86cc1a6e1877eaede05be016389/install-php-extensions;   echo 2c3e48c01d5346be2c6cdd8d6f0a754f107d1119960b3f9d7cad0cae3ac663fb3646eab890310f89aeb3066460fee712034c0f5537608996f9a9f5f413992528 /usr/local/bin/install-php-extensions | sha512sum --strict --check;   chmod +x /usr/local/bin/install-php-extensions
# Fri, 27 Aug 2021 04:53:36 GMT
RUN set -eux;   install-php-extensions     bz2     zip
# Fri, 27 Aug 2021 04:53:36 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Aug 2021 04:53:37 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Aug 2021 04:53:37 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Aug 2021 04:53:37 GMT
ENV COMPOSER_VERSION=2.1.6
# Fri, 27 Aug 2021 04:53:40 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   php -r "     \$signature = '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Aug 2021 04:53:40 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 27 Aug 2021 04:53:40 GMT
WORKDIR /app
# Fri, 27 Aug 2021 04:53:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Aug 2021 04:53:41 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fd3acdcea5682abced546ec19fb6ebee725c5184e5d91614c469c0a79e67f2d0`  
		Last Modified: Fri, 06 Aug 2021 17:40:12 GMT  
		Size: 2.7 MB (2710613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e75c04557b83c6887fa33eb52320a5c1afed1d1b8299d3accdf27cea6b5860`  
		Last Modified: Fri, 06 Aug 2021 23:19:35 GMT  
		Size: 1.7 MB (1710420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6439bb8bd6ba02680eef64ad51b996399f05a740cd7ab8e62834b24527f60c`  
		Last Modified: Fri, 06 Aug 2021 23:19:35 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d61d6c7061c67dabfce2227dc9665b59eb7c43fd2f927c11e7c76446b50fed3`  
		Last Modified: Fri, 06 Aug 2021 23:19:35 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573e88bfa4246de96a5fad37abe061ef94b135a319385e1a0f92c8d9f96ef8db`  
		Last Modified: Fri, 27 Aug 2021 02:45:17 GMT  
		Size: 10.7 MB (10722820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4b5acbe908a9bd68f6cb55cd33331e9fcdb6e6a84ef6f747c6470f47e6afd3`  
		Last Modified: Fri, 27 Aug 2021 02:45:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e379b2e166a3c56d49867ca62a4937499f9b74ec02c47639b060947d181dc45`  
		Last Modified: Fri, 27 Aug 2021 02:45:19 GMT  
		Size: 15.9 MB (15921498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919dde615f44ad49f496b62297d5544a4a75e0cd490d639fca0c27aa7c385f15`  
		Last Modified: Fri, 27 Aug 2021 02:45:16 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be68096005c38ead5788e6d45ea28fbc1226bf9e1cfbca8fe5974eb5b51beab9`  
		Last Modified: Fri, 27 Aug 2021 02:45:16 GMT  
		Size: 17.9 KB (17856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794aa822e8547387eb70e94088082e971ad7e9ee3f89f8d0f1718e79e67595b3`  
		Last Modified: Fri, 27 Aug 2021 04:54:24 GMT  
		Size: 32.8 MB (32833890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff9cee95b4aaf807a574d2726d02d7f7e5d5413c1a617a020fd0b98cb677917`  
		Last Modified: Fri, 27 Aug 2021 04:54:18 GMT  
		Size: 19.3 KB (19334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0cba8145982ce90472990759ee18265ee3d198ac1c9f8e6beda174af0b1ddf`  
		Last Modified: Fri, 27 Aug 2021 04:54:15 GMT  
		Size: 210.1 KB (210076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d6ab3dbf2d7be7ba8c6fed02699366e28768c39c3fdcb61a4031a49ab401a9`  
		Last Modified: Fri, 27 Aug 2021 04:54:15 GMT  
		Size: 258.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d56ef1a9b3fa9cfb4181a8db31315f8a312fc79b4dc2646b6cfbdf405cdede2`  
		Last Modified: Fri, 27 Aug 2021 04:54:16 GMT  
		Size: 555.7 KB (555734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d11674470758652305d17aa3a28a77de96dfd8391964bb45a09e5822339055`  
		Last Modified: Fri, 27 Aug 2021 04:54:15 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afdac17968baecc619105315ac605f58ed22865073c303148bd17cd3c3932e71`  
		Last Modified: Fri, 27 Aug 2021 04:54:15 GMT  
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
$ docker pull composer@sha256:cedae52c08ff3ec536be815a50bc56381a0bb4065e16451b053d231a0c522721
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67064025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc82748227dc1512a115f011f3d2b069a18c3c64faf9ea8839a00ed03af767d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Aug 2021 18:28:28 GMT
ADD file:40f3b617d7ff269d92f0ffcf8aad561b5f2c0626ef519a7f584f1ba0182b3188 in / 
# Fri, 06 Aug 2021 18:28:35 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 23:16:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 23:17:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 23:17:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 23:17:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 23:17:36 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 23:17:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 23:17:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 23:17:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 23:31:24 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Fri, 06 Aug 2021 23:31:27 GMT
ENV PHP_VERSION=8.0.9
# Fri, 06 Aug 2021 23:31:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.9.tar.xz.asc
# Fri, 06 Aug 2021 23:31:32 GMT
ENV PHP_SHA256=71a01b2b56544e20e28696ad5b366e431a0984eaa39aa5e35426a4843e172010
# Fri, 06 Aug 2021 23:31:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 06 Aug 2021 23:31:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 06 Aug 2021 23:36:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libedit-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		sqlite-dev 	; 		export CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 06 Aug 2021 23:36:39 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Fri, 06 Aug 2021 23:36:47 GMT
RUN docker-php-ext-enable sodium
# Fri, 06 Aug 2021 23:36:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 06 Aug 2021 23:36:55 GMT
CMD ["php" "-a"]
# Tue, 24 Aug 2021 21:17:03 GMT
RUN set -eux;   apk upgrade --no-cache;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Tue, 24 Aug 2021 21:17:30 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/edf2c4d40de3b86cc1a6e1877eaede05be016389/install-php-extensions;   echo 2c3e48c01d5346be2c6cdd8d6f0a754f107d1119960b3f9d7cad0cae3ac663fb3646eab890310f89aeb3066460fee712034c0f5537608996f9a9f5f413992528 /usr/local/bin/install-php-extensions | sha512sum --strict --check;   chmod +x /usr/local/bin/install-php-extensions
# Tue, 24 Aug 2021 21:18:35 GMT
RUN set -eux;   install-php-extensions     bz2     zip
# Tue, 24 Aug 2021 21:18:44 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Tue, 24 Aug 2021 21:18:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 24 Aug 2021 21:18:53 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 24 Aug 2021 21:18:59 GMT
ENV COMPOSER_VERSION=2.1.6
# Tue, 24 Aug 2021 21:19:25 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   php -r "     \$signature = '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Tue, 24 Aug 2021 21:19:30 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Tue, 24 Aug 2021 21:19:41 GMT
WORKDIR /app
# Tue, 24 Aug 2021 21:19:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Aug 2021 21:19:54 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:0ff902055236f70c4694c806877243e1dd52c513825a2a3ecc7eba8f5202acc8`  
		Last Modified: Fri, 06 Aug 2021 18:29:33 GMT  
		Size: 2.8 MB (2811152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6ff25f38da82eae5b2405214e57c7c39a03ddb9e5eb9d04b31edf4dcc07669`  
		Last Modified: Sat, 07 Aug 2021 00:29:55 GMT  
		Size: 1.8 MB (1753673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af333e5ee6f8ffe8b982f0c46d826dbc17bbc35803e4c60443beea3af1ab1bc`  
		Last Modified: Sat, 07 Aug 2021 00:29:54 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c80d5e8e81136737bd0d714e4bbecc9480689bf7e1faf489f1ad332150d992`  
		Last Modified: Sat, 07 Aug 2021 00:29:54 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3881d096611c361e85cb37932cd5461bf9279391f0c70ee19fcd381ff21085e`  
		Last Modified: Sat, 07 Aug 2021 00:31:38 GMT  
		Size: 10.7 MB (10698207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e18e7693ac56c64a45d1f92442689618857bf7c14c191e66396672d9dfa21b`  
		Last Modified: Sat, 07 Aug 2021 00:31:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3d970e94ac55b458bd440157dd4ebeff987b330da614e503febc4bd8804775`  
		Last Modified: Sat, 07 Aug 2021 00:31:40 GMT  
		Size: 15.7 MB (15691529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa782a12845b2756bf1b9007a53bc921e39ff1b0ac1ffb35d5b919c3179a832`  
		Last Modified: Sat, 07 Aug 2021 00:31:36 GMT  
		Size: 2.3 KB (2265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7da2181c5829ba6c70625faed8cc46d740dbd874ad5ff767bcda1472cd96117`  
		Last Modified: Sat, 07 Aug 2021 00:31:36 GMT  
		Size: 17.8 KB (17789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac276ac2f4c0a0e73f0e42b9b5a0bd12def375f503eab6052cf273b3b833638`  
		Last Modified: Tue, 24 Aug 2021 21:21:57 GMT  
		Size: 35.3 MB (35291260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25dc797aed49df72b2b4541d50a84db213ca3c6413507b4ee2fe1aaf64f594d7`  
		Last Modified: Tue, 24 Aug 2021 21:21:49 GMT  
		Size: 19.3 KB (19337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c198f595078b7302fa896ff128d0142fb6988ff2c1f9bf88299a20a931bad67`  
		Last Modified: Tue, 24 Aug 2021 21:21:46 GMT  
		Size: 220.3 KB (220261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91916fb4190c07c62b255884c221d03896912255fe98a16b424225b8806c0d0`  
		Last Modified: Tue, 24 Aug 2021 21:21:45 GMT  
		Size: 261.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c4d72d716596010a50e5e8c552b84ca1a9fc6ed8142ea5270619d00cc7da74`  
		Last Modified: Tue, 24 Aug 2021 21:21:45 GMT  
		Size: 555.7 KB (555735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4488abafb8100aaa2fb9e88be3d3cb5e9fdeae6e00b2fbc58cd5a40e20fa20f9`  
		Last Modified: Tue, 24 Aug 2021 21:21:45 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d495b0afd069da8bae08e880354d822a682468073cad659e6df8261d1beb21ea`  
		Last Modified: Tue, 24 Aug 2021 21:21:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:28afd267e18cc330a1db102808513b906686da1bdefdc019ac90413112d865d4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.0 MB (66001538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9f1072ef0f1a7866ac737422fe88cd6838dfebfa66c0bacb67730b6fa7e2881`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 06 Aug 2021 17:41:30 GMT
ADD file:bdf19d63e9f8600d2fbe02435279b8df06fbcb5105e6b8eea778d8ef928e219a in / 
# Fri, 06 Aug 2021 17:41:31 GMT
CMD ["/bin/sh"]
# Fri, 06 Aug 2021 19:04:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Aug 2021 19:04:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 06 Aug 2021 19:04:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Aug 2021 19:04:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Aug 2021 19:04:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 06 Aug 2021 19:04:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 19:04:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Aug 2021 19:04:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Aug 2021 19:12:31 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 26 Aug 2021 20:41:34 GMT
ENV PHP_VERSION=8.0.10
# Thu, 26 Aug 2021 20:41:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.10.tar.xz.asc
# Thu, 26 Aug 2021 20:41:35 GMT
ENV PHP_SHA256=66dc4d1bc86d9c1bc255b51b79d337ed1a7a035cf71230daabbf9a4ca35795eb
# Thu, 26 Aug 2021 20:41:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Aug 2021 20:41:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Aug 2021 20:47:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Aug 2021 20:47:18 GMT
COPY multi:efd917b98407edb5d558edb0edbd8e63c9318f701892aaa449794d019a092f37 in /usr/local/bin/ 
# Thu, 26 Aug 2021 20:47:20 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Aug 2021 20:47:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Aug 2021 20:47:21 GMT
CMD ["php" "-a"]
# Fri, 27 Aug 2021 04:51:05 GMT
RUN set -eux;   apk upgrade --no-cache;   apk add --no-cache --virtual .composer-rundeps     p7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip
# Fri, 27 Aug 2021 04:51:11 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://raw.githubusercontent.com/mlocati/docker-php-extension-installer/edf2c4d40de3b86cc1a6e1877eaede05be016389/install-php-extensions;   echo 2c3e48c01d5346be2c6cdd8d6f0a754f107d1119960b3f9d7cad0cae3ac663fb3646eab890310f89aeb3066460fee712034c0f5537608996f9a9f5f413992528 /usr/local/bin/install-php-extensions | sha512sum --strict --check;   chmod +x /usr/local/bin/install-php-extensions
# Fri, 27 Aug 2021 04:51:43 GMT
RUN set -eux;   install-php-extensions     bz2     zip
# Fri, 27 Aug 2021 04:51:44 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini
# Fri, 27 Aug 2021 04:51:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 27 Aug 2021 04:51:44 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 27 Aug 2021 04:51:44 GMT
ENV COMPOSER_VERSION=2.1.6
# Fri, 27 Aug 2021 04:51:47 GMT
RUN set -eux;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   php -r "     \$signature = '4ac45767e5ec22652f0c1167cbbb8a2b0c708369153e328cad90147dafe50952';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.dev.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, dev public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   php -r "     \$signature = '57815ba27e54dc317ecc7cc5573090d087719ba68f3bb7234e5d42d084a14642';     \$hash = hash('sha256', preg_replace('{\s}', '', file_get_contents('/tmp/keys.tags.pub')));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, tags public key is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   php -r "     \$signature = '756890a4488ce9024fc62c56153228907f1545c228516cbf63f885e036d37e9a59d27d63f46af1d4d07ee0f76181c7d3';     \$hash = hash('sha384', file_get_contents('/tmp/installer.php'));     if (!hash_equals(\$signature, \$hash)) {       echo 'Integrity check failed, installer is either corrupt or worse.' . PHP_EOL;       exit(1);     }"   ;   php /tmp/installer.php --no-ansi --install-dir=/usr/bin --filename=composer --version=${COMPOSER_VERSION};   composer --ansi --version --no-interaction;   composer diagnose;   rm -f /tmp/installer.php;   find /tmp -type d -exec chmod -v 1777 {} +
# Fri, 27 Aug 2021 04:51:47 GMT
COPY file:fec7a37c0f859c3b5da390e40fa6f3ea8445ed26f54be61f4bce40efcaad57ee in /docker-entrypoint.sh 
# Fri, 27 Aug 2021 04:51:47 GMT
WORKDIR /app
# Fri, 27 Aug 2021 04:51:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 27 Aug 2021 04:51:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:625f57562315453466f73bc9d8c96e678f8d4ea436b462d06c60fb217c6b3d38`  
		Last Modified: Fri, 06 Aug 2021 17:42:42 GMT  
		Size: 2.6 MB (2602036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2568987867095245025c394f06456a47a6c8bdaa6c96639c49ddb43f6bff047`  
		Last Modified: Fri, 20 Aug 2021 19:50:42 GMT  
		Size: 1.8 MB (1768133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd26dcb760c8a12fd1e292df471c9fde4aba0c4c70b845397a1dfe2e434b942b`  
		Last Modified: Fri, 20 Aug 2021 19:50:41 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba8a5b372f3024025b5c742c3ac12e1b59f6c09600dbc45c2ce807f5dfa3935`  
		Last Modified: Fri, 20 Aug 2021 19:50:41 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0749afcf44dc17247d43d96f52a89d5ebe104445770d31172ddf35e5689eeece`  
		Last Modified: Fri, 27 Aug 2021 00:17:29 GMT  
		Size: 10.7 MB (10722817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110bc9fe7dd07ed22ec28d981fa1daac45bb8708ac0350b1e97767d8a76b9b55`  
		Last Modified: Fri, 27 Aug 2021 00:17:29 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ea7fe21de1566512cb468677d5e79f66854c07eeb445f343a87d3d74620ba5`  
		Last Modified: Fri, 27 Aug 2021 00:17:31 GMT  
		Size: 15.4 MB (15377250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc88633cb5d342f2bb9a20fc8504761d90b5e0b39bc9b5332e9a7e5b1d05ad3`  
		Last Modified: Fri, 27 Aug 2021 00:17:28 GMT  
		Size: 2.3 KB (2263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8034c94a4bd10617f4f80a94615d2ea2a1b7f1d63b682643f2b03f434bda4b3c`  
		Last Modified: Fri, 27 Aug 2021 00:17:28 GMT  
		Size: 17.9 KB (17861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb372ae86a351410c85550d653706f4af79c1417767f487db6151d9c1a2e19b4`  
		Last Modified: Fri, 27 Aug 2021 04:52:35 GMT  
		Size: 34.7 MB (34720900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461cf3140e551bbbbc5c671977c629716622286578e3be819e0eac831d42d199`  
		Last Modified: Fri, 27 Aug 2021 04:52:30 GMT  
		Size: 19.3 KB (19337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec81e501921ab74ba18a04553318a4dd61cda07d308d402b2cfd1e9722c6ab2`  
		Last Modified: Fri, 27 Aug 2021 04:52:29 GMT  
		Size: 212.4 KB (212400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54eb6dc50fe58758f155cb9687950be854b075b96207b70bcd03c4d1343c2e20`  
		Last Modified: Fri, 27 Aug 2021 04:52:28 GMT  
		Size: 257.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36eae416d62c86342507a4c1ad23e454649a549e448550e534203e4c2592f405`  
		Last Modified: Fri, 27 Aug 2021 04:52:29 GMT  
		Size: 555.7 KB (555726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983674988b1411bc600a8efcb846575bd5549637fc7e8dd72a05a4cce9a486ad`  
		Last Modified: Fri, 27 Aug 2021 04:52:29 GMT  
		Size: 408.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:575f2a53be3cce037f556f22e59cbaa34e89a5c9a0e9b97e09000c15201d9d39`  
		Last Modified: Fri, 27 Aug 2021 04:52:28 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
