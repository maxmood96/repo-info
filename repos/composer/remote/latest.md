## `composer:latest`

```console
$ docker pull composer@sha256:7087d97fc804abaa5292c2349bcf96f5055dc5527313e1d4b15bca4ada77f9bb
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
$ docker pull composer@sha256:572efdb615b8a744555bab9f1d0798cd1e01e874aea8f8fa99541f5015223921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69836865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bba1f537c99c7fd18bf199bf035d534be95ae8be923d8689a1928dd097de84`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:23:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 04:23:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 04:23:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 04:23:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 04:23:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 04:23:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:23:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:23:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 04:23:28 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 27 Jan 2024 04:23:28 GMT
ENV PHP_VERSION=8.3.2
# Sat, 27 Jan 2024 04:23:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 27 Jan 2024 04:23:28 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 27 Jan 2024 04:23:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 04:23:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:27:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 04:27:20 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:27:21 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 04:27:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 04:27:21 GMT
CMD ["php" "-a"]
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_VERSION=2.6.6
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
WORKDIR /app
# Mon, 11 Dec 2023 11:48:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 Dec 2023 11:48:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9ef19a461f9d419fc91c59399a9daa1f3302d30f099065a185a8bfeea3c9a8`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 2.8 MB (2761515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2fc49c6a93ebf520a5ecba9c061dbdd22083df74d0de9dcac9011f3f927d9f`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a4aa92ed6361a95da0e916e30e661754a1edf38c0b8b15bee6872d055e3603`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9cf6050c6fc86a1d59a8456d6bbc592142d2423bca682bfcc4f06515b62d39`  
		Last Modified: Sat, 27 Jan 2024 05:36:07 GMT  
		Size: 12.5 MB (12460883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ee940ccff4705d6ea3e013cbf4cc5f7442c7ed1fb0ef7e4affdcc2f4703274`  
		Last Modified: Sat, 27 Jan 2024 05:36:06 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a267137b654236587382697c275efab339bee32d96061f4b339516cedb61f0f`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 17.2 MB (17187605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bf9756a9a7d1026955a017a3b6ff814e6666b9ea3651b24a71b391884e5e82`  
		Last Modified: Sat, 27 Jan 2024 05:36:06 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfdc99627deb47cc30bb00f24a76026e86b22a29070a9536fb919b0f91159c0`  
		Last Modified: Sat, 27 Jan 2024 05:36:06 GMT  
		Size: 19.3 KB (19290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d66e15a4da2e923bedef73dc290f680203aa5c353347c36dd6e420c7015801`  
		Last Modified: Sat, 27 Jan 2024 11:03:50 GMT  
		Size: 32.7 MB (32682731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de472e3a316ccdb3c4f978a61ccc29cd60999c5463550aa9423efd2b48c49ab9`  
		Last Modified: Sat, 27 Jan 2024 11:03:45 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb2cd8ca4493045921a9f94fd4819c544f201c3be81e9df9eeda51dd739c7fa`  
		Last Modified: Sat, 27 Jan 2024 11:03:45 GMT  
		Size: 1.3 MB (1310836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434a139006467fa936940e1737068b498d37b318ed68c0929eeb28d06d669b01`  
		Last Modified: Sat, 27 Jan 2024 11:03:45 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d1d7cf6af85624f5918fb0c730ace0f2ec45b4d3099eae59b072521f977a73`  
		Last Modified: Sat, 27 Jan 2024 11:03:45 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:2dcb82b27bfcb7c1d28ed1de4cea54a677f8094968600a51f4537ad1e4cd602f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67024564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f165b0ed2fd384fff0028697738e2c5a1ee7e673e90b424359caee43ebd438d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:22:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 05:22:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 05:22:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 05:22:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 05:22:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 05:22:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:22:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:22:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 05:22:23 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 27 Jan 2024 05:22:23 GMT
ENV PHP_VERSION=8.3.2
# Sat, 27 Jan 2024 05:22:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 27 Jan 2024 05:22:23 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 27 Jan 2024 05:22:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 05:22:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:26:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 05:26:39 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:26:40 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 05:26:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 05:26:40 GMT
CMD ["php" "-a"]
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_VERSION=2.6.6
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
WORKDIR /app
# Mon, 11 Dec 2023 11:48:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 Dec 2023 11:48:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6147d01edb253ab7eff347bb08482a430759361f869152a4c0a0ecdd946e0d17`  
		Last Modified: Sat, 27 Jan 2024 06:44:23 GMT  
		Size: 2.8 MB (2764487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b42f6e9b3a3a721beed37ea494f71a49e981f945e849780a3cc6a57bf1c0ed9`  
		Last Modified: Sat, 27 Jan 2024 06:44:22 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7136267c1932cb42af7ae697ecc07c459f4c5a75f3adf037cdfff9774f183ff3`  
		Last Modified: Sat, 27 Jan 2024 06:44:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea6b899bbae9bb1c725f38ac1380917779c1853cc90f826d0ab55ddae5aa08a`  
		Last Modified: Sat, 27 Jan 2024 06:44:21 GMT  
		Size: 12.5 MB (12460908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd20b45739fb4f1f0bf78a78912a555f4c350d34553395c43646ac6938d9e16`  
		Last Modified: Sat, 27 Jan 2024 06:44:20 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a912ca9164f2427b5ee76a5422c436a01ba89fabd2441fb12f3b495884e4fc04`  
		Last Modified: Sat, 27 Jan 2024 06:44:23 GMT  
		Size: 15.7 MB (15696949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d30945795e7ab62b6147225c114c114729b4d023067f670c4b8aea0d443be6`  
		Last Modified: Sat, 27 Jan 2024 06:44:20 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe0fa55607613cc91bd0a2bad8bc9a8f8a8e7ae1ed863faeb5b440fb61bc17a`  
		Last Modified: Sat, 27 Jan 2024 06:44:20 GMT  
		Size: 19.1 KB (19133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18391edc391e05609b76ef4df5a7e74b03860ea57560f10eaef284318bf186e4`  
		Last Modified: Sat, 27 Jan 2024 09:37:42 GMT  
		Size: 31.6 MB (31627804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab91b70f4a58ff6a36b21778226d755a0983116b4f9c43368bda32857a6efba6`  
		Last Modified: Sat, 27 Jan 2024 09:37:37 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcd4161d08e2a647464469b988ed67d3f33863b5cb71ec853b4b5383725aff0`  
		Last Modified: Sat, 27 Jan 2024 09:37:37 GMT  
		Size: 1.3 MB (1284611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7504e1c8a4efb9b0117473de6a230752adfa6b41c1b5ed898ca45cf17ad5f9ba`  
		Last Modified: Sat, 27 Jan 2024 09:37:37 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6322470e1f9bd3834777ad89a97a7805fa8ee18bdc5420990229b39e4eee39`  
		Last Modified: Sat, 27 Jan 2024 09:37:37 GMT  
		Size: 125.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:a6af81f2253990f2e7b9c6d9be39714668385cda2c28db3d856182df82c4f54d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65090471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a078239d45dd2f7968c3f8eb3d8c1b963e7aa60649e4b8ce4b1dccb8ddb350`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:34:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 06:34:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 06:34:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 06:34:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 06:34:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 06:34:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 06:34:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 06:34:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 06:34:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 27 Jan 2024 06:34:56 GMT
ENV PHP_VERSION=8.3.2
# Sat, 27 Jan 2024 06:34:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 27 Jan 2024 06:34:56 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 27 Jan 2024 06:35:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 06:35:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:38:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 06:38:30 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:38:32 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 06:38:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 06:38:32 GMT
CMD ["php" "-a"]
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_VERSION=2.6.6
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
WORKDIR /app
# Mon, 11 Dec 2023 11:48:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 Dec 2023 11:48:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fad4c06f9510d8c219b7fe261aa66aed178abd7a1c84deb7c27194f902386d7`  
		Last Modified: Sat, 27 Jan 2024 07:33:08 GMT  
		Size: 2.6 MB (2612619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b84d0418e4ec14c0677d1849ef32a6fc29b8ff5271474a5fc99e97086db728`  
		Last Modified: Sat, 27 Jan 2024 07:33:07 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae368cea0e62724a4b01ec73e9ff3a02291ca0fd945c2ae68057812a20aaa69`  
		Last Modified: Sat, 27 Jan 2024 07:33:07 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6216ddf2898e9abdbf1c04d72c832c83f4ef2b3bd2c1e3d5550910e59d04616c`  
		Last Modified: Sat, 27 Jan 2024 07:33:07 GMT  
		Size: 12.5 MB (12460905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39c5c0335631b22c4e31c9d23fa41b288a90802c57ffacbc459ba52a3e55d16`  
		Last Modified: Sat, 27 Jan 2024 07:33:05 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597dcfc055d050018eecb2dee9a81021a1dc19f0ba009ec0bf4945f8e3040696`  
		Last Modified: Sat, 27 Jan 2024 07:33:08 GMT  
		Size: 14.7 MB (14692578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97549bfd8d8b98e8a2271a8a8e3b0ccf287b960020815230c9e3b83c83c684c0`  
		Last Modified: Sat, 27 Jan 2024 07:33:05 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde6f26f53a052833b6fd18d71febf835f44a0fca3085ba3957f4c29fc2dde43`  
		Last Modified: Sat, 27 Jan 2024 07:33:05 GMT  
		Size: 19.1 KB (19107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6008ec0182396b2409524a7daca7112bbf3dc17599c08c5663d3623522d2a7a6`  
		Last Modified: Sat, 27 Jan 2024 10:54:15 GMT  
		Size: 31.1 MB (31134694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82603e10e8fde19ca02cda4f42ca5fe9f664b1c73feffe2cf5c656e7ef78f69`  
		Last Modified: Sat, 27 Jan 2024 10:54:09 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd61f673f76028c49c4b8e639ef9bf381f8fdcb69f775ab4b87c85016ac2d33c`  
		Last Modified: Sat, 27 Jan 2024 10:54:09 GMT  
		Size: 1.2 MB (1246395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a9e1308e0e6d80fdcbf5108e427b12d7a9c9295c7c6551950c772eb1ca32788`  
		Last Modified: Sat, 27 Jan 2024 10:54:09 GMT  
		Size: 417.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389572991e93299bd2afaf0f586ccbede3907a10c4bc889d609db8626140645a`  
		Last Modified: Sat, 27 Jan 2024 10:54:12 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:8283185a720537b7b2f503d081cb987ef8e460de461cae8de5b53dcb43549192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70309374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6ecbdd386a4cbfe5a7dd4f13e409a0b15cc516a22076b325dc8f246753d8fdd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:28:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 07:28:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 07:28:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 07:28:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 07:28:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 07:28:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 07:28:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 07:28:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 07:28:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 27 Jan 2024 07:28:56 GMT
ENV PHP_VERSION=8.3.2
# Sat, 27 Jan 2024 07:28:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 27 Jan 2024 07:28:57 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 27 Jan 2024 07:29:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 07:29:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:33:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 07:33:05 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:33:06 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 07:33:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 07:33:07 GMT
CMD ["php" "-a"]
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_VERSION=2.6.6
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
WORKDIR /app
# Mon, 11 Dec 2023 11:48:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 Dec 2023 11:48:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f072bab4d3b766550992c322a39fcd900b329ffbe17cdcb1a7d74010688b23ec`  
		Last Modified: Sat, 27 Jan 2024 08:40:23 GMT  
		Size: 2.8 MB (2815760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537d23c253bc777c8630b1470aee1d7857122cbdf09144b5cb061bde634e0fbd`  
		Last Modified: Sat, 27 Jan 2024 08:40:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c65cde09541f81b6406c9aa0f33cd98ae9716bc8c625290248755e374475bda3`  
		Last Modified: Sat, 27 Jan 2024 08:40:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84822948d41e3b301325fe741efc11ac7ace3a6b598d24aa111e89de71deee9d`  
		Last Modified: Sat, 27 Jan 2024 08:40:21 GMT  
		Size: 12.5 MB (12460901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a0b1452faef5fc1d3cb18f75f8ca465d7d2b15daee0e6ce51437452e62881e`  
		Last Modified: Sat, 27 Jan 2024 08:40:20 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292dd4ac776ff20c740d95d1c0c9162f522b24f3194d314cbb261a028f37c794`  
		Last Modified: Sat, 27 Jan 2024 08:40:22 GMT  
		Size: 17.2 MB (17158390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6688d2bd30879bedc9d2f5c919eacfffa74f90befe0b34bb2e028cab8e52e71`  
		Last Modified: Sat, 27 Jan 2024 08:40:20 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1db26f84cd8593debc9c87e062c4b3568069da5375d7a1161058f1bf0a150f0`  
		Last Modified: Sat, 27 Jan 2024 08:40:20 GMT  
		Size: 19.1 KB (19082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203bb7d23b09aceb94f28ec883d21b26670fc55ca01854862018c96e024aa031`  
		Last Modified: Sat, 27 Jan 2024 10:53:40 GMT  
		Size: 33.2 MB (33191363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94458096517d237b10627cebd0ede1d7a7b0a53dd7ea8748ea0d692001293372`  
		Last Modified: Sat, 27 Jan 2024 10:53:36 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f511a47f92dbaa396097ec7e8a5602fac99a4f22b70671333659a606e34ef006`  
		Last Modified: Sat, 27 Jan 2024 10:53:36 GMT  
		Size: 1.3 MB (1310888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0a22028373b2d635e5a6a3d5fcdaa61afd528c7f6e94ea8b0829d3fea5a67c`  
		Last Modified: Sat, 27 Jan 2024 10:53:36 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1c867692a6bb7ac4dd6ae6d50bcaccdb173860240de66950070f94f506358e`  
		Last Modified: Sat, 27 Jan 2024 10:53:36 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:61cff45ee97b3d1ab935b99b157c24690954d9536d5963cc984b2b964208d196
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48426951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5aeddb86924b4550fd8fde892a6e1d4b7e1597a19ab3e27f28cd10f7ee58b9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:42:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 04:42:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 04:42:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 04:42:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 04:42:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 04:42:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:42:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:42:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 04:42:13 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 27 Jan 2024 04:42:13 GMT
ENV PHP_VERSION=8.3.2
# Sat, 27 Jan 2024 04:42:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 27 Jan 2024 04:42:14 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 27 Jan 2024 04:42:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 04:42:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:49:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 04:49:06 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:49:08 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 04:49:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 04:49:08 GMT
CMD ["php" "-a"]
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_VERSION=2.6.6
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
WORKDIR /app
# Mon, 11 Dec 2023 11:48:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 Dec 2023 11:48:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf91a7316d2e2098b1a91882947964b19bab201421576e249c440063e956bcab`  
		Last Modified: Sat, 27 Jan 2024 06:46:12 GMT  
		Size: 2.8 MB (2825332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a5caaf92a60154c94967702a2fdee5954dec8352f776f8abc87659c4de67f6`  
		Last Modified: Sat, 27 Jan 2024 06:46:11 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d170158e1d1cffac62a145eb90dbbfd417840d1e2a9a4ae707cafa0bcc2781`  
		Last Modified: Sat, 27 Jan 2024 06:46:11 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f764086f31884d7b0f1d7eb0ba50a7b60b54ba024be9203e346e7c20e21bf91`  
		Last Modified: Sat, 27 Jan 2024 06:46:11 GMT  
		Size: 12.5 MB (12460896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:227533438eebd55051b7f7a308b969d3a741e478d18e7b99124830dbf77fa548`  
		Last Modified: Sat, 27 Jan 2024 06:46:09 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04013657a86362c807cc94e24f0f17c14f904fd2d702a5a6f394c27280c4c30`  
		Last Modified: Sat, 27 Jan 2024 06:46:14 GMT  
		Size: 17.6 MB (17619941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e69c1134ef674dbf87f6e944b2fa40cd619587dc30eee552f4e6fd032c36ef`  
		Last Modified: Sat, 27 Jan 2024 06:46:09 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb0b2889b5559b0afca36633c2736ccad53063a71a8667aa8066846b1ea5fcd`  
		Last Modified: Sat, 27 Jan 2024 06:46:09 GMT  
		Size: 19.3 KB (19293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c48cd36a22b54ecbae34842d0c60ce9ff0603d8940bf0fb9c382e8b7f8f8c5d`  
		Last Modified: Sat, 27 Jan 2024 08:35:02 GMT  
		Size: 11.0 MB (10992151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868a9cd94a94806f0e49b251a9ea4091419b2013a448786669b12d9f867440f2`  
		Last Modified: Sat, 27 Jan 2024 08:35:00 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0a6dcf7732a176d3bb82b730a8739e39249ebac7579d776748c593e1afb987`  
		Last Modified: Sat, 27 Jan 2024 08:35:00 GMT  
		Size: 1.3 MB (1259975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:526a31ae89bcbd1e08e3d852912aa46e19b825a4fe87f658452babfcc2f29ec8`  
		Last Modified: Sat, 27 Jan 2024 08:35:00 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9795797999b8a7857e57ce06e338aaadeb4f8e68393855b38a85e3964a91a4`  
		Last Modified: Sat, 27 Jan 2024 08:35:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:57870772d0b4d4adcf0894aae90b25807009343340fe4cf23022d4982981e38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71880020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ccd211edf5f16b66627398e96c8da923db2cce3eb5b9552eee442d079cdb781`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:26:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 03:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 03:26:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 03:26:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 03:26:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 03:26:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 03:26:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 03:26:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 03:26:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 27 Jan 2024 03:26:20 GMT
ENV PHP_VERSION=8.3.2
# Sat, 27 Jan 2024 03:26:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 27 Jan 2024 03:26:21 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 27 Jan 2024 03:26:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 03:26:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:29:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 03:29:08 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:29:10 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 03:29:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 03:29:11 GMT
CMD ["php" "-a"]
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_VERSION=2.6.6
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
WORKDIR /app
# Mon, 11 Dec 2023 11:48:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 Dec 2023 11:48:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8953adc2ed89719cf332d6841a33f5396f09790ebe287db3934fd2327d14b7`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 2.8 MB (2842838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a412c6f832e805dac7f8f5eb85b03e9340bde010929c469a7aa203611edf867d`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ad5c29bf6c410c283dc6e7c4619fb7570382a7860ef5d8b6a00e3228ea8a03`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e402736c65d3021e174eb60d2119ca14cb71d8cc898dc4787e32373e3a93d38`  
		Last Modified: Sat, 27 Jan 2024 04:21:20 GMT  
		Size: 12.5 MB (12460901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc05ac212c82d7ae00e8fd659bf8741a99dc3f78dc994b3479d4b534bab8fffe`  
		Last Modified: Sat, 27 Jan 2024 04:21:18 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388d426f5ed84edb688688d18bb3a69f5d74006eb2465eac42ea962726d4c375`  
		Last Modified: Sat, 27 Jan 2024 04:21:22 GMT  
		Size: 18.1 MB (18053481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3bc359fcdd4fe6139fa6ebcfb2d83bff37f0be9b9ffadb4c175793bf03cd64`  
		Last Modified: Sat, 27 Jan 2024 04:21:19 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371bc4cf722169c2e8dd4965433cab25c0fbc3cd952ece441f4a7ae237bbd960`  
		Last Modified: Sat, 27 Jan 2024 04:21:18 GMT  
		Size: 19.1 KB (19104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ce147398d8d566711bf99e7ce612dbeee06d13aed143b8372f3785bf511c59`  
		Last Modified: Sat, 27 Jan 2024 07:51:30 GMT  
		Size: 33.8 MB (33779806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2112075f8f8609763e62679bb00ab061e106aab49062152d4a5a59d323a6ef8c`  
		Last Modified: Sat, 27 Jan 2024 07:51:24 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151ba5a202a1870ac7254b565837d59dfce8205eb11e746e52fd07ad3866ed36`  
		Last Modified: Sat, 27 Jan 2024 07:51:25 GMT  
		Size: 1.4 MB (1360257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c91a0924533127793e1ffb235381444f69f6b6f1c7ea29c5fa56fa4b0717199`  
		Last Modified: Sat, 27 Jan 2024 07:51:24 GMT  
		Size: 418.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d36dccd93e4c54eb431fa255e34d576eb87caaed46a14e3c9ed8155c43c4d2d`  
		Last Modified: Sat, 27 Jan 2024 07:51:24 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:b82f65fa1482aa347e926f9f924e5e4981e3f2379cddd289ee3240759d408da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72167301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8f8c0e2bdfb214f4e11c1b06cd7505e9dcd8874a298e2cd3a906b38c96b4b8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Tue, 12 Dec 2023 19:58:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Dec 2023 19:58:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Dec 2023 19:58:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Dec 2023 19:58:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Dec 2023 19:58:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Dec 2023 19:58:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 19:58:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Dec 2023 19:58:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Dec 2023 19:58:26 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Sat, 20 Jan 2024 00:08:39 GMT
ENV PHP_VERSION=8.3.2
# Sat, 20 Jan 2024 00:08:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.2.tar.xz.asc
# Sat, 20 Jan 2024 00:08:39 GMT
ENV PHP_SHA256=4ffa3e44afc9c590e28dc0d2d31fc61f0139f8b335f11880a121b9f9b9f0634e
# Sat, 20 Jan 2024 00:08:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 20 Jan 2024 00:08:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 20 Jan 2024 00:11:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 20 Jan 2024 00:11:49 GMT
COPY multi:6edd033b037aa2d7697fc3b9f82c2f162146c1920a0c6d25a165dc56783204db in /usr/local/bin/ 
# Sat, 20 Jan 2024 00:11:50 GMT
RUN docker-php-ext-enable sodium
# Sat, 20 Jan 2024 00:11:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 20 Jan 2024 00:11:50 GMT
CMD ["php" "-a"]
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 11 Dec 2023 11:48:14 GMT
ENV COMPOSER_VERSION=2.6.6
# Mon, 11 Dec 2023 11:48:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   composer diagnose ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:48:14 GMT
WORKDIR /app
# Mon, 11 Dec 2023 11:48:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 11 Dec 2023 11:48:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0180a7268e169fa6dd82fc04f9270dbd4fe716cf09b03fc82f84618025bad4`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 2.9 MB (2937974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecaefbf268f4b1e4d9f16c5d67523f3b76e72db0c3fc7a2f3fb6fd7fbdec547`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f0d18e8f1067fcb105dea2ad180f140d138c6d99310025696d1aaa322017db`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a78f4a5e1412d833b4f2288a3f0cb1009a0200b4933bde41eeda4189af7d93`  
		Last Modified: Sat, 20 Jan 2024 01:58:09 GMT  
		Size: 12.5 MB (12460908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a89c1504cf5d7d7eea82d5d30ab5b8b9af1df13ce2d302839814fe0f08627f`  
		Last Modified: Sat, 20 Jan 2024 01:58:08 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f3939cacd6242eece0d6bdf0da655b533a91bf5cab2413d4974d8ffbd4b1c5`  
		Last Modified: Sat, 20 Jan 2024 01:58:11 GMT  
		Size: 19.3 MB (19313006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6239cd07acc68c451064e6194002552ff4749a0e7bcec572e7c4b9ea7253960`  
		Last Modified: Sat, 20 Jan 2024 01:58:08 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c3dfb785f3206890bb1e5402941734ece304d9d214faf06bc2216215a880d0`  
		Last Modified: Sat, 20 Jan 2024 01:58:08 GMT  
		Size: 19.1 KB (19088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbd146a7dc03d56db4658712ae24a5f6eaedb8f869d6484f429ed9e2f987aa9`  
		Last Modified: Sat, 20 Jan 2024 03:16:04 GMT  
		Size: 32.9 MB (32856477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fcc29a6ba4958a08e8864a7b4a0dd1f1ddf54c8f4807122c4fd4eaf24a6006`  
		Last Modified: Sat, 20 Jan 2024 03:16:00 GMT  
		Size: 265.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9555a38d8050b53960a0115f432aa1e335ba88fbd8b7c3c13f1b37115ab196c5`  
		Last Modified: Sat, 20 Jan 2024 03:16:00 GMT  
		Size: 1.3 MB (1332233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a1b3a5e43cd0c0c35cc98182fbdcbdadfaac690472abbb729242943ec74d21`  
		Last Modified: Sat, 20 Jan 2024 03:16:00 GMT  
		Size: 419.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a120399d4e90777c872064e75c5fdd0f013979ba4447fa72fa22ca1f0070222b`  
		Last Modified: Sat, 20 Jan 2024 03:16:00 GMT  
		Size: 126.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
