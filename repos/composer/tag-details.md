<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.25`](#composer2225)
-	[`composer:2.8`](#composer28)
-	[`composer:2.8.10`](#composer2810)
-	[`composer:latest`](#composerlatest)

## `composer:1`

```console
$ docker pull composer@sha256:6d71e5693b24a8d1d0a6cc0e791d24b9fe8ac5c93dc2a36d04f583e5617af9f7
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

### `composer:1` - linux; amd64

```console
$ docker pull composer@sha256:c54003d5eb87c26e5e700769788155cecfaab4e67ba443e58c7b2f073754f556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76594613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0021dafdd4fa74a0706df28a233d5e4fdf23abadba410ae4b883f06db3396a7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b8c404eae668716a1e38e4cfbfa17a24db95c67ac43f1c7fc370b54d3ca087`  
		Last Modified: Mon, 04 Aug 2025 20:49:49 GMT  
		Size: 3.5 MB (3460957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d882c5edba216e9f63d26119702e252a7f88372fa0af1077c58c6f937c29f`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769d794d159afc0f29bb41cae73fa8177791b4078920913550d6035fce888bf2`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3cf3bc6932e6344a1c898a1bdf35235fe0327d7cac86e56f4b07b23b9e9847`  
		Last Modified: Mon, 04 Aug 2025 20:49:51 GMT  
		Size: 13.7 MB (13653337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7066989316ffccd2c577fe6ce99e5bd4047a2f447f99f832d66a2f1cf334e8`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2176a4cebfd98252931aee5773d33b5a3a42d7e11f90f52e09364ad1fa8fd18`  
		Last Modified: Mon, 04 Aug 2025 20:49:52 GMT  
		Size: 21.0 MB (20975718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43e4b7ed65e42eff594acdcad113649b65b82ee4f86ccddb9c65ef1633a2fd7`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d54c809af2e0932d4bc53c9c0fa80cc499fba826b868e3ddc446d3361cb44`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 20.0 KB (19952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2151aa88e776b0b7a7bf7705e4dc7d63b02f2b67ebb32a829a34e18f38c3b1fc`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fe67c28dd380fb9d034436907eba4e9f531e36e618b2250b5db3b7fa8d56cc`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 33.9 MB (33924822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a594a597b20e45f01dbdf35451ac3ea882cf160ff9488af8ef8bf2c9b612b282`  
		Last Modified: Mon, 04 Aug 2025 21:00:13 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d4116fdf820847be31bf0c21a6ef192760c95f72efd1774d228ec7efda633e`  
		Last Modified: Mon, 04 Aug 2025 21:00:13 GMT  
		Size: 735.3 KB (735336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0ed3e474d106de7e08acf6903e1d56e71c8d3a2e0dfb2f6d391a808818381f`  
		Last Modified: Mon, 04 Aug 2025 21:00:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b494f816a6650c915cb5c09c07e675189183a0ca691444f56e3f783b181fe34`  
		Last Modified: Mon, 04 Aug 2025 21:00:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:d1cdcf6c237ba6bdbf471646f24ccbdd2c04030d93f81bd636f88b69d0fa6c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757b09cc5443d2eaf2ea50ba1791348225112fa92ea402f0317cea4bbc4256c6`

```dockerfile
```

-	Layers:
	-	`sha256:9635d825247c25d5bc3361de19612e13680753e9c261c425e43ae0ce4f47fba1`  
		Last Modified: Mon, 04 Aug 2025 22:13:26 GMT  
		Size: 2.2 MB (2169304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcbcd115f72960e4fbd5904250297d12ea1631fda234d7ae3926e6bfba3a356`  
		Last Modified: Mon, 04 Aug 2025 22:13:27 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:30cb45241a9563758dd42abce1bd8ae746fd2546165867530debbf399be23590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74239445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94678d3bf400f557c789f8c1ab4eff13d5813f550f849e54cff0dd524a2e4a0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7494cac4578077d244b00bcd8c4b9cc24cbac12fe484fc52bdb253b7be68d33`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 13.7 MB (13653331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb9d8c4b4750c9afc1de1182d3a39f160769ecb594f5119173d9999fdc1b99`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08da3ca3515f68d5f047717865555b86a20702e1abbb868f91b827eac6e5ebf`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 19.1 MB (19094736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174f8de30188274046eddf1fa9fea9d286fe5b22b08972783323bdc3074e69f9`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890cfd4e2ff1fb6e00ae91a595e532b992ff926f2b1aabb5d5cf4550fc056385`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ba3c18d23646492096ded6ff9adf0df6739c2b4139249d0ae790e82cfb69ae`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab618c8fb396a56d07a5986ec1e2c89587a34750ca91962eb0f8fc69192e86`  
		Last Modified: Mon, 04 Aug 2025 23:52:25 GMT  
		Size: 33.8 MB (33788254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610e01a216465a5a644cfe45ea36450b82393adf820afdeb633ed5876549f9e`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfead96b44b3a2abd1e425fc66f5b4016407daba06dbf7d84204e63ee4ca58b`  
		Last Modified: Mon, 04 Aug 2025 23:53:43 GMT  
		Size: 735.9 KB (735893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f7554a791b8f2097cc9477df1c2a7c4a6df66aeb67a04c3f75e59c1bef76e`  
		Last Modified: Mon, 04 Aug 2025 23:53:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbce85d740fbdb7943bdcd6bef72b8813437a32e1db5a5f25dda0af500063b3`  
		Last Modified: Mon, 04 Aug 2025 23:53:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:5d84303d37b9a44cb875c4a80e280bce213658cfd509a6a29efc975bbc1dc312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93074c139d91d719893295fda37e7db80bdf72b6f5870c3b07285013a6d28d5`

```dockerfile
```

-	Layers:
	-	`sha256:4a1088f36f1313ba6c6fed92467d5d7f309818cb0462ddace41bee2c6e264a59`  
		Last Modified: Tue, 05 Aug 2025 01:13:26 GMT  
		Size: 31.2 KB (31235 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:8a115a37e2e8ca57fe408432f1d77a86dd192b6b77be3ad90cbbebf0e7af1f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71023258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebade064c227a2113cd033a890101531d3249e99b0425e6d2ed3b4470bf86187`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca2e4db931023b2bd56443c80dbf78e53bf1efb748d1e76bf1242168c76cca6`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 13.7 MB (13653322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77469fa7f1256b86a0f5f641b66b80360641be9666ae4294dc5d6be17b7a5d8`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054413e584c9543fe5cdb41980742080a4ae1f7cae6744e77e0218deb7dac34d`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 18.1 MB (18070661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72860d23def789d218635f72e9644f4a04f18a8fa12c536da7af1ffa8743fa3c`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e66e44f6101fa11b28b93eec29aae52f52e35e47962ce16a425ce2822f9f64`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97417a1c0369df9443f468952dc56830ae71371b90f313f4b54c1c3b3f96390`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e233c39dcbf452f1d1e155cfa780907783f14f748767e9311ea6d9865ebc0896`  
		Last Modified: Tue, 05 Aug 2025 02:53:45 GMT  
		Size: 32.1 MB (32068670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45df4acb4b1365a6f7848309ec8384dbef2fded39db7a60a972ed210bacfc2e6`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86df24d504fe85588365a5efd26ce73e03cfbd5084f8bc0cb9e2ec28c7d0e4`  
		Last Modified: Tue, 05 Aug 2025 02:55:21 GMT  
		Size: 726.4 KB (726371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b6ae98d157dd0e1d270649bb4183f040212698e8243da6acacbbe301d6cf33`  
		Last Modified: Tue, 05 Aug 2025 02:55:20 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637a1452ff587f1379e6679c83777e31051f802906b1301a3383e1277053ff20`  
		Last Modified: Tue, 05 Aug 2025 02:55:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:571067be6f007ee91eda644494bbe3086b2746eef580c318e2d99618112be04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067ec23ec78ca2afeb6971e7bc895834f5a68ea3bffdfd1379e63cc53615a08f`

```dockerfile
```

-	Layers:
	-	`sha256:e626cd36a9aaf1b1f231d11893604b0ae06ea9d948a6eb8fd5ada05236989161`  
		Last Modified: Tue, 05 Aug 2025 04:13:30 GMT  
		Size: 2.2 MB (2169620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b7af08b3953fbc0df5df5dbb1593412aa0715fc84babdd30bee01fb818e80d2`  
		Last Modified: Tue, 05 Aug 2025 04:13:30 GMT  
		Size: 31.4 KB (31450 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:3dcc77730658e5a92ec3e049c891e2d3783ba147259296143b85c630ed65ffaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76541931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ccf6b49e1878bae8ff00cd7aa12b0c7f0b5361224812caf066e84b536a7fb8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb504dccc917de6b6b8bbc11ff4b9599d71f3ad971f142f67cc631aea843760`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 3.5 MB (3454743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7532649a0813cdb3165d225287dc7cbef8b4e47991127457849e1947e5549636`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253b9848099c2406835511872822d9dab1ea36834b393e1588c17a784e3bcb1`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973767f0cf0415e63013511841e37ace48afe3d8bbfaafa677dc100c89eb06ec`  
		Last Modified: Tue, 05 Aug 2025 01:42:19 GMT  
		Size: 13.7 MB (13653329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f37d53d2ef75f6d7f5ad4ee6e5eb97589d9dcf67380e28c57d85687f0a1c5c`  
		Last Modified: Tue, 05 Aug 2025 01:42:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3bef5a3676aa8a22d37f4aaaf0f903109f38d4050ea5bbf416baa0f2fdd4e9`  
		Last Modified: Tue, 05 Aug 2025 01:42:20 GMT  
		Size: 20.5 MB (20525567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfec7e98ad7662f3c4c51de1bf161799051d12f213dfd998753921e6a8cbe6d`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa68af9933e1df5a29b63199d57877c41b14c9f12615222a4ae65df1d2b9df`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 19.8 KB (19756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6fec7f9b2035416690d429232af55e7cafdbc99a57c3e473d5b44c4dc43fba`  
		Last Modified: Tue, 05 Aug 2025 01:42:18 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbf0d70d9d667639b695d04960c9fdafdd0aa711ae79b558e2e0959bf5b52f2`  
		Last Modified: Tue, 05 Aug 2025 08:15:54 GMT  
		Size: 34.0 MB (33997952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e41cdc44d3ea60f653b652041902b0f7ce6913b4b4f696e18302e88e07fae1`  
		Last Modified: Tue, 05 Aug 2025 08:15:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09193a92ada83add730d8c0f4282ff6fdc2dc83b456645eb75701f29b92b4d50`  
		Last Modified: Tue, 05 Aug 2025 08:16:45 GMT  
		Size: 735.2 KB (735231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b68cce5f680c42cc5c7d4c751b7f8cf49d2f10bb6e9f1ae0ccc0982642fce47`  
		Last Modified: Tue, 05 Aug 2025 08:16:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305dbefa45742158bf3b592156deda533fc2ed9ae46cea054eab407cc1d37c4b`  
		Last Modified: Tue, 05 Aug 2025 08:16:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:20de4cc4768d0249be875aa4f624b7e51840f3de0348d705ae34408151ef91ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa82a5145e89e22dd1a0107ef892fecfc2e4c94b680bad5594de70bd4d9947e`

```dockerfile
```

-	Layers:
	-	`sha256:e44fad7f5553d4b722182cae416f79ae69d64b1a6257dc1c350f7cd574460fb1`  
		Last Modified: Tue, 05 Aug 2025 10:13:28 GMT  
		Size: 2.2 MB (2169444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5e94a56e2cfd87963c7e9166e5328569b057565f5607c1eb904b044d76e72a`  
		Last Modified: Tue, 05 Aug 2025 10:13:28 GMT  
		Size: 31.5 KB (31478 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:048e4459850cef7ba685421c79ca2501e6dbec1b1f80e2eb9002a10bd76c8242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77518575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d692e30b246a086ca03ab968812cdb2ba47ae767b94913c33c0926b21af2a3a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe8439d75dd031f7f3a6908ae96e53d52128e10c30e23a158b9b8345d576f43`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 3.5 MB (3516254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dedafe9669d1a09c51f168c3d4db6477986ec7b7f4bb274347c5befbf1ab6e1`  
		Last Modified: Mon, 04 Aug 2025 20:50:20 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a8b0cb75e0335ca0c6f5b93ad9737facd671ebe28fba3a32ced09f40d7920b`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b409694fac1f06392e029aa1cce26b25863976e502862723282bece6849fd`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 13.7 MB (13653332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7d6aac432e4a310a74c720b92ddf62f125372b97cf40257ee5385d2159c3be`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abcffe2eb78cea70305ac08e1e90d0ac3e5de7b2671042ae50d8f9dcc2a38df`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 21.5 MB (21505197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4278be9860874f02951ab37abd3b1f199cca3b88299e7b54e4aec44ae9b6c97a`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dfdfedf576c6450fc46466c1f8e3b5b4d8c16aac720b69705113e7b87b3567`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482cd711b6eff6cb6033c515ddc86de794a4ca97eba0a2ff1d2555201ea9187a`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db77b3cf9bfb59dd8cfa41ebffd8d52c201213af184651cb7c46eaffff8c2b97`  
		Last Modified: Mon, 04 Aug 2025 20:58:58 GMT  
		Size: 34.4 MB (34436928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8b6fbed48ae536a36948de7cea211f922b9583682afc0fe4bd94de212fd941`  
		Last Modified: Mon, 04 Aug 2025 20:58:56 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a570db9332eaf689c5bae8c9c3b94bc52d346e385e0f424d60c3a035a73c4f`  
		Last Modified: Mon, 04 Aug 2025 20:58:57 GMT  
		Size: 747.1 KB (747144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ea502e4516812c2831d64f18305a246ba03b6f559b4e9c4571652026e63420`  
		Last Modified: Mon, 04 Aug 2025 20:58:56 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0427f58d49e65068523a6162f6534beded17307cefa29c6c57436ed6a6d25c73`  
		Last Modified: Mon, 04 Aug 2025 20:58:56 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:b1eead030887161ff7006e10184a47ed0bb9bd2181995a08fb76f461b0b22657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f936b82e26a46992a4e41a5dc59853c9f7e7376a7457f4972c1298deeb4ca4d6`

```dockerfile
```

-	Layers:
	-	`sha256:0e665dbd6988ff5a2cc8505b8eb13720ead82e3aea86d933fc0a8964ea613bfb`  
		Last Modified: Mon, 04 Aug 2025 22:13:40 GMT  
		Size: 2.2 MB (2169092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd259450a5705e7ddd47bf34b3bdf666ee12161d5eda15d366fe2b7c5d82583`  
		Last Modified: Mon, 04 Aug 2025 22:13:41 GMT  
		Size: 31.3 KB (31323 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:562aa20440afb6e249f2db8c4f65c1bea49ec0f7c4ac85c02170c9ae9681e7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78893164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fb79b009bdbff99bee3ac535310002302e60c626bbdfc173445cf99e549dea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2149fd89f974e7ea3dea06f37d735922f1379a8f6a3848f9f27b655a231533a`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 13.7 MB (13653344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7733690cb25c9174f17fcd594fb9aa92de487681f9a30a88d38ce0fb49dfc9b7`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56aa0ea4063f0f606994769dabd9afcf81090a22a66567e6f1bbad01c84cef`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 21.9 MB (21877960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555ac5f064703fcb811adc2fc69166c7117941c125b03426671e1d4f55cc4f67`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa79fbfe4077bdecbc88d7a5d32f94313e38f9fcff1170cbba0b60e5f5454ae`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb096667c2eb8e8cc9f745a91245901b951632f05bd4a18c84e5fc700638654e`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1b83dffa45f0edf0a1799b639b0fe41010c6dc26daab3cc2ef4cc0b91d9b0b`  
		Last Modified: Tue, 05 Aug 2025 05:16:22 GMT  
		Size: 35.2 MB (35236910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e32f6aebd439ba8d413a2195d63d2c585e5e02c6dab1edf8a99373046e6e7f3`  
		Last Modified: Tue, 05 Aug 2025 05:16:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916f60b60679cd13e5b42e54a54ce09c04ab6190fdb74ff15b55e7fb95b2dcbe`  
		Last Modified: Tue, 05 Aug 2025 05:18:14 GMT  
		Size: 742.4 KB (742354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e92b3fe9ba0e875f17c6c795b8a20084b71790b3dbde102dd29529b31ba2515`  
		Last Modified: Tue, 05 Aug 2025 05:18:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43b960d784625431b6d77f73ca73ddb5e698c47e2e9c9fb7e2d650746e9112b`  
		Last Modified: Tue, 05 Aug 2025 05:18:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:f229c5947d89c599f62886150c208726d8611a3aa479290d0c23507089fb1f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544a30442166ccf22fc930b2963e678d967a0c11d780cedfc912151c3d57c609`

```dockerfile
```

-	Layers:
	-	`sha256:4cac9e7de0807a5b2dd0c792f33add966b44cc9b59e0fce839b6dc5c214549df`  
		Last Modified: Tue, 05 Aug 2025 07:13:35 GMT  
		Size: 2.2 MB (2167861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb721c92b0bc772ea37e599a564c6644471bec757fade7e44562e289ca595d9`  
		Last Modified: Tue, 05 Aug 2025 07:13:35 GMT  
		Size: 31.4 KB (31398 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:242a86ee1f2a4972b4a5fd4c56c3f3e28a9d3145ff2185c79952cb9127a0f38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73598633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93629e5855d8a26a43486c3bc80104e59c8461452b0bab0b4f77fe92fd3da805`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c69a28ac4d61cac15663b00afee7413a9a9efb61c173baf6d196a4a2b9eec`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 13.7 MB (13653334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e800d2c2d3dcabafd275ce5da9cd5b69a400c8d4e434fe0e169de8f847150c16`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc97540dd5b29ed35499d386792721453e9f2993fb6f31092fe292cb6cda3058`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 20.4 MB (20394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d682aa8b41ba1c48a1513a4764d3db005a8137af9425b4d401f86d8da3f88`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b4c9e4ab292bff4638f9d9c3c6bc2450aaf32e67ac31c00ae732b7f092d3c`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb9edc9e8c62872be6f09d92a7e349b9ecbbf22f3ca071428c2f79c001def07`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881222ef14b0d5e786e3466828f16530cdf02394d48ed40521acec353050c3e8`  
		Last Modified: Wed, 06 Aug 2025 09:08:34 GMT  
		Size: 31.1 MB (31108914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c5d76f8d2e998778c7ad2d7c0bbe518c050e6e366cdc8dcc6ea90cc70961`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d7ba92160d829f4a1147899670be733f3b8117bd926eb56223e0482b62682d`  
		Last Modified: Wed, 06 Aug 2025 09:18:39 GMT  
		Size: 1.3 MB (1290273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d80c36800cf582b2c2406ace451dfac0b65aecc35a93c610f45e7f392d324`  
		Last Modified: Wed, 06 Aug 2025 09:18:40 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780ba637a7eb98e40bdb5151ed089eaa9a780374151efc76375115e950f90695`  
		Last Modified: Wed, 06 Aug 2025 09:18:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:bd905e926b62b2d9eef4c53d2b3c04a5bd467e69776f1f1f15e5b9f17b6ec215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e46afb38fc67fcb9d774406047a771b5cd67d3d7fba007d67d137b0713d6a8`

```dockerfile
```

-	Layers:
	-	`sha256:bd1c8aeb78950f04da58e1d9dada364adc7af0b0f1724b1964e2a62527d9fe63`  
		Last Modified: Wed, 06 Aug 2025 10:13:37 GMT  
		Size: 2.2 MB (2166128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0fecf4c0913683031404dcde1dd78d737ecddf4a7495c4ee3f8ba06413db13`  
		Last Modified: Wed, 06 Aug 2025 10:13:37 GMT  
		Size: 31.4 KB (31401 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:58bdb1d4ca462f708b185894b4697a35704daba6aab4122cc52c0015f653f125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75051335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161cd63851c613ce699ee9318c5c5b8d68d41eac056d0d2d1a4dc31f464b0635`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08eafa4a3224fe6eb688860741f0e8b65ac49b919952d4a7d1e5a4d195e134b`  
		Last Modified: Mon, 04 Aug 2025 22:58:42 GMT  
		Size: 13.7 MB (13653336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796e5c7e7fd28fa790bea89b2528028cbd5ba464a2cb410bd870445103de9197`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd0c014783d431392fbe4b78080b9c1485624e796271f5c4962f96941a32672`  
		Last Modified: Mon, 04 Aug 2025 22:58:56 GMT  
		Size: 21.5 MB (21451616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2a328a5b7b993670851ac5c6d63c129a67f13f999a03570b930367d089028`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5907607760dc2ba6786bf93d6c9d658346353233ad6c45f9d5bb678fb84e4ea`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18809b1760a6fe568eea4d22f4a08260e8eb4844a67a924b8f1ad360fcc505a0`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d55c6b75b483330745503675543c8c8cd53487c52f04fc538ffca072685af4`  
		Last Modified: Tue, 05 Aug 2025 03:05:15 GMT  
		Size: 31.8 MB (31838538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e906a6e05460592955352f726700115f5fd99ecac21d52a8a8f215008ac11b`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45f7df5f4295792ceefd0adfa37e8b7e545c982b334f8c2641cf5382c7f5700`  
		Last Modified: Tue, 05 Aug 2025 03:07:13 GMT  
		Size: 738.7 KB (738681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b70fd5741010b697ca1671dbc0ea62d414fc02f11b7a47ae485b4b4e5765eb`  
		Last Modified: Tue, 05 Aug 2025 03:07:12 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e37f21e57c8269cd9982e3a616240b1ddb3688578545ef69e210b32e6aae1fc`  
		Last Modified: Tue, 05 Aug 2025 03:07:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:0255b45872e93067f760754d6af6b4555837380e83cdfae233f9298cfd4ff1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65c3714895dc975efb547603eb6327b8a448266f019315dc234aff79df006d1`

```dockerfile
```

-	Layers:
	-	`sha256:a5637a55de3c57719ef68b7f6151f1ed73902c7e04aa17919ecdfdce350f362a`  
		Last Modified: Tue, 05 Aug 2025 04:13:44 GMT  
		Size: 2.2 MB (2165916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3972278882a3e75c399bcff07420440b5e9a5ff47eb0b793376b9d6ea0282b`  
		Last Modified: Tue, 05 Aug 2025 04:13:45 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:6d71e5693b24a8d1d0a6cc0e791d24b9fe8ac5c93dc2a36d04f583e5617af9f7
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

### `composer:1.10` - linux; amd64

```console
$ docker pull composer@sha256:c54003d5eb87c26e5e700769788155cecfaab4e67ba443e58c7b2f073754f556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76594613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0021dafdd4fa74a0706df28a233d5e4fdf23abadba410ae4b883f06db3396a7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b8c404eae668716a1e38e4cfbfa17a24db95c67ac43f1c7fc370b54d3ca087`  
		Last Modified: Mon, 04 Aug 2025 20:49:49 GMT  
		Size: 3.5 MB (3460957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d882c5edba216e9f63d26119702e252a7f88372fa0af1077c58c6f937c29f`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769d794d159afc0f29bb41cae73fa8177791b4078920913550d6035fce888bf2`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3cf3bc6932e6344a1c898a1bdf35235fe0327d7cac86e56f4b07b23b9e9847`  
		Last Modified: Mon, 04 Aug 2025 20:49:51 GMT  
		Size: 13.7 MB (13653337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7066989316ffccd2c577fe6ce99e5bd4047a2f447f99f832d66a2f1cf334e8`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2176a4cebfd98252931aee5773d33b5a3a42d7e11f90f52e09364ad1fa8fd18`  
		Last Modified: Mon, 04 Aug 2025 20:49:52 GMT  
		Size: 21.0 MB (20975718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43e4b7ed65e42eff594acdcad113649b65b82ee4f86ccddb9c65ef1633a2fd7`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d54c809af2e0932d4bc53c9c0fa80cc499fba826b868e3ddc446d3361cb44`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 20.0 KB (19952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2151aa88e776b0b7a7bf7705e4dc7d63b02f2b67ebb32a829a34e18f38c3b1fc`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fe67c28dd380fb9d034436907eba4e9f531e36e618b2250b5db3b7fa8d56cc`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 33.9 MB (33924822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a594a597b20e45f01dbdf35451ac3ea882cf160ff9488af8ef8bf2c9b612b282`  
		Last Modified: Mon, 04 Aug 2025 21:00:13 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d4116fdf820847be31bf0c21a6ef192760c95f72efd1774d228ec7efda633e`  
		Last Modified: Mon, 04 Aug 2025 21:00:13 GMT  
		Size: 735.3 KB (735336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0ed3e474d106de7e08acf6903e1d56e71c8d3a2e0dfb2f6d391a808818381f`  
		Last Modified: Mon, 04 Aug 2025 21:00:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b494f816a6650c915cb5c09c07e675189183a0ca691444f56e3f783b181fe34`  
		Last Modified: Mon, 04 Aug 2025 21:00:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:d1cdcf6c237ba6bdbf471646f24ccbdd2c04030d93f81bd636f88b69d0fa6c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757b09cc5443d2eaf2ea50ba1791348225112fa92ea402f0317cea4bbc4256c6`

```dockerfile
```

-	Layers:
	-	`sha256:9635d825247c25d5bc3361de19612e13680753e9c261c425e43ae0ce4f47fba1`  
		Last Modified: Mon, 04 Aug 2025 22:13:26 GMT  
		Size: 2.2 MB (2169304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcbcd115f72960e4fbd5904250297d12ea1631fda234d7ae3926e6bfba3a356`  
		Last Modified: Mon, 04 Aug 2025 22:13:27 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:30cb45241a9563758dd42abce1bd8ae746fd2546165867530debbf399be23590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74239445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94678d3bf400f557c789f8c1ab4eff13d5813f550f849e54cff0dd524a2e4a0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7494cac4578077d244b00bcd8c4b9cc24cbac12fe484fc52bdb253b7be68d33`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 13.7 MB (13653331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb9d8c4b4750c9afc1de1182d3a39f160769ecb594f5119173d9999fdc1b99`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08da3ca3515f68d5f047717865555b86a20702e1abbb868f91b827eac6e5ebf`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 19.1 MB (19094736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174f8de30188274046eddf1fa9fea9d286fe5b22b08972783323bdc3074e69f9`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890cfd4e2ff1fb6e00ae91a595e532b992ff926f2b1aabb5d5cf4550fc056385`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ba3c18d23646492096ded6ff9adf0df6739c2b4139249d0ae790e82cfb69ae`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab618c8fb396a56d07a5986ec1e2c89587a34750ca91962eb0f8fc69192e86`  
		Last Modified: Mon, 04 Aug 2025 23:52:25 GMT  
		Size: 33.8 MB (33788254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610e01a216465a5a644cfe45ea36450b82393adf820afdeb633ed5876549f9e`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfead96b44b3a2abd1e425fc66f5b4016407daba06dbf7d84204e63ee4ca58b`  
		Last Modified: Mon, 04 Aug 2025 23:53:43 GMT  
		Size: 735.9 KB (735893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f7554a791b8f2097cc9477df1c2a7c4a6df66aeb67a04c3f75e59c1bef76e`  
		Last Modified: Mon, 04 Aug 2025 23:53:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbce85d740fbdb7943bdcd6bef72b8813437a32e1db5a5f25dda0af500063b3`  
		Last Modified: Mon, 04 Aug 2025 23:53:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:5d84303d37b9a44cb875c4a80e280bce213658cfd509a6a29efc975bbc1dc312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93074c139d91d719893295fda37e7db80bdf72b6f5870c3b07285013a6d28d5`

```dockerfile
```

-	Layers:
	-	`sha256:4a1088f36f1313ba6c6fed92467d5d7f309818cb0462ddace41bee2c6e264a59`  
		Last Modified: Tue, 05 Aug 2025 01:13:26 GMT  
		Size: 31.2 KB (31235 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:8a115a37e2e8ca57fe408432f1d77a86dd192b6b77be3ad90cbbebf0e7af1f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71023258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebade064c227a2113cd033a890101531d3249e99b0425e6d2ed3b4470bf86187`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca2e4db931023b2bd56443c80dbf78e53bf1efb748d1e76bf1242168c76cca6`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 13.7 MB (13653322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77469fa7f1256b86a0f5f641b66b80360641be9666ae4294dc5d6be17b7a5d8`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054413e584c9543fe5cdb41980742080a4ae1f7cae6744e77e0218deb7dac34d`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 18.1 MB (18070661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72860d23def789d218635f72e9644f4a04f18a8fa12c536da7af1ffa8743fa3c`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e66e44f6101fa11b28b93eec29aae52f52e35e47962ce16a425ce2822f9f64`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97417a1c0369df9443f468952dc56830ae71371b90f313f4b54c1c3b3f96390`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e233c39dcbf452f1d1e155cfa780907783f14f748767e9311ea6d9865ebc0896`  
		Last Modified: Tue, 05 Aug 2025 02:53:45 GMT  
		Size: 32.1 MB (32068670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45df4acb4b1365a6f7848309ec8384dbef2fded39db7a60a972ed210bacfc2e6`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86df24d504fe85588365a5efd26ce73e03cfbd5084f8bc0cb9e2ec28c7d0e4`  
		Last Modified: Tue, 05 Aug 2025 02:55:21 GMT  
		Size: 726.4 KB (726371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b6ae98d157dd0e1d270649bb4183f040212698e8243da6acacbbe301d6cf33`  
		Last Modified: Tue, 05 Aug 2025 02:55:20 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637a1452ff587f1379e6679c83777e31051f802906b1301a3383e1277053ff20`  
		Last Modified: Tue, 05 Aug 2025 02:55:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:571067be6f007ee91eda644494bbe3086b2746eef580c318e2d99618112be04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067ec23ec78ca2afeb6971e7bc895834f5a68ea3bffdfd1379e63cc53615a08f`

```dockerfile
```

-	Layers:
	-	`sha256:e626cd36a9aaf1b1f231d11893604b0ae06ea9d948a6eb8fd5ada05236989161`  
		Last Modified: Tue, 05 Aug 2025 04:13:30 GMT  
		Size: 2.2 MB (2169620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b7af08b3953fbc0df5df5dbb1593412aa0715fc84babdd30bee01fb818e80d2`  
		Last Modified: Tue, 05 Aug 2025 04:13:30 GMT  
		Size: 31.4 KB (31450 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:3dcc77730658e5a92ec3e049c891e2d3783ba147259296143b85c630ed65ffaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76541931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ccf6b49e1878bae8ff00cd7aa12b0c7f0b5361224812caf066e84b536a7fb8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb504dccc917de6b6b8bbc11ff4b9599d71f3ad971f142f67cc631aea843760`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 3.5 MB (3454743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7532649a0813cdb3165d225287dc7cbef8b4e47991127457849e1947e5549636`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253b9848099c2406835511872822d9dab1ea36834b393e1588c17a784e3bcb1`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973767f0cf0415e63013511841e37ace48afe3d8bbfaafa677dc100c89eb06ec`  
		Last Modified: Tue, 05 Aug 2025 01:42:19 GMT  
		Size: 13.7 MB (13653329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f37d53d2ef75f6d7f5ad4ee6e5eb97589d9dcf67380e28c57d85687f0a1c5c`  
		Last Modified: Tue, 05 Aug 2025 01:42:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3bef5a3676aa8a22d37f4aaaf0f903109f38d4050ea5bbf416baa0f2fdd4e9`  
		Last Modified: Tue, 05 Aug 2025 01:42:20 GMT  
		Size: 20.5 MB (20525567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfec7e98ad7662f3c4c51de1bf161799051d12f213dfd998753921e6a8cbe6d`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa68af9933e1df5a29b63199d57877c41b14c9f12615222a4ae65df1d2b9df`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 19.8 KB (19756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6fec7f9b2035416690d429232af55e7cafdbc99a57c3e473d5b44c4dc43fba`  
		Last Modified: Tue, 05 Aug 2025 01:42:18 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbf0d70d9d667639b695d04960c9fdafdd0aa711ae79b558e2e0959bf5b52f2`  
		Last Modified: Tue, 05 Aug 2025 08:15:54 GMT  
		Size: 34.0 MB (33997952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e41cdc44d3ea60f653b652041902b0f7ce6913b4b4f696e18302e88e07fae1`  
		Last Modified: Tue, 05 Aug 2025 08:15:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09193a92ada83add730d8c0f4282ff6fdc2dc83b456645eb75701f29b92b4d50`  
		Last Modified: Tue, 05 Aug 2025 08:16:45 GMT  
		Size: 735.2 KB (735231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b68cce5f680c42cc5c7d4c751b7f8cf49d2f10bb6e9f1ae0ccc0982642fce47`  
		Last Modified: Tue, 05 Aug 2025 08:16:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305dbefa45742158bf3b592156deda533fc2ed9ae46cea054eab407cc1d37c4b`  
		Last Modified: Tue, 05 Aug 2025 08:16:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:20de4cc4768d0249be875aa4f624b7e51840f3de0348d705ae34408151ef91ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa82a5145e89e22dd1a0107ef892fecfc2e4c94b680bad5594de70bd4d9947e`

```dockerfile
```

-	Layers:
	-	`sha256:e44fad7f5553d4b722182cae416f79ae69d64b1a6257dc1c350f7cd574460fb1`  
		Last Modified: Tue, 05 Aug 2025 10:13:28 GMT  
		Size: 2.2 MB (2169444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5e94a56e2cfd87963c7e9166e5328569b057565f5607c1eb904b044d76e72a`  
		Last Modified: Tue, 05 Aug 2025 10:13:28 GMT  
		Size: 31.5 KB (31478 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:048e4459850cef7ba685421c79ca2501e6dbec1b1f80e2eb9002a10bd76c8242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77518575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d692e30b246a086ca03ab968812cdb2ba47ae767b94913c33c0926b21af2a3a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe8439d75dd031f7f3a6908ae96e53d52128e10c30e23a158b9b8345d576f43`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 3.5 MB (3516254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dedafe9669d1a09c51f168c3d4db6477986ec7b7f4bb274347c5befbf1ab6e1`  
		Last Modified: Mon, 04 Aug 2025 20:50:20 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a8b0cb75e0335ca0c6f5b93ad9737facd671ebe28fba3a32ced09f40d7920b`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b409694fac1f06392e029aa1cce26b25863976e502862723282bece6849fd`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 13.7 MB (13653332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7d6aac432e4a310a74c720b92ddf62f125372b97cf40257ee5385d2159c3be`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abcffe2eb78cea70305ac08e1e90d0ac3e5de7b2671042ae50d8f9dcc2a38df`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 21.5 MB (21505197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4278be9860874f02951ab37abd3b1f199cca3b88299e7b54e4aec44ae9b6c97a`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dfdfedf576c6450fc46466c1f8e3b5b4d8c16aac720b69705113e7b87b3567`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482cd711b6eff6cb6033c515ddc86de794a4ca97eba0a2ff1d2555201ea9187a`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db77b3cf9bfb59dd8cfa41ebffd8d52c201213af184651cb7c46eaffff8c2b97`  
		Last Modified: Mon, 04 Aug 2025 20:58:58 GMT  
		Size: 34.4 MB (34436928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8b6fbed48ae536a36948de7cea211f922b9583682afc0fe4bd94de212fd941`  
		Last Modified: Mon, 04 Aug 2025 20:58:56 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a570db9332eaf689c5bae8c9c3b94bc52d346e385e0f424d60c3a035a73c4f`  
		Last Modified: Mon, 04 Aug 2025 20:58:57 GMT  
		Size: 747.1 KB (747144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ea502e4516812c2831d64f18305a246ba03b6f559b4e9c4571652026e63420`  
		Last Modified: Mon, 04 Aug 2025 20:58:56 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0427f58d49e65068523a6162f6534beded17307cefa29c6c57436ed6a6d25c73`  
		Last Modified: Mon, 04 Aug 2025 20:58:56 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:b1eead030887161ff7006e10184a47ed0bb9bd2181995a08fb76f461b0b22657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f936b82e26a46992a4e41a5dc59853c9f7e7376a7457f4972c1298deeb4ca4d6`

```dockerfile
```

-	Layers:
	-	`sha256:0e665dbd6988ff5a2cc8505b8eb13720ead82e3aea86d933fc0a8964ea613bfb`  
		Last Modified: Mon, 04 Aug 2025 22:13:40 GMT  
		Size: 2.2 MB (2169092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd259450a5705e7ddd47bf34b3bdf666ee12161d5eda15d366fe2b7c5d82583`  
		Last Modified: Mon, 04 Aug 2025 22:13:41 GMT  
		Size: 31.3 KB (31323 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:562aa20440afb6e249f2db8c4f65c1bea49ec0f7c4ac85c02170c9ae9681e7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78893164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fb79b009bdbff99bee3ac535310002302e60c626bbdfc173445cf99e549dea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2149fd89f974e7ea3dea06f37d735922f1379a8f6a3848f9f27b655a231533a`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 13.7 MB (13653344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7733690cb25c9174f17fcd594fb9aa92de487681f9a30a88d38ce0fb49dfc9b7`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56aa0ea4063f0f606994769dabd9afcf81090a22a66567e6f1bbad01c84cef`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 21.9 MB (21877960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555ac5f064703fcb811adc2fc69166c7117941c125b03426671e1d4f55cc4f67`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa79fbfe4077bdecbc88d7a5d32f94313e38f9fcff1170cbba0b60e5f5454ae`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb096667c2eb8e8cc9f745a91245901b951632f05bd4a18c84e5fc700638654e`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1b83dffa45f0edf0a1799b639b0fe41010c6dc26daab3cc2ef4cc0b91d9b0b`  
		Last Modified: Tue, 05 Aug 2025 05:16:22 GMT  
		Size: 35.2 MB (35236910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e32f6aebd439ba8d413a2195d63d2c585e5e02c6dab1edf8a99373046e6e7f3`  
		Last Modified: Tue, 05 Aug 2025 05:16:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916f60b60679cd13e5b42e54a54ce09c04ab6190fdb74ff15b55e7fb95b2dcbe`  
		Last Modified: Tue, 05 Aug 2025 05:18:14 GMT  
		Size: 742.4 KB (742354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e92b3fe9ba0e875f17c6c795b8a20084b71790b3dbde102dd29529b31ba2515`  
		Last Modified: Tue, 05 Aug 2025 05:18:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43b960d784625431b6d77f73ca73ddb5e698c47e2e9c9fb7e2d650746e9112b`  
		Last Modified: Tue, 05 Aug 2025 05:18:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:f229c5947d89c599f62886150c208726d8611a3aa479290d0c23507089fb1f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544a30442166ccf22fc930b2963e678d967a0c11d780cedfc912151c3d57c609`

```dockerfile
```

-	Layers:
	-	`sha256:4cac9e7de0807a5b2dd0c792f33add966b44cc9b59e0fce839b6dc5c214549df`  
		Last Modified: Tue, 05 Aug 2025 07:13:35 GMT  
		Size: 2.2 MB (2167861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb721c92b0bc772ea37e599a564c6644471bec757fade7e44562e289ca595d9`  
		Last Modified: Tue, 05 Aug 2025 07:13:35 GMT  
		Size: 31.4 KB (31398 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:242a86ee1f2a4972b4a5fd4c56c3f3e28a9d3145ff2185c79952cb9127a0f38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73598633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93629e5855d8a26a43486c3bc80104e59c8461452b0bab0b4f77fe92fd3da805`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c69a28ac4d61cac15663b00afee7413a9a9efb61c173baf6d196a4a2b9eec`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 13.7 MB (13653334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e800d2c2d3dcabafd275ce5da9cd5b69a400c8d4e434fe0e169de8f847150c16`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc97540dd5b29ed35499d386792721453e9f2993fb6f31092fe292cb6cda3058`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 20.4 MB (20394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d682aa8b41ba1c48a1513a4764d3db005a8137af9425b4d401f86d8da3f88`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b4c9e4ab292bff4638f9d9c3c6bc2450aaf32e67ac31c00ae732b7f092d3c`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb9edc9e8c62872be6f09d92a7e349b9ecbbf22f3ca071428c2f79c001def07`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881222ef14b0d5e786e3466828f16530cdf02394d48ed40521acec353050c3e8`  
		Last Modified: Wed, 06 Aug 2025 09:08:34 GMT  
		Size: 31.1 MB (31108914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c5d76f8d2e998778c7ad2d7c0bbe518c050e6e366cdc8dcc6ea90cc70961`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d7ba92160d829f4a1147899670be733f3b8117bd926eb56223e0482b62682d`  
		Last Modified: Wed, 06 Aug 2025 09:18:39 GMT  
		Size: 1.3 MB (1290273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d80c36800cf582b2c2406ace451dfac0b65aecc35a93c610f45e7f392d324`  
		Last Modified: Wed, 06 Aug 2025 09:18:40 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780ba637a7eb98e40bdb5151ed089eaa9a780374151efc76375115e950f90695`  
		Last Modified: Wed, 06 Aug 2025 09:18:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:bd905e926b62b2d9eef4c53d2b3c04a5bd467e69776f1f1f15e5b9f17b6ec215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e46afb38fc67fcb9d774406047a771b5cd67d3d7fba007d67d137b0713d6a8`

```dockerfile
```

-	Layers:
	-	`sha256:bd1c8aeb78950f04da58e1d9dada364adc7af0b0f1724b1964e2a62527d9fe63`  
		Last Modified: Wed, 06 Aug 2025 10:13:37 GMT  
		Size: 2.2 MB (2166128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0fecf4c0913683031404dcde1dd78d737ecddf4a7495c4ee3f8ba06413db13`  
		Last Modified: Wed, 06 Aug 2025 10:13:37 GMT  
		Size: 31.4 KB (31401 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:58bdb1d4ca462f708b185894b4697a35704daba6aab4122cc52c0015f653f125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75051335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161cd63851c613ce699ee9318c5c5b8d68d41eac056d0d2d1a4dc31f464b0635`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08eafa4a3224fe6eb688860741f0e8b65ac49b919952d4a7d1e5a4d195e134b`  
		Last Modified: Mon, 04 Aug 2025 22:58:42 GMT  
		Size: 13.7 MB (13653336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796e5c7e7fd28fa790bea89b2528028cbd5ba464a2cb410bd870445103de9197`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd0c014783d431392fbe4b78080b9c1485624e796271f5c4962f96941a32672`  
		Last Modified: Mon, 04 Aug 2025 22:58:56 GMT  
		Size: 21.5 MB (21451616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2a328a5b7b993670851ac5c6d63c129a67f13f999a03570b930367d089028`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5907607760dc2ba6786bf93d6c9d658346353233ad6c45f9d5bb678fb84e4ea`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18809b1760a6fe568eea4d22f4a08260e8eb4844a67a924b8f1ad360fcc505a0`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d55c6b75b483330745503675543c8c8cd53487c52f04fc538ffca072685af4`  
		Last Modified: Tue, 05 Aug 2025 03:05:15 GMT  
		Size: 31.8 MB (31838538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e906a6e05460592955352f726700115f5fd99ecac21d52a8a8f215008ac11b`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45f7df5f4295792ceefd0adfa37e8b7e545c982b334f8c2641cf5382c7f5700`  
		Last Modified: Tue, 05 Aug 2025 03:07:13 GMT  
		Size: 738.7 KB (738681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b70fd5741010b697ca1671dbc0ea62d414fc02f11b7a47ae485b4b4e5765eb`  
		Last Modified: Tue, 05 Aug 2025 03:07:12 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e37f21e57c8269cd9982e3a616240b1ddb3688578545ef69e210b32e6aae1fc`  
		Last Modified: Tue, 05 Aug 2025 03:07:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:0255b45872e93067f760754d6af6b4555837380e83cdfae233f9298cfd4ff1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65c3714895dc975efb547603eb6327b8a448266f019315dc234aff79df006d1`

```dockerfile
```

-	Layers:
	-	`sha256:a5637a55de3c57719ef68b7f6151f1ed73902c7e04aa17919ecdfdce350f362a`  
		Last Modified: Tue, 05 Aug 2025 04:13:44 GMT  
		Size: 2.2 MB (2165916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3972278882a3e75c399bcff07420440b5e9a5ff47eb0b793376b9d6ea0282b`  
		Last Modified: Tue, 05 Aug 2025 04:13:45 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:6d71e5693b24a8d1d0a6cc0e791d24b9fe8ac5c93dc2a36d04f583e5617af9f7
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

### `composer:1.10.27` - linux; amd64

```console
$ docker pull composer@sha256:c54003d5eb87c26e5e700769788155cecfaab4e67ba443e58c7b2f073754f556
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76594613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0021dafdd4fa74a0706df28a233d5e4fdf23abadba410ae4b883f06db3396a7d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b8c404eae668716a1e38e4cfbfa17a24db95c67ac43f1c7fc370b54d3ca087`  
		Last Modified: Mon, 04 Aug 2025 20:49:49 GMT  
		Size: 3.5 MB (3460957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d882c5edba216e9f63d26119702e252a7f88372fa0af1077c58c6f937c29f`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769d794d159afc0f29bb41cae73fa8177791b4078920913550d6035fce888bf2`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3cf3bc6932e6344a1c898a1bdf35235fe0327d7cac86e56f4b07b23b9e9847`  
		Last Modified: Mon, 04 Aug 2025 20:49:51 GMT  
		Size: 13.7 MB (13653337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7066989316ffccd2c577fe6ce99e5bd4047a2f447f99f832d66a2f1cf334e8`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2176a4cebfd98252931aee5773d33b5a3a42d7e11f90f52e09364ad1fa8fd18`  
		Last Modified: Mon, 04 Aug 2025 20:49:52 GMT  
		Size: 21.0 MB (20975718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43e4b7ed65e42eff594acdcad113649b65b82ee4f86ccddb9c65ef1633a2fd7`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d54c809af2e0932d4bc53c9c0fa80cc499fba826b868e3ddc446d3361cb44`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 20.0 KB (19952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2151aa88e776b0b7a7bf7705e4dc7d63b02f2b67ebb32a829a34e18f38c3b1fc`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fe67c28dd380fb9d034436907eba4e9f531e36e618b2250b5db3b7fa8d56cc`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 33.9 MB (33924822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a594a597b20e45f01dbdf35451ac3ea882cf160ff9488af8ef8bf2c9b612b282`  
		Last Modified: Mon, 04 Aug 2025 21:00:13 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d4116fdf820847be31bf0c21a6ef192760c95f72efd1774d228ec7efda633e`  
		Last Modified: Mon, 04 Aug 2025 21:00:13 GMT  
		Size: 735.3 KB (735336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0ed3e474d106de7e08acf6903e1d56e71c8d3a2e0dfb2f6d391a808818381f`  
		Last Modified: Mon, 04 Aug 2025 21:00:13 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b494f816a6650c915cb5c09c07e675189183a0ca691444f56e3f783b181fe34`  
		Last Modified: Mon, 04 Aug 2025 21:00:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:d1cdcf6c237ba6bdbf471646f24ccbdd2c04030d93f81bd636f88b69d0fa6c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757b09cc5443d2eaf2ea50ba1791348225112fa92ea402f0317cea4bbc4256c6`

```dockerfile
```

-	Layers:
	-	`sha256:9635d825247c25d5bc3361de19612e13680753e9c261c425e43ae0ce4f47fba1`  
		Last Modified: Mon, 04 Aug 2025 22:13:26 GMT  
		Size: 2.2 MB (2169304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcbcd115f72960e4fbd5904250297d12ea1631fda234d7ae3926e6bfba3a356`  
		Last Modified: Mon, 04 Aug 2025 22:13:27 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:30cb45241a9563758dd42abce1bd8ae746fd2546165867530debbf399be23590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74239445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d94678d3bf400f557c789f8c1ab4eff13d5813f550f849e54cff0dd524a2e4a0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7494cac4578077d244b00bcd8c4b9cc24cbac12fe484fc52bdb253b7be68d33`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 13.7 MB (13653331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb9d8c4b4750c9afc1de1182d3a39f160769ecb594f5119173d9999fdc1b99`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08da3ca3515f68d5f047717865555b86a20702e1abbb868f91b827eac6e5ebf`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 19.1 MB (19094736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174f8de30188274046eddf1fa9fea9d286fe5b22b08972783323bdc3074e69f9`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890cfd4e2ff1fb6e00ae91a595e532b992ff926f2b1aabb5d5cf4550fc056385`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ba3c18d23646492096ded6ff9adf0df6739c2b4139249d0ae790e82cfb69ae`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab618c8fb396a56d07a5986ec1e2c89587a34750ca91962eb0f8fc69192e86`  
		Last Modified: Mon, 04 Aug 2025 23:52:25 GMT  
		Size: 33.8 MB (33788254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610e01a216465a5a644cfe45ea36450b82393adf820afdeb633ed5876549f9e`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dfead96b44b3a2abd1e425fc66f5b4016407daba06dbf7d84204e63ee4ca58b`  
		Last Modified: Mon, 04 Aug 2025 23:53:43 GMT  
		Size: 735.9 KB (735893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254f7554a791b8f2097cc9477df1c2a7c4a6df66aeb67a04c3f75e59c1bef76e`  
		Last Modified: Mon, 04 Aug 2025 23:53:42 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecbce85d740fbdb7943bdcd6bef72b8813437a32e1db5a5f25dda0af500063b3`  
		Last Modified: Mon, 04 Aug 2025 23:53:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:5d84303d37b9a44cb875c4a80e280bce213658cfd509a6a29efc975bbc1dc312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.2 KB (31235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93074c139d91d719893295fda37e7db80bdf72b6f5870c3b07285013a6d28d5`

```dockerfile
```

-	Layers:
	-	`sha256:4a1088f36f1313ba6c6fed92467d5d7f309818cb0462ddace41bee2c6e264a59`  
		Last Modified: Tue, 05 Aug 2025 01:13:26 GMT  
		Size: 31.2 KB (31235 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:8a115a37e2e8ca57fe408432f1d77a86dd192b6b77be3ad90cbbebf0e7af1f6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71023258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebade064c227a2113cd033a890101531d3249e99b0425e6d2ed3b4470bf86187`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca2e4db931023b2bd56443c80dbf78e53bf1efb748d1e76bf1242168c76cca6`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 13.7 MB (13653322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77469fa7f1256b86a0f5f641b66b80360641be9666ae4294dc5d6be17b7a5d8`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054413e584c9543fe5cdb41980742080a4ae1f7cae6744e77e0218deb7dac34d`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 18.1 MB (18070661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72860d23def789d218635f72e9644f4a04f18a8fa12c536da7af1ffa8743fa3c`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e66e44f6101fa11b28b93eec29aae52f52e35e47962ce16a425ce2822f9f64`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97417a1c0369df9443f468952dc56830ae71371b90f313f4b54c1c3b3f96390`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e233c39dcbf452f1d1e155cfa780907783f14f748767e9311ea6d9865ebc0896`  
		Last Modified: Tue, 05 Aug 2025 02:53:45 GMT  
		Size: 32.1 MB (32068670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45df4acb4b1365a6f7848309ec8384dbef2fded39db7a60a972ed210bacfc2e6`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d86df24d504fe85588365a5efd26ce73e03cfbd5084f8bc0cb9e2ec28c7d0e4`  
		Last Modified: Tue, 05 Aug 2025 02:55:21 GMT  
		Size: 726.4 KB (726371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b6ae98d157dd0e1d270649bb4183f040212698e8243da6acacbbe301d6cf33`  
		Last Modified: Tue, 05 Aug 2025 02:55:20 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637a1452ff587f1379e6679c83777e31051f802906b1301a3383e1277053ff20`  
		Last Modified: Tue, 05 Aug 2025 02:55:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:571067be6f007ee91eda644494bbe3086b2746eef580c318e2d99618112be04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:067ec23ec78ca2afeb6971e7bc895834f5a68ea3bffdfd1379e63cc53615a08f`

```dockerfile
```

-	Layers:
	-	`sha256:e626cd36a9aaf1b1f231d11893604b0ae06ea9d948a6eb8fd5ada05236989161`  
		Last Modified: Tue, 05 Aug 2025 04:13:30 GMT  
		Size: 2.2 MB (2169620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b7af08b3953fbc0df5df5dbb1593412aa0715fc84babdd30bee01fb818e80d2`  
		Last Modified: Tue, 05 Aug 2025 04:13:30 GMT  
		Size: 31.4 KB (31450 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:3dcc77730658e5a92ec3e049c891e2d3783ba147259296143b85c630ed65ffaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76541931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ccf6b49e1878bae8ff00cd7aa12b0c7f0b5361224812caf066e84b536a7fb8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb504dccc917de6b6b8bbc11ff4b9599d71f3ad971f142f67cc631aea843760`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 3.5 MB (3454743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7532649a0813cdb3165d225287dc7cbef8b4e47991127457849e1947e5549636`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253b9848099c2406835511872822d9dab1ea36834b393e1588c17a784e3bcb1`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973767f0cf0415e63013511841e37ace48afe3d8bbfaafa677dc100c89eb06ec`  
		Last Modified: Tue, 05 Aug 2025 01:42:19 GMT  
		Size: 13.7 MB (13653329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f37d53d2ef75f6d7f5ad4ee6e5eb97589d9dcf67380e28c57d85687f0a1c5c`  
		Last Modified: Tue, 05 Aug 2025 01:42:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3bef5a3676aa8a22d37f4aaaf0f903109f38d4050ea5bbf416baa0f2fdd4e9`  
		Last Modified: Tue, 05 Aug 2025 01:42:20 GMT  
		Size: 20.5 MB (20525567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfec7e98ad7662f3c4c51de1bf161799051d12f213dfd998753921e6a8cbe6d`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa68af9933e1df5a29b63199d57877c41b14c9f12615222a4ae65df1d2b9df`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 19.8 KB (19756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6fec7f9b2035416690d429232af55e7cafdbc99a57c3e473d5b44c4dc43fba`  
		Last Modified: Tue, 05 Aug 2025 01:42:18 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbf0d70d9d667639b695d04960c9fdafdd0aa711ae79b558e2e0959bf5b52f2`  
		Last Modified: Tue, 05 Aug 2025 08:15:54 GMT  
		Size: 34.0 MB (33997952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e41cdc44d3ea60f653b652041902b0f7ce6913b4b4f696e18302e88e07fae1`  
		Last Modified: Tue, 05 Aug 2025 08:15:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09193a92ada83add730d8c0f4282ff6fdc2dc83b456645eb75701f29b92b4d50`  
		Last Modified: Tue, 05 Aug 2025 08:16:45 GMT  
		Size: 735.2 KB (735231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b68cce5f680c42cc5c7d4c751b7f8cf49d2f10bb6e9f1ae0ccc0982642fce47`  
		Last Modified: Tue, 05 Aug 2025 08:16:44 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305dbefa45742158bf3b592156deda533fc2ed9ae46cea054eab407cc1d37c4b`  
		Last Modified: Tue, 05 Aug 2025 08:16:44 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:20de4cc4768d0249be875aa4f624b7e51840f3de0348d705ae34408151ef91ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa82a5145e89e22dd1a0107ef892fecfc2e4c94b680bad5594de70bd4d9947e`

```dockerfile
```

-	Layers:
	-	`sha256:e44fad7f5553d4b722182cae416f79ae69d64b1a6257dc1c350f7cd574460fb1`  
		Last Modified: Tue, 05 Aug 2025 10:13:28 GMT  
		Size: 2.2 MB (2169444 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d5e94a56e2cfd87963c7e9166e5328569b057565f5607c1eb904b044d76e72a`  
		Last Modified: Tue, 05 Aug 2025 10:13:28 GMT  
		Size: 31.5 KB (31478 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:048e4459850cef7ba685421c79ca2501e6dbec1b1f80e2eb9002a10bd76c8242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77518575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d692e30b246a086ca03ab968812cdb2ba47ae767b94913c33c0926b21af2a3a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe8439d75dd031f7f3a6908ae96e53d52128e10c30e23a158b9b8345d576f43`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 3.5 MB (3516254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dedafe9669d1a09c51f168c3d4db6477986ec7b7f4bb274347c5befbf1ab6e1`  
		Last Modified: Mon, 04 Aug 2025 20:50:20 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a8b0cb75e0335ca0c6f5b93ad9737facd671ebe28fba3a32ced09f40d7920b`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b409694fac1f06392e029aa1cce26b25863976e502862723282bece6849fd`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 13.7 MB (13653332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7d6aac432e4a310a74c720b92ddf62f125372b97cf40257ee5385d2159c3be`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abcffe2eb78cea70305ac08e1e90d0ac3e5de7b2671042ae50d8f9dcc2a38df`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 21.5 MB (21505197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4278be9860874f02951ab37abd3b1f199cca3b88299e7b54e4aec44ae9b6c97a`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dfdfedf576c6450fc46466c1f8e3b5b4d8c16aac720b69705113e7b87b3567`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482cd711b6eff6cb6033c515ddc86de794a4ca97eba0a2ff1d2555201ea9187a`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db77b3cf9bfb59dd8cfa41ebffd8d52c201213af184651cb7c46eaffff8c2b97`  
		Last Modified: Mon, 04 Aug 2025 20:58:58 GMT  
		Size: 34.4 MB (34436928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8b6fbed48ae536a36948de7cea211f922b9583682afc0fe4bd94de212fd941`  
		Last Modified: Mon, 04 Aug 2025 20:58:56 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a570db9332eaf689c5bae8c9c3b94bc52d346e385e0f424d60c3a035a73c4f`  
		Last Modified: Mon, 04 Aug 2025 20:58:57 GMT  
		Size: 747.1 KB (747144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ea502e4516812c2831d64f18305a246ba03b6f559b4e9c4571652026e63420`  
		Last Modified: Mon, 04 Aug 2025 20:58:56 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0427f58d49e65068523a6162f6534beded17307cefa29c6c57436ed6a6d25c73`  
		Last Modified: Mon, 04 Aug 2025 20:58:56 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:b1eead030887161ff7006e10184a47ed0bb9bd2181995a08fb76f461b0b22657
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2200415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f936b82e26a46992a4e41a5dc59853c9f7e7376a7457f4972c1298deeb4ca4d6`

```dockerfile
```

-	Layers:
	-	`sha256:0e665dbd6988ff5a2cc8505b8eb13720ead82e3aea86d933fc0a8964ea613bfb`  
		Last Modified: Mon, 04 Aug 2025 22:13:40 GMT  
		Size: 2.2 MB (2169092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbd259450a5705e7ddd47bf34b3bdf666ee12161d5eda15d366fe2b7c5d82583`  
		Last Modified: Mon, 04 Aug 2025 22:13:41 GMT  
		Size: 31.3 KB (31323 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:562aa20440afb6e249f2db8c4f65c1bea49ec0f7c4ac85c02170c9ae9681e7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.9 MB (78893164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fb79b009bdbff99bee3ac535310002302e60c626bbdfc173445cf99e549dea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2149fd89f974e7ea3dea06f37d735922f1379a8f6a3848f9f27b655a231533a`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 13.7 MB (13653344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7733690cb25c9174f17fcd594fb9aa92de487681f9a30a88d38ce0fb49dfc9b7`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56aa0ea4063f0f606994769dabd9afcf81090a22a66567e6f1bbad01c84cef`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 21.9 MB (21877960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555ac5f064703fcb811adc2fc69166c7117941c125b03426671e1d4f55cc4f67`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa79fbfe4077bdecbc88d7a5d32f94313e38f9fcff1170cbba0b60e5f5454ae`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb096667c2eb8e8cc9f745a91245901b951632f05bd4a18c84e5fc700638654e`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1b83dffa45f0edf0a1799b639b0fe41010c6dc26daab3cc2ef4cc0b91d9b0b`  
		Last Modified: Tue, 05 Aug 2025 05:16:22 GMT  
		Size: 35.2 MB (35236910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e32f6aebd439ba8d413a2195d63d2c585e5e02c6dab1edf8a99373046e6e7f3`  
		Last Modified: Tue, 05 Aug 2025 05:16:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916f60b60679cd13e5b42e54a54ce09c04ab6190fdb74ff15b55e7fb95b2dcbe`  
		Last Modified: Tue, 05 Aug 2025 05:18:14 GMT  
		Size: 742.4 KB (742354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e92b3fe9ba0e875f17c6c795b8a20084b71790b3dbde102dd29529b31ba2515`  
		Last Modified: Tue, 05 Aug 2025 05:18:14 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43b960d784625431b6d77f73ca73ddb5e698c47e2e9c9fb7e2d650746e9112b`  
		Last Modified: Tue, 05 Aug 2025 05:18:14 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:f229c5947d89c599f62886150c208726d8611a3aa479290d0c23507089fb1f43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:544a30442166ccf22fc930b2963e678d967a0c11d780cedfc912151c3d57c609`

```dockerfile
```

-	Layers:
	-	`sha256:4cac9e7de0807a5b2dd0c792f33add966b44cc9b59e0fce839b6dc5c214549df`  
		Last Modified: Tue, 05 Aug 2025 07:13:35 GMT  
		Size: 2.2 MB (2167861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bb721c92b0bc772ea37e599a564c6644471bec757fade7e44562e289ca595d9`  
		Last Modified: Tue, 05 Aug 2025 07:13:35 GMT  
		Size: 31.4 KB (31398 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:242a86ee1f2a4972b4a5fd4c56c3f3e28a9d3145ff2185c79952cb9127a0f38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73598633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93629e5855d8a26a43486c3bc80104e59c8461452b0bab0b4f77fe92fd3da805`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c69a28ac4d61cac15663b00afee7413a9a9efb61c173baf6d196a4a2b9eec`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 13.7 MB (13653334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e800d2c2d3dcabafd275ce5da9cd5b69a400c8d4e434fe0e169de8f847150c16`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc97540dd5b29ed35499d386792721453e9f2993fb6f31092fe292cb6cda3058`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 20.4 MB (20394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d682aa8b41ba1c48a1513a4764d3db005a8137af9425b4d401f86d8da3f88`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b4c9e4ab292bff4638f9d9c3c6bc2450aaf32e67ac31c00ae732b7f092d3c`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb9edc9e8c62872be6f09d92a7e349b9ecbbf22f3ca071428c2f79c001def07`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881222ef14b0d5e786e3466828f16530cdf02394d48ed40521acec353050c3e8`  
		Last Modified: Wed, 06 Aug 2025 09:08:34 GMT  
		Size: 31.1 MB (31108914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c5d76f8d2e998778c7ad2d7c0bbe518c050e6e366cdc8dcc6ea90cc70961`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d7ba92160d829f4a1147899670be733f3b8117bd926eb56223e0482b62682d`  
		Last Modified: Wed, 06 Aug 2025 09:18:39 GMT  
		Size: 1.3 MB (1290273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02d80c36800cf582b2c2406ace451dfac0b65aecc35a93c610f45e7f392d324`  
		Last Modified: Wed, 06 Aug 2025 09:18:40 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780ba637a7eb98e40bdb5151ed089eaa9a780374151efc76375115e950f90695`  
		Last Modified: Wed, 06 Aug 2025 09:18:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:bd905e926b62b2d9eef4c53d2b3c04a5bd467e69776f1f1f15e5b9f17b6ec215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e46afb38fc67fcb9d774406047a771b5cd67d3d7fba007d67d137b0713d6a8`

```dockerfile
```

-	Layers:
	-	`sha256:bd1c8aeb78950f04da58e1d9dada364adc7af0b0f1724b1964e2a62527d9fe63`  
		Last Modified: Wed, 06 Aug 2025 10:13:37 GMT  
		Size: 2.2 MB (2166128 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa0fecf4c0913683031404dcde1dd78d737ecddf4a7495c4ee3f8ba06413db13`  
		Last Modified: Wed, 06 Aug 2025 10:13:37 GMT  
		Size: 31.4 KB (31401 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:58bdb1d4ca462f708b185894b4697a35704daba6aab4122cc52c0015f653f125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75051335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161cd63851c613ce699ee9318c5c5b8d68d41eac056d0d2d1a4dc31f464b0635`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08eafa4a3224fe6eb688860741f0e8b65ac49b919952d4a7d1e5a4d195e134b`  
		Last Modified: Mon, 04 Aug 2025 22:58:42 GMT  
		Size: 13.7 MB (13653336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796e5c7e7fd28fa790bea89b2528028cbd5ba464a2cb410bd870445103de9197`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd0c014783d431392fbe4b78080b9c1485624e796271f5c4962f96941a32672`  
		Last Modified: Mon, 04 Aug 2025 22:58:56 GMT  
		Size: 21.5 MB (21451616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2a328a5b7b993670851ac5c6d63c129a67f13f999a03570b930367d089028`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5907607760dc2ba6786bf93d6c9d658346353233ad6c45f9d5bb678fb84e4ea`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18809b1760a6fe568eea4d22f4a08260e8eb4844a67a924b8f1ad360fcc505a0`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d55c6b75b483330745503675543c8c8cd53487c52f04fc538ffca072685af4`  
		Last Modified: Tue, 05 Aug 2025 03:05:15 GMT  
		Size: 31.8 MB (31838538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e906a6e05460592955352f726700115f5fd99ecac21d52a8a8f215008ac11b`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d45f7df5f4295792ceefd0adfa37e8b7e545c982b334f8c2641cf5382c7f5700`  
		Last Modified: Tue, 05 Aug 2025 03:07:13 GMT  
		Size: 738.7 KB (738681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b70fd5741010b697ca1671dbc0ea62d414fc02f11b7a47ae485b4b4e5765eb`  
		Last Modified: Tue, 05 Aug 2025 03:07:12 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e37f21e57c8269cd9982e3a616240b1ddb3688578545ef69e210b32e6aae1fc`  
		Last Modified: Tue, 05 Aug 2025 03:07:11 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:0255b45872e93067f760754d6af6b4555837380e83cdfae233f9298cfd4ff1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65c3714895dc975efb547603eb6327b8a448266f019315dc234aff79df006d1`

```dockerfile
```

-	Layers:
	-	`sha256:a5637a55de3c57719ef68b7f6151f1ed73902c7e04aa17919ecdfdce350f362a`  
		Last Modified: Tue, 05 Aug 2025 04:13:44 GMT  
		Size: 2.2 MB (2165916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b3972278882a3e75c399bcff07420440b5e9a5ff47eb0b793376b9d6ea0282b`  
		Last Modified: Tue, 05 Aug 2025 04:13:45 GMT  
		Size: 31.4 KB (31356 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:20462d70afcfa999ad75dbd9333194067f4d869078bdb37430339e8d97e541d6
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

### `composer:2` - linux; amd64

```console
$ docker pull composer@sha256:3945507689e27f577e4c251ce0a3f0d5d37b51c11d177874c2e485afd37cd747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76830755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe866d01c638502b5aabe801f86c9dac2b1934bb955d8f290079a12c23d3ecd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b8c404eae668716a1e38e4cfbfa17a24db95c67ac43f1c7fc370b54d3ca087`  
		Last Modified: Mon, 04 Aug 2025 20:49:49 GMT  
		Size: 3.5 MB (3460957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d882c5edba216e9f63d26119702e252a7f88372fa0af1077c58c6f937c29f`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769d794d159afc0f29bb41cae73fa8177791b4078920913550d6035fce888bf2`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3cf3bc6932e6344a1c898a1bdf35235fe0327d7cac86e56f4b07b23b9e9847`  
		Last Modified: Mon, 04 Aug 2025 20:49:51 GMT  
		Size: 13.7 MB (13653337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7066989316ffccd2c577fe6ce99e5bd4047a2f447f99f832d66a2f1cf334e8`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2176a4cebfd98252931aee5773d33b5a3a42d7e11f90f52e09364ad1fa8fd18`  
		Last Modified: Mon, 04 Aug 2025 20:49:52 GMT  
		Size: 21.0 MB (20975718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43e4b7ed65e42eff594acdcad113649b65b82ee4f86ccddb9c65ef1633a2fd7`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d54c809af2e0932d4bc53c9c0fa80cc499fba826b868e3ddc446d3361cb44`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 20.0 KB (19952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2151aa88e776b0b7a7bf7705e4dc7d63b02f2b67ebb32a829a34e18f38c3b1fc`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3d748b962dbf28c3f32f875009988343f709a6675518d6429dc81d248756a1`  
		Last Modified: Mon, 04 Aug 2025 21:00:24 GMT  
		Size: 33.9 MB (33925437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9807502fbc2a249159230ea6e961954135898e05417c88f8defbceb2fa9928f0`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993df12ef1b29b3ae5a8b6bb85419d981c1aef5d61e6725946675969265a84fc`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 970.9 KB (970855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69faa1b1fca1e579936e8775bf5d5dd6bd03432d2c68e19af29d19221bea2415`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d304213f65bda4383fcb1d13533167474be38480be6fdaf430ea96783d494d6d`  
		Last Modified: Mon, 04 Aug 2025 21:00:18 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:7d50db5b0c2bd627980ff70892d0d3534aca40e2a584a4f5796d6d473b80b38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0432d851d822729c57cdaf2c173cbc30284b27d82a0043e6403ab0ef45c0ce3`

```dockerfile
```

-	Layers:
	-	`sha256:25a8fafdd0ae54a46c9aee4ca880d093d50d7829b4ded946d64268ed54ed6951`  
		Last Modified: Mon, 04 Aug 2025 22:13:41 GMT  
		Size: 2.2 MB (2170802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96bb6a558b9c4d973e5da2679996a1a7ba39eb4c414be2cdc2c1c2b83911feda`  
		Last Modified: Mon, 04 Aug 2025 22:13:42 GMT  
		Size: 31.7 KB (31654 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:cbb23c77f4df826d1b8f662c82dc7f1f0c2c0979117ad5c64e1bddb11f00b223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74474554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b5565e8b37ed3e30397a672bd962362b10856219a859f824eaed5f52001e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7494cac4578077d244b00bcd8c4b9cc24cbac12fe484fc52bdb253b7be68d33`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 13.7 MB (13653331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb9d8c4b4750c9afc1de1182d3a39f160769ecb594f5119173d9999fdc1b99`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08da3ca3515f68d5f047717865555b86a20702e1abbb868f91b827eac6e5ebf`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 19.1 MB (19094736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174f8de30188274046eddf1fa9fea9d286fe5b22b08972783323bdc3074e69f9`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890cfd4e2ff1fb6e00ae91a595e532b992ff926f2b1aabb5d5cf4550fc056385`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ba3c18d23646492096ded6ff9adf0df6739c2b4139249d0ae790e82cfb69ae`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab618c8fb396a56d07a5986ec1e2c89587a34750ca91962eb0f8fc69192e86`  
		Last Modified: Mon, 04 Aug 2025 23:52:25 GMT  
		Size: 33.8 MB (33788254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610e01a216465a5a644cfe45ea36450b82393adf820afdeb633ed5876549f9e`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ddb27b58bc85c93cfde9f7f795e727cd01a16c674302be72668df5157c22e7`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 971.0 KB (970991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9086d6cd3389c76fe762d42484c1c888dfeca9c871cb3f8b7b7da3e5e9daed0`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6269c4496e0e22c66528769735b397a32967ed478a0da39ab00af135ae1df3a`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:90dc291226a369e83931948b794817bebe2433c995ccbbdcf54057cd27f5b426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88149dfdda7c8a00cae62b12c288d1042b9d89f9140149d7a3dd74850377f0d9`

```dockerfile
```

-	Layers:
	-	`sha256:65bffdc5d5e71983244c1d19c0e7f2e6f8fcc9d073adfb301077c45674a24633`  
		Last Modified: Tue, 05 Aug 2025 01:13:37 GMT  
		Size: 31.5 KB (31542 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:aea165e2b3f65f9cd6f7a6a2f459d0e0dd57f2dc1168d04dc7bb83815297f470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71258733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc0c514e4ccb94629affdfa6fee21cddaa9a606cde6d5d2b3d7e4f9c2b4e812`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca2e4db931023b2bd56443c80dbf78e53bf1efb748d1e76bf1242168c76cca6`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 13.7 MB (13653322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77469fa7f1256b86a0f5f641b66b80360641be9666ae4294dc5d6be17b7a5d8`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054413e584c9543fe5cdb41980742080a4ae1f7cae6744e77e0218deb7dac34d`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 18.1 MB (18070661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72860d23def789d218635f72e9644f4a04f18a8fa12c536da7af1ffa8743fa3c`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e66e44f6101fa11b28b93eec29aae52f52e35e47962ce16a425ce2822f9f64`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97417a1c0369df9443f468952dc56830ae71371b90f313f4b54c1c3b3f96390`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e233c39dcbf452f1d1e155cfa780907783f14f748767e9311ea6d9865ebc0896`  
		Last Modified: Tue, 05 Aug 2025 02:53:45 GMT  
		Size: 32.1 MB (32068670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45df4acb4b1365a6f7848309ec8384dbef2fded39db7a60a972ed210bacfc2e6`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0f69d706b0cdf49ed91cdd1a1b7e8b969bfe4e3f4cbdacf1230d7a8c536bdc`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 961.8 KB (961837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efde64a5f0035d069cf4f4b2accd54a50d652019c1f2fd0271eceb786e7eb2`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40bff23f29506a22b6724bac2dc8a9824c0aba32267c51a6ac473262c2e6bae`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:c66fb3ea6402a430587463e1bcb0db4d7ebd9212290726253c67df3202c7224e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f4719aff19ca7f9d0eeed9a5eaeeabc532e604eb714685416e18e2797859a9`

```dockerfile
```

-	Layers:
	-	`sha256:c81a4d85161e1d4108c2721183ecd4b588ec6687bca06a85bbdaf51efa44cc36`  
		Last Modified: Tue, 05 Aug 2025 04:14:02 GMT  
		Size: 2.2 MB (2171126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec15c40e803eaf944f6ded66014b9ba769454156b200f0ab3ba2d80341e1c57`  
		Last Modified: Tue, 05 Aug 2025 04:14:03 GMT  
		Size: 31.8 KB (31757 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:08e3389734d346ac8d451fb97c9b278802c73c61f44e439814cdcf0039591d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76777486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbf6534e1e10ffe687e5198e516a78745031e7d63674edace6898059193bcd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb504dccc917de6b6b8bbc11ff4b9599d71f3ad971f142f67cc631aea843760`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 3.5 MB (3454743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7532649a0813cdb3165d225287dc7cbef8b4e47991127457849e1947e5549636`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253b9848099c2406835511872822d9dab1ea36834b393e1588c17a784e3bcb1`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973767f0cf0415e63013511841e37ace48afe3d8bbfaafa677dc100c89eb06ec`  
		Last Modified: Tue, 05 Aug 2025 01:42:19 GMT  
		Size: 13.7 MB (13653329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f37d53d2ef75f6d7f5ad4ee6e5eb97589d9dcf67380e28c57d85687f0a1c5c`  
		Last Modified: Tue, 05 Aug 2025 01:42:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3bef5a3676aa8a22d37f4aaaf0f903109f38d4050ea5bbf416baa0f2fdd4e9`  
		Last Modified: Tue, 05 Aug 2025 01:42:20 GMT  
		Size: 20.5 MB (20525567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfec7e98ad7662f3c4c51de1bf161799051d12f213dfd998753921e6a8cbe6d`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa68af9933e1df5a29b63199d57877c41b14c9f12615222a4ae65df1d2b9df`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 19.8 KB (19756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6fec7f9b2035416690d429232af55e7cafdbc99a57c3e473d5b44c4dc43fba`  
		Last Modified: Tue, 05 Aug 2025 01:42:18 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbf0d70d9d667639b695d04960c9fdafdd0aa711ae79b558e2e0959bf5b52f2`  
		Last Modified: Tue, 05 Aug 2025 08:15:54 GMT  
		Size: 34.0 MB (33997952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e41cdc44d3ea60f653b652041902b0f7ce6913b4b4f696e18302e88e07fae1`  
		Last Modified: Tue, 05 Aug 2025 08:15:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4b9384b9b5dd9ae1d88abf18b42d3a970d84d8913e45e7170fca01c382969b`  
		Last Modified: Tue, 05 Aug 2025 08:15:47 GMT  
		Size: 970.8 KB (970776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3988bc851387ceef0287f5db25480cde4005099a5398d1b1f7cbe49541266834`  
		Last Modified: Tue, 05 Aug 2025 08:15:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e25bb8521481d37023fac2634fdb9f2d972ec7eef18621ea5371fab2e765b1`  
		Last Modified: Tue, 05 Aug 2025 08:15:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:606cae1475f184b8fcf6766e12409fea124e7f126567228b82f74399afea1e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8f91f519d7e4b57e099ebad266b11088f4f8502fe8a9ac82f3744999b5bd16`

```dockerfile
```

-	Layers:
	-	`sha256:8038ff9053185ee45b8d45db485c4408a335878007ac7e71bd5cab69d842dc63`  
		Last Modified: Tue, 05 Aug 2025 10:13:39 GMT  
		Size: 2.2 MB (2170954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d992d60b19bf5a9ddfc63fad4ebe9905a796a336ff427fc16c5709cc28c8b11`  
		Last Modified: Tue, 05 Aug 2025 10:13:40 GMT  
		Size: 31.8 KB (31788 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:d6bc37d9ee867506c3d4365376c7966b3cdece0db1043174f396a2f227975e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77755088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b73057212af6f05544bed4039b36c9affdb62400f54d619dc7f827b0dd7aed5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe8439d75dd031f7f3a6908ae96e53d52128e10c30e23a158b9b8345d576f43`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 3.5 MB (3516254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dedafe9669d1a09c51f168c3d4db6477986ec7b7f4bb274347c5befbf1ab6e1`  
		Last Modified: Mon, 04 Aug 2025 20:50:20 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a8b0cb75e0335ca0c6f5b93ad9737facd671ebe28fba3a32ced09f40d7920b`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b409694fac1f06392e029aa1cce26b25863976e502862723282bece6849fd`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 13.7 MB (13653332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7d6aac432e4a310a74c720b92ddf62f125372b97cf40257ee5385d2159c3be`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abcffe2eb78cea70305ac08e1e90d0ac3e5de7b2671042ae50d8f9dcc2a38df`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 21.5 MB (21505197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4278be9860874f02951ab37abd3b1f199cca3b88299e7b54e4aec44ae9b6c97a`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dfdfedf576c6450fc46466c1f8e3b5b4d8c16aac720b69705113e7b87b3567`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482cd711b6eff6cb6033c515ddc86de794a4ca97eba0a2ff1d2555201ea9187a`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5c79f90b50a32f524d4b2da1607b5941987c9591da01842d7ba5cf1ef442d8`  
		Last Modified: Mon, 04 Aug 2025 20:59:20 GMT  
		Size: 34.4 MB (34436755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfe56d0f83c2b45a04e2d8dfa45f737a5f06068e755d1cf7cf36272df01db4c`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d734b8ae6fdeb107c2533e63ad5f1b473247698e5cca986f3fd8b026bbfbf28e`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffe9aaa7aa6de73af43a17a9193a13f43337de84804c51a167ad83538e69cb6`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324dd6780d35d4d930390f89bb2cc09b28ab0ab8376386c254781771b7a772e6`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:ded8c47f813c8d5533379e04bd78ffd97a169e4a33cbdaaf72f8741cf9ede86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e5c9ceef9330c05579c9fd204d1be12aaab0a29c0fd28347e7736fb826b31b`

```dockerfile
```

-	Layers:
	-	`sha256:3ce986804eb8aa74b49248f92ff30b01ca67114e40d34a1636beedc973d81d8b`  
		Last Modified: Mon, 04 Aug 2025 22:14:12 GMT  
		Size: 2.2 MB (2170585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:650629cff569d1105c7da001ff4f736f229bb18f0241208820506cb6226fc367`  
		Last Modified: Mon, 04 Aug 2025 22:14:13 GMT  
		Size: 31.6 KB (31619 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:57f049c8b47c5775859cbdfa374607111c7d418e22f12cf5bb7920f2063c2aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79128056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a6683e9c665154286e00e0dfea3d0ddaa6fc044afcd7caee6e437d2b39d56e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2149fd89f974e7ea3dea06f37d735922f1379a8f6a3848f9f27b655a231533a`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 13.7 MB (13653344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7733690cb25c9174f17fcd594fb9aa92de487681f9a30a88d38ce0fb49dfc9b7`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56aa0ea4063f0f606994769dabd9afcf81090a22a66567e6f1bbad01c84cef`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 21.9 MB (21877960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555ac5f064703fcb811adc2fc69166c7117941c125b03426671e1d4f55cc4f67`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa79fbfe4077bdecbc88d7a5d32f94313e38f9fcff1170cbba0b60e5f5454ae`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb096667c2eb8e8cc9f745a91245901b951632f05bd4a18c84e5fc700638654e`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1b83dffa45f0edf0a1799b639b0fe41010c6dc26daab3cc2ef4cc0b91d9b0b`  
		Last Modified: Tue, 05 Aug 2025 05:16:22 GMT  
		Size: 35.2 MB (35236910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e32f6aebd439ba8d413a2195d63d2c585e5e02c6dab1edf8a99373046e6e7f3`  
		Last Modified: Tue, 05 Aug 2025 05:16:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaac5d9ba510f90dc7373a9658a66baddb71aceb65465cb13540244ab0b77fc5`  
		Last Modified: Tue, 05 Aug 2025 05:16:18 GMT  
		Size: 977.2 KB (977236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0597ed65ad041e26db8cbc906e55caff1995219723badc8ba3d5ca7c506aca`  
		Last Modified: Tue, 05 Aug 2025 05:16:18 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50957638bb2745278398389025f8d8196d8e51f97b8a359bbe9137f1456beeb8`  
		Last Modified: Tue, 05 Aug 2025 05:16:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:2e96e1493048b9a2ce6ea1ab85b86253fe75966f7fac5c8779e014ddce68a5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017f81ae467c4a4fa2a12508b8f2aa84ea796f1714444da9befbf5d3a8357962`

```dockerfile
```

-	Layers:
	-	`sha256:41fb3e7bf64afe3d05635d6709a31f9a7c26e44042a90671009534606dd1bb67`  
		Last Modified: Tue, 05 Aug 2025 07:13:43 GMT  
		Size: 2.2 MB (2169365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a810c0f0f5c586b41fcc1ccf9e89e585a4869aa9d981b690543569a86675602`  
		Last Modified: Tue, 05 Aug 2025 07:13:44 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:980909ad037a24e51ba3429498490c3843de5323e00ecdf3df7735708c74dbf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73835415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27da9235b3a9747d939dbe21f6ef318657a6b3baca42b6c5664adda60a517bd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c69a28ac4d61cac15663b00afee7413a9a9efb61c173baf6d196a4a2b9eec`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 13.7 MB (13653334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e800d2c2d3dcabafd275ce5da9cd5b69a400c8d4e434fe0e169de8f847150c16`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc97540dd5b29ed35499d386792721453e9f2993fb6f31092fe292cb6cda3058`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 20.4 MB (20394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d682aa8b41ba1c48a1513a4764d3db005a8137af9425b4d401f86d8da3f88`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b4c9e4ab292bff4638f9d9c3c6bc2450aaf32e67ac31c00ae732b7f092d3c`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb9edc9e8c62872be6f09d92a7e349b9ecbbf22f3ca071428c2f79c001def07`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881222ef14b0d5e786e3466828f16530cdf02394d48ed40521acec353050c3e8`  
		Last Modified: Wed, 06 Aug 2025 09:08:34 GMT  
		Size: 31.1 MB (31108914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c5d76f8d2e998778c7ad2d7c0bbe518c050e6e366cdc8dcc6ea90cc70961`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087f1c391e30813fd4fa6ee493863cb0bbe2e4f360450d7ecabaff5de0139545`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 1.5 MB (1527045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f8488d1a46211627180c2fd827b894dab9a4f3b11ffd718270ccb440bf8f59`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1039958b2ef45d29d5ee5f8ed5e67b16fa0024ebdb8988d1f70d1327df8b992`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:f9ced1def07c8e1140a9f4e13ef6f9896310fbbd6ebc4b1b72b91321125c343f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb6869646674227adb986e14bcf7811d8c7fae642eb0b9b47944d54ea73d791`

```dockerfile
```

-	Layers:
	-	`sha256:688626909813c8c53a4d5643a92cc1ef76d6c723c65c626749f6cde3fefd2700`  
		Last Modified: Wed, 06 Aug 2025 10:13:48 GMT  
		Size: 2.2 MB (2167632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d53448c67f2dc151d63d9415a2f4979994344d99f768f96e615bf3d5af0790b6`  
		Last Modified: Wed, 06 Aug 2025 10:13:49 GMT  
		Size: 31.7 KB (31706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:3454652f5c01659d7d14d4484f06c37464ca11b213e78de7ce29ba077e89f36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75286560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5447e24db8ba6387cc17dcb0049fb80a50cbe97103813f4783213211fe95c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08eafa4a3224fe6eb688860741f0e8b65ac49b919952d4a7d1e5a4d195e134b`  
		Last Modified: Mon, 04 Aug 2025 22:58:42 GMT  
		Size: 13.7 MB (13653336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796e5c7e7fd28fa790bea89b2528028cbd5ba464a2cb410bd870445103de9197`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd0c014783d431392fbe4b78080b9c1485624e796271f5c4962f96941a32672`  
		Last Modified: Mon, 04 Aug 2025 22:58:56 GMT  
		Size: 21.5 MB (21451616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2a328a5b7b993670851ac5c6d63c129a67f13f999a03570b930367d089028`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5907607760dc2ba6786bf93d6c9d658346353233ad6c45f9d5bb678fb84e4ea`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18809b1760a6fe568eea4d22f4a08260e8eb4844a67a924b8f1ad360fcc505a0`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d55c6b75b483330745503675543c8c8cd53487c52f04fc538ffca072685af4`  
		Last Modified: Tue, 05 Aug 2025 03:05:15 GMT  
		Size: 31.8 MB (31838538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e906a6e05460592955352f726700115f5fd99ecac21d52a8a8f215008ac11b`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63184a90ffc761dc4e7021b2ac5bdd5b532c00e7ec5b3117482911a54a0da2e4`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 973.9 KB (973898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571c018a34b28319ba20267a7ce0ed4a6a55c45f0d9f82e9bfb0463a01ccbc8a`  
		Last Modified: Tue, 05 Aug 2025 03:05:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f5b12f8a659364b18b513be700392ed488b402212825aa2628511d39a1fdcb`  
		Last Modified: Tue, 05 Aug 2025 03:05:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:0cac2c1bd4b7516f02c4901581db87053d7f13d7162ed5893e2385e01d04ed06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf6d507c9d49db36eb5803a136cba47685933da214626fd6c9169c5b52519c4`

```dockerfile
```

-	Layers:
	-	`sha256:5a2334c87641f2bd18bc7ef2964f426cc33ffda0341112220f04384d1a624de9`  
		Last Modified: Tue, 05 Aug 2025 04:13:53 GMT  
		Size: 2.2 MB (2167414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8221622de3b92e6e87dc965f40bb6cdc356d9db5fa5fc13a4cf4d519f7d968`  
		Last Modified: Tue, 05 Aug 2025 04:13:54 GMT  
		Size: 31.7 KB (31655 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:e4d831dbf55eac67aaad352c8f3db7afdba209abcc44c4f09d38c4b1b40ced8a
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

### `composer:2.2` - linux; amd64

```console
$ docker pull composer@sha256:b9b09be7c876e9098aed04d44da8811dfc162997538d7cd8239aeae847d4f21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76679807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad8fb3a786abce13bfbbeff32b7f3696b22f8d606ec7a88bbb69843c3e8c4b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b8c404eae668716a1e38e4cfbfa17a24db95c67ac43f1c7fc370b54d3ca087`  
		Last Modified: Mon, 04 Aug 2025 20:49:49 GMT  
		Size: 3.5 MB (3460957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d882c5edba216e9f63d26119702e252a7f88372fa0af1077c58c6f937c29f`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769d794d159afc0f29bb41cae73fa8177791b4078920913550d6035fce888bf2`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3cf3bc6932e6344a1c898a1bdf35235fe0327d7cac86e56f4b07b23b9e9847`  
		Last Modified: Mon, 04 Aug 2025 20:49:51 GMT  
		Size: 13.7 MB (13653337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7066989316ffccd2c577fe6ce99e5bd4047a2f447f99f832d66a2f1cf334e8`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2176a4cebfd98252931aee5773d33b5a3a42d7e11f90f52e09364ad1fa8fd18`  
		Last Modified: Mon, 04 Aug 2025 20:49:52 GMT  
		Size: 21.0 MB (20975718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43e4b7ed65e42eff594acdcad113649b65b82ee4f86ccddb9c65ef1633a2fd7`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d54c809af2e0932d4bc53c9c0fa80cc499fba826b868e3ddc446d3361cb44`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 20.0 KB (19952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2151aa88e776b0b7a7bf7705e4dc7d63b02f2b67ebb32a829a34e18f38c3b1fc`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42521d242052834d1f612c414f05b2728c4e4c18872e568677b10cfba2af733b`  
		Last Modified: Mon, 04 Aug 2025 21:00:27 GMT  
		Size: 33.9 MB (33925210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5be58f8e3299b9ac7baaf5b9e55ae312272f81527f6c648a08da1ca0756147`  
		Last Modified: Mon, 04 Aug 2025 21:00:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb496c25eb1fb27b7d85b6bf3b5b4da0b3e3c12984e26b39be6585d425d4aec9`  
		Last Modified: Mon, 04 Aug 2025 21:00:22 GMT  
		Size: 820.1 KB (820132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177f86c7a2c755a187122477be9a8e72311e46087400330fee197c58bb8f973a`  
		Last Modified: Mon, 04 Aug 2025 21:00:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a070f6070f28edd2983c0dc4be26c930d5b4ecc5504b285e3d7f4bf6b0d3b`  
		Last Modified: Mon, 04 Aug 2025 21:00:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:de76bf0b5c4a1f41973617379914543333acc830508dcdc6cab4f0f2f4258949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2bed5c529d7bad4d943c7faf2b5f41e730071a94b1a20143d10b583e83634b`

```dockerfile
```

-	Layers:
	-	`sha256:2f7801e2c52b541fe2b3db455e87bf4e55b38ff87aa348b3fced1b3b9154b6d1`  
		Last Modified: Mon, 04 Aug 2025 22:13:52 GMT  
		Size: 2.2 MB (2170208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade918a62b64717016014f3142d864bc2cbdcc9701abcc514b11c0db32b123ee`  
		Last Modified: Mon, 04 Aug 2025 22:13:53 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:1c7c61d3286a8b516e8e7363d7b7a045f7d74ab60dce546c13554454ce2e20be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74323724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3de0505afa486ebdbca923503bae0f79d1d68b5a80d308c923166b84abe8966`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7494cac4578077d244b00bcd8c4b9cc24cbac12fe484fc52bdb253b7be68d33`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 13.7 MB (13653331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb9d8c4b4750c9afc1de1182d3a39f160769ecb594f5119173d9999fdc1b99`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08da3ca3515f68d5f047717865555b86a20702e1abbb868f91b827eac6e5ebf`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 19.1 MB (19094736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174f8de30188274046eddf1fa9fea9d286fe5b22b08972783323bdc3074e69f9`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890cfd4e2ff1fb6e00ae91a595e532b992ff926f2b1aabb5d5cf4550fc056385`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ba3c18d23646492096ded6ff9adf0df6739c2b4139249d0ae790e82cfb69ae`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab618c8fb396a56d07a5986ec1e2c89587a34750ca91962eb0f8fc69192e86`  
		Last Modified: Mon, 04 Aug 2025 23:52:25 GMT  
		Size: 33.8 MB (33788254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610e01a216465a5a644cfe45ea36450b82393adf820afdeb633ed5876549f9e`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6c47633ac970681879563ab0bca624ea05670e42eb5cfefdf1deb939a952ca`  
		Last Modified: Tue, 05 Aug 2025 00:01:14 GMT  
		Size: 820.2 KB (820161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6a6a96869dd541ba726ddc0b505e33a96f2c82c962b7f1ba5978eaa314c43`  
		Last Modified: Tue, 05 Aug 2025 00:01:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a31f24ad97614486ca6240ff471ceae4b0399a0ffaf50b9be6e9ff8d84268e5`  
		Last Modified: Tue, 05 Aug 2025 00:01:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:98629bb898366a9316aad9b51ccc80973bfe243ce22e69cfd39399aba62613bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5031a4975b711ccaa0c2ac02446f526c7a7fae666e5e14cba2019a60ffe0bf6e`

```dockerfile
```

-	Layers:
	-	`sha256:6b58c24a92aad3b7e43f85f1fd3846903736f3ac5df7ca8d5358142a91e1f54e`  
		Last Modified: Tue, 05 Aug 2025 01:13:42 GMT  
		Size: 30.9 KB (30923 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:8775f14bb2c815ee766dcfaf203f8ffb4e80eba912a4d4d2f9c19dda30644b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71107521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dff07971d14b105d35be1dab38eb8af8ce5613da6e10a33a3759c40bf197b9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca2e4db931023b2bd56443c80dbf78e53bf1efb748d1e76bf1242168c76cca6`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 13.7 MB (13653322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77469fa7f1256b86a0f5f641b66b80360641be9666ae4294dc5d6be17b7a5d8`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054413e584c9543fe5cdb41980742080a4ae1f7cae6744e77e0218deb7dac34d`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 18.1 MB (18070661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72860d23def789d218635f72e9644f4a04f18a8fa12c536da7af1ffa8743fa3c`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e66e44f6101fa11b28b93eec29aae52f52e35e47962ce16a425ce2822f9f64`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97417a1c0369df9443f468952dc56830ae71371b90f313f4b54c1c3b3f96390`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e233c39dcbf452f1d1e155cfa780907783f14f748767e9311ea6d9865ebc0896`  
		Last Modified: Tue, 05 Aug 2025 02:53:45 GMT  
		Size: 32.1 MB (32068670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45df4acb4b1365a6f7848309ec8384dbef2fded39db7a60a972ed210bacfc2e6`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665a593f8bbea206b07cf0d789da9292fc291f046db66acdcc60c415a32e88bb`  
		Last Modified: Tue, 05 Aug 2025 02:54:27 GMT  
		Size: 810.6 KB (810625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0c4a45dd74c477a7a268ad1530d60cfc7b7c80774640da8a8f646a0d0f9a42`  
		Last Modified: Tue, 05 Aug 2025 02:54:27 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff4758ac6745768cfc54a65813abf430c5b3effe313351af9f6d3d783522a2f`  
		Last Modified: Tue, 05 Aug 2025 02:54:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:724a9a5a8550a2ac70ee17e251dcc870f5fa99365e5fc1c1dae5375fa04da38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde286d1be7b9d4753cb1672690016fb6a312d70e97fb7d3669d190ebcb72cfb`

```dockerfile
```

-	Layers:
	-	`sha256:00a33e4b4307e72a6ce97793cac0053998b17a917357f4b288f27dada631a1c4`  
		Last Modified: Tue, 05 Aug 2025 04:13:54 GMT  
		Size: 2.2 MB (2170516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:230dc24c12e4947978d1acfbe1e8b3d4cfae5dadd3f3bcfb93a947c3dfae9206`  
		Last Modified: Tue, 05 Aug 2025 04:13:55 GMT  
		Size: 31.1 KB (31138 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:3c4f160ff7197d810f2607b14ce371900bcb3f6953e41b9ee52298f7c5808e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76626464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c166aed76dc8516ce310f9f7263dbb4295b52289ae2d7ba4c1d883ffba2ab5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb504dccc917de6b6b8bbc11ff4b9599d71f3ad971f142f67cc631aea843760`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 3.5 MB (3454743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7532649a0813cdb3165d225287dc7cbef8b4e47991127457849e1947e5549636`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253b9848099c2406835511872822d9dab1ea36834b393e1588c17a784e3bcb1`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973767f0cf0415e63013511841e37ace48afe3d8bbfaafa677dc100c89eb06ec`  
		Last Modified: Tue, 05 Aug 2025 01:42:19 GMT  
		Size: 13.7 MB (13653329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f37d53d2ef75f6d7f5ad4ee6e5eb97589d9dcf67380e28c57d85687f0a1c5c`  
		Last Modified: Tue, 05 Aug 2025 01:42:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3bef5a3676aa8a22d37f4aaaf0f903109f38d4050ea5bbf416baa0f2fdd4e9`  
		Last Modified: Tue, 05 Aug 2025 01:42:20 GMT  
		Size: 20.5 MB (20525567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfec7e98ad7662f3c4c51de1bf161799051d12f213dfd998753921e6a8cbe6d`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa68af9933e1df5a29b63199d57877c41b14c9f12615222a4ae65df1d2b9df`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 19.8 KB (19756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6fec7f9b2035416690d429232af55e7cafdbc99a57c3e473d5b44c4dc43fba`  
		Last Modified: Tue, 05 Aug 2025 01:42:18 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbf0d70d9d667639b695d04960c9fdafdd0aa711ae79b558e2e0959bf5b52f2`  
		Last Modified: Tue, 05 Aug 2025 08:15:54 GMT  
		Size: 34.0 MB (33997952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e41cdc44d3ea60f653b652041902b0f7ce6913b4b4f696e18302e88e07fae1`  
		Last Modified: Tue, 05 Aug 2025 08:15:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69041fc77b646ebd041aa131db64c7ef620778885df078421470efd11443b96e`  
		Last Modified: Tue, 05 Aug 2025 08:16:12 GMT  
		Size: 819.8 KB (819754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44003d492f6c37236ab8b6c7fe36bf2b2315663d300c882c01cd23ecb4b3fc41`  
		Last Modified: Tue, 05 Aug 2025 08:16:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1055e77a40eec0bdcf37449118e6fd349941f80eabd99a2eace84aa30e1a9624`  
		Last Modified: Tue, 05 Aug 2025 08:19:15 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:0574cdeff8c13bd8dc27540e12e375a2ed23c6f50af466c85bb620ffcafe1c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff43b188a76aeb91fd39f263074d4176bb6aa0ba9943fcf9828af05412802d98`

```dockerfile
```

-	Layers:
	-	`sha256:4fa6bd2fdd2921bbdd7a1536f04614c102006e92433191d9fb247915ce218c7d`  
		Last Modified: Tue, 05 Aug 2025 10:13:45 GMT  
		Size: 2.2 MB (2170336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a00361bfe1f892ed0a81ea1695c0a53afec4e7f2e6eaa36bc6767c815614545`  
		Last Modified: Tue, 05 Aug 2025 10:13:45 GMT  
		Size: 31.2 KB (31162 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:60c5ac09ee8c750da0dfdb0eff146cd8bf4c54556e8839569fcf6aeb97172a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77605363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34011d64fcf79da6600810a2d40db224a5e915e75992144dedcf07cace6ec8f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe8439d75dd031f7f3a6908ae96e53d52128e10c30e23a158b9b8345d576f43`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 3.5 MB (3516254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dedafe9669d1a09c51f168c3d4db6477986ec7b7f4bb274347c5befbf1ab6e1`  
		Last Modified: Mon, 04 Aug 2025 20:50:20 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a8b0cb75e0335ca0c6f5b93ad9737facd671ebe28fba3a32ced09f40d7920b`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b409694fac1f06392e029aa1cce26b25863976e502862723282bece6849fd`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 13.7 MB (13653332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7d6aac432e4a310a74c720b92ddf62f125372b97cf40257ee5385d2159c3be`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abcffe2eb78cea70305ac08e1e90d0ac3e5de7b2671042ae50d8f9dcc2a38df`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 21.5 MB (21505197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4278be9860874f02951ab37abd3b1f199cca3b88299e7b54e4aec44ae9b6c97a`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dfdfedf576c6450fc46466c1f8e3b5b4d8c16aac720b69705113e7b87b3567`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482cd711b6eff6cb6033c515ddc86de794a4ca97eba0a2ff1d2555201ea9187a`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd134b56d13a4f6807177b03eecdab652ebc25473384d205a8daf16dfda4bcf5`  
		Last Modified: Mon, 04 Aug 2025 20:59:26 GMT  
		Size: 34.4 MB (34436887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c68a1ce12c4e4bba939c6c29025a2f485902fad4b6d39c568de1b9b3162ff7`  
		Last Modified: Mon, 04 Aug 2025 20:59:19 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b522913865a1d331e8bfeea9e5b2137a3817d2acf7d1bbbc5e19d8a4d260173a`  
		Last Modified: Mon, 04 Aug 2025 20:59:20 GMT  
		Size: 834.0 KB (833963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fad9ce6662d1b81415054adf4a9d591ec7be56917a38ef0925edac2ed235865`  
		Last Modified: Mon, 04 Aug 2025 20:59:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef951fd9e1cfe14cfea90e97d9a0f18f146ce92deac5f81466d946df7fa1f7ae`  
		Last Modified: Mon, 04 Aug 2025 20:59:19 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:f58a8b9dadc5978513c1851ed5baf24e2822490cee41bc877f817d0cdb345714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2111db9e30c5c8414e55d63bfec47df9448247e98cbcad57159340fb076b854b`

```dockerfile
```

-	Layers:
	-	`sha256:a27d02cf13fe0b6f438f953ea2492849a73d1ba4706b49e9ffb1e4eb362a0acd`  
		Last Modified: Mon, 04 Aug 2025 22:14:07 GMT  
		Size: 2.2 MB (2170001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7b9a5a65c882a3b0c974c040fa230739aa45526f3f57ea79e34fbe97cac1ac`  
		Last Modified: Mon, 04 Aug 2025 22:14:08 GMT  
		Size: 31.0 KB (31026 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:83e8220907da8af905fc35d9e49bf9e0b1a93d4e74e87fc77f6ac09f0b8dd7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78977545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43eea3ec6230204d10b3f53e6f12e1fdf6d4be04743fb80f3503cb2c2f684093`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2149fd89f974e7ea3dea06f37d735922f1379a8f6a3848f9f27b655a231533a`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 13.7 MB (13653344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7733690cb25c9174f17fcd594fb9aa92de487681f9a30a88d38ce0fb49dfc9b7`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56aa0ea4063f0f606994769dabd9afcf81090a22a66567e6f1bbad01c84cef`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 21.9 MB (21877960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555ac5f064703fcb811adc2fc69166c7117941c125b03426671e1d4f55cc4f67`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa79fbfe4077bdecbc88d7a5d32f94313e38f9fcff1170cbba0b60e5f5454ae`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb096667c2eb8e8cc9f745a91245901b951632f05bd4a18c84e5fc700638654e`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1b83dffa45f0edf0a1799b639b0fe41010c6dc26daab3cc2ef4cc0b91d9b0b`  
		Last Modified: Tue, 05 Aug 2025 05:16:22 GMT  
		Size: 35.2 MB (35236910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e32f6aebd439ba8d413a2195d63d2c585e5e02c6dab1edf8a99373046e6e7f3`  
		Last Modified: Tue, 05 Aug 2025 05:16:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e00ed63bcccb55f3efefbaf89c4f412ffc8d9ab4f0f71df72a7e20a0d8e89f`  
		Last Modified: Tue, 05 Aug 2025 05:16:56 GMT  
		Size: 826.7 KB (826725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e084a43876485a7836892164af65fcf58daec99d16aee5e875b17c6699cc2240`  
		Last Modified: Tue, 05 Aug 2025 05:16:55 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842a5cbf4a762fc4d26cc44efb4e8ef154a366fd70919f4d00cff22acba9da6`  
		Last Modified: Tue, 05 Aug 2025 05:16:55 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:f497f2f6afdef96a45dd910d493c5393b1efce1db44cbf5f3860727a8aed26bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4f7ea4b46b7dc62395bdf42fadd1933af4387e97d3812efce4f2e89cb796eb`

```dockerfile
```

-	Layers:
	-	`sha256:252590f51df0bf3039991e968e670b99f904cd6d69296e06fa238a55edd6d3f7`  
		Last Modified: Tue, 05 Aug 2025 07:13:52 GMT  
		Size: 2.2 MB (2168759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207712cc1f1f898034931e5b151662e6b825d3e75ed192491872fcfd97611cbb`  
		Last Modified: Tue, 05 Aug 2025 07:13:53 GMT  
		Size: 31.1 KB (31088 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:5c47cd0ab78bf55e8c0699771ffa1bbfe6a415ae688ee4197087dc3c1c135212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73686439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d1b64be83426691fcb9ebe3f1c43ec0faf515ffc4fd0617784a404f1e0b3f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c69a28ac4d61cac15663b00afee7413a9a9efb61c173baf6d196a4a2b9eec`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 13.7 MB (13653334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e800d2c2d3dcabafd275ce5da9cd5b69a400c8d4e434fe0e169de8f847150c16`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc97540dd5b29ed35499d386792721453e9f2993fb6f31092fe292cb6cda3058`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 20.4 MB (20394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d682aa8b41ba1c48a1513a4764d3db005a8137af9425b4d401f86d8da3f88`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b4c9e4ab292bff4638f9d9c3c6bc2450aaf32e67ac31c00ae732b7f092d3c`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb9edc9e8c62872be6f09d92a7e349b9ecbbf22f3ca071428c2f79c001def07`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881222ef14b0d5e786e3466828f16530cdf02394d48ed40521acec353050c3e8`  
		Last Modified: Wed, 06 Aug 2025 09:08:34 GMT  
		Size: 31.1 MB (31108914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c5d76f8d2e998778c7ad2d7c0bbe518c050e6e366cdc8dcc6ea90cc70961`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f64d9925c37219ba496bb0f3a112f0ddd6743c27f243bbcb2064dcacd1e95`  
		Last Modified: Wed, 06 Aug 2025 09:13:41 GMT  
		Size: 1.4 MB (1378072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da33bfefe1d226db28ddd8db4f6499dfcd3044fcdcc81496c6f4f1d17c6fc1f3`  
		Last Modified: Wed, 06 Aug 2025 09:13:39 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b855a283fdae8d1252261d9e6e5428cfd53c375873ded19fa051d52c6863f5d0`  
		Last Modified: Wed, 06 Aug 2025 09:13:40 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:80df035d2a31cf26a4bcfc7cccea03c781b71cec534faf9059071d2c124731e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2198117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60d881f5fed614b6043187222b8cab2cb32bd33e4aa2008fa8809e4422cf856`

```dockerfile
```

-	Layers:
	-	`sha256:2ac86dfcd1990020fe3bc57dc7dfb287b6e442cea1b145c010941cd604adf0bd`  
		Last Modified: Wed, 06 Aug 2025 10:13:53 GMT  
		Size: 2.2 MB (2167026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b704549320424e5cc9064e6db90be4e757c3cda1000de5c296bf35eed006e4bf`  
		Last Modified: Wed, 06 Aug 2025 10:13:53 GMT  
		Size: 31.1 KB (31091 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:e319af6c99ace8ffcdf31cbcfad28925be5ed175726acbb14c634fd511eb31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75135820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22eeadcc2b1f5a3358fe33808193c7aa795d5bc40adb35847a2e531e1cc6ca0c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08eafa4a3224fe6eb688860741f0e8b65ac49b919952d4a7d1e5a4d195e134b`  
		Last Modified: Mon, 04 Aug 2025 22:58:42 GMT  
		Size: 13.7 MB (13653336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796e5c7e7fd28fa790bea89b2528028cbd5ba464a2cb410bd870445103de9197`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd0c014783d431392fbe4b78080b9c1485624e796271f5c4962f96941a32672`  
		Last Modified: Mon, 04 Aug 2025 22:58:56 GMT  
		Size: 21.5 MB (21451616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2a328a5b7b993670851ac5c6d63c129a67f13f999a03570b930367d089028`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5907607760dc2ba6786bf93d6c9d658346353233ad6c45f9d5bb678fb84e4ea`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18809b1760a6fe568eea4d22f4a08260e8eb4844a67a924b8f1ad360fcc505a0`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d55c6b75b483330745503675543c8c8cd53487c52f04fc538ffca072685af4`  
		Last Modified: Tue, 05 Aug 2025 03:05:15 GMT  
		Size: 31.8 MB (31838538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e906a6e05460592955352f726700115f5fd99ecac21d52a8a8f215008ac11b`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b49835da356bca9922f94f7872ccb8552a010fbc43c8667c952368c079adb`  
		Last Modified: Tue, 05 Aug 2025 03:06:14 GMT  
		Size: 823.2 KB (823158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46c8bef38db4d267aee037560265f54b981b23cc32e5904858281f2519750f9`  
		Last Modified: Tue, 05 Aug 2025 03:06:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfda908f9b5474ab8fb7498cc9bb8d9b1e8eca9f6b67153a89fdb28edd519d1`  
		Last Modified: Tue, 05 Aug 2025 03:06:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:3ab2a6d9a479a4bdba950876417efeefd7c69f51701461f3932f98744d2e5ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3718abf288a2413243aaa581f0c551229ed88b72854a72c79b5ee1680297a3a`

```dockerfile
```

-	Layers:
	-	`sha256:ce190a78464044b26a67ff0144c1e419b2c7db13674b7cde77c5b5aaba206b25`  
		Last Modified: Tue, 05 Aug 2025 04:14:11 GMT  
		Size: 2.2 MB (2166820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8472d6be33e2314c1105758de771a4200f91cfcec672f8354098887150c7b875`  
		Last Modified: Tue, 05 Aug 2025 04:14:11 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.25`

```console
$ docker pull composer@sha256:e4d831dbf55eac67aaad352c8f3db7afdba209abcc44c4f09d38c4b1b40ced8a
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

### `composer:2.2.25` - linux; amd64

```console
$ docker pull composer@sha256:b9b09be7c876e9098aed04d44da8811dfc162997538d7cd8239aeae847d4f21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76679807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad8fb3a786abce13bfbbeff32b7f3696b22f8d606ec7a88bbb69843c3e8c4b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b8c404eae668716a1e38e4cfbfa17a24db95c67ac43f1c7fc370b54d3ca087`  
		Last Modified: Mon, 04 Aug 2025 20:49:49 GMT  
		Size: 3.5 MB (3460957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d882c5edba216e9f63d26119702e252a7f88372fa0af1077c58c6f937c29f`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769d794d159afc0f29bb41cae73fa8177791b4078920913550d6035fce888bf2`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3cf3bc6932e6344a1c898a1bdf35235fe0327d7cac86e56f4b07b23b9e9847`  
		Last Modified: Mon, 04 Aug 2025 20:49:51 GMT  
		Size: 13.7 MB (13653337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7066989316ffccd2c577fe6ce99e5bd4047a2f447f99f832d66a2f1cf334e8`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2176a4cebfd98252931aee5773d33b5a3a42d7e11f90f52e09364ad1fa8fd18`  
		Last Modified: Mon, 04 Aug 2025 20:49:52 GMT  
		Size: 21.0 MB (20975718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43e4b7ed65e42eff594acdcad113649b65b82ee4f86ccddb9c65ef1633a2fd7`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d54c809af2e0932d4bc53c9c0fa80cc499fba826b868e3ddc446d3361cb44`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 20.0 KB (19952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2151aa88e776b0b7a7bf7705e4dc7d63b02f2b67ebb32a829a34e18f38c3b1fc`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42521d242052834d1f612c414f05b2728c4e4c18872e568677b10cfba2af733b`  
		Last Modified: Mon, 04 Aug 2025 21:00:27 GMT  
		Size: 33.9 MB (33925210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5be58f8e3299b9ac7baaf5b9e55ae312272f81527f6c648a08da1ca0756147`  
		Last Modified: Mon, 04 Aug 2025 21:00:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb496c25eb1fb27b7d85b6bf3b5b4da0b3e3c12984e26b39be6585d425d4aec9`  
		Last Modified: Mon, 04 Aug 2025 21:00:22 GMT  
		Size: 820.1 KB (820132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177f86c7a2c755a187122477be9a8e72311e46087400330fee197c58bb8f973a`  
		Last Modified: Mon, 04 Aug 2025 21:00:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f9a070f6070f28edd2983c0dc4be26c930d5b4ecc5504b285e3d7f4bf6b0d3b`  
		Last Modified: Mon, 04 Aug 2025 21:00:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:de76bf0b5c4a1f41973617379914543333acc830508dcdc6cab4f0f2f4258949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2bed5c529d7bad4d943c7faf2b5f41e730071a94b1a20143d10b583e83634b`

```dockerfile
```

-	Layers:
	-	`sha256:2f7801e2c52b541fe2b3db455e87bf4e55b38ff87aa348b3fced1b3b9154b6d1`  
		Last Modified: Mon, 04 Aug 2025 22:13:52 GMT  
		Size: 2.2 MB (2170208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade918a62b64717016014f3142d864bc2cbdcc9701abcc514b11c0db32b123ee`  
		Last Modified: Mon, 04 Aug 2025 22:13:53 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v6

```console
$ docker pull composer@sha256:1c7c61d3286a8b516e8e7363d7b7a045f7d74ab60dce546c13554454ce2e20be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74323724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3de0505afa486ebdbca923503bae0f79d1d68b5a80d308c923166b84abe8966`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7494cac4578077d244b00bcd8c4b9cc24cbac12fe484fc52bdb253b7be68d33`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 13.7 MB (13653331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb9d8c4b4750c9afc1de1182d3a39f160769ecb594f5119173d9999fdc1b99`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08da3ca3515f68d5f047717865555b86a20702e1abbb868f91b827eac6e5ebf`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 19.1 MB (19094736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174f8de30188274046eddf1fa9fea9d286fe5b22b08972783323bdc3074e69f9`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890cfd4e2ff1fb6e00ae91a595e532b992ff926f2b1aabb5d5cf4550fc056385`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ba3c18d23646492096ded6ff9adf0df6739c2b4139249d0ae790e82cfb69ae`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab618c8fb396a56d07a5986ec1e2c89587a34750ca91962eb0f8fc69192e86`  
		Last Modified: Mon, 04 Aug 2025 23:52:25 GMT  
		Size: 33.8 MB (33788254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610e01a216465a5a644cfe45ea36450b82393adf820afdeb633ed5876549f9e`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe6c47633ac970681879563ab0bca624ea05670e42eb5cfefdf1deb939a952ca`  
		Last Modified: Tue, 05 Aug 2025 00:01:14 GMT  
		Size: 820.2 KB (820161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e6a6a96869dd541ba726ddc0b505e33a96f2c82c962b7f1ba5978eaa314c43`  
		Last Modified: Tue, 05 Aug 2025 00:01:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a31f24ad97614486ca6240ff471ceae4b0399a0ffaf50b9be6e9ff8d84268e5`  
		Last Modified: Tue, 05 Aug 2025 00:01:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:98629bb898366a9316aad9b51ccc80973bfe243ce22e69cfd39399aba62613bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5031a4975b711ccaa0c2ac02446f526c7a7fae666e5e14cba2019a60ffe0bf6e`

```dockerfile
```

-	Layers:
	-	`sha256:6b58c24a92aad3b7e43f85f1fd3846903736f3ac5df7ca8d5358142a91e1f54e`  
		Last Modified: Tue, 05 Aug 2025 01:13:42 GMT  
		Size: 30.9 KB (30923 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v7

```console
$ docker pull composer@sha256:8775f14bb2c815ee766dcfaf203f8ffb4e80eba912a4d4d2f9c19dda30644b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71107521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dff07971d14b105d35be1dab38eb8af8ce5613da6e10a33a3759c40bf197b9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca2e4db931023b2bd56443c80dbf78e53bf1efb748d1e76bf1242168c76cca6`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 13.7 MB (13653322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77469fa7f1256b86a0f5f641b66b80360641be9666ae4294dc5d6be17b7a5d8`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054413e584c9543fe5cdb41980742080a4ae1f7cae6744e77e0218deb7dac34d`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 18.1 MB (18070661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72860d23def789d218635f72e9644f4a04f18a8fa12c536da7af1ffa8743fa3c`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e66e44f6101fa11b28b93eec29aae52f52e35e47962ce16a425ce2822f9f64`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97417a1c0369df9443f468952dc56830ae71371b90f313f4b54c1c3b3f96390`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e233c39dcbf452f1d1e155cfa780907783f14f748767e9311ea6d9865ebc0896`  
		Last Modified: Tue, 05 Aug 2025 02:53:45 GMT  
		Size: 32.1 MB (32068670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45df4acb4b1365a6f7848309ec8384dbef2fded39db7a60a972ed210bacfc2e6`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:665a593f8bbea206b07cf0d789da9292fc291f046db66acdcc60c415a32e88bb`  
		Last Modified: Tue, 05 Aug 2025 02:54:27 GMT  
		Size: 810.6 KB (810625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0c4a45dd74c477a7a268ad1530d60cfc7b7c80774640da8a8f646a0d0f9a42`  
		Last Modified: Tue, 05 Aug 2025 02:54:27 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff4758ac6745768cfc54a65813abf430c5b3effe313351af9f6d3d783522a2f`  
		Last Modified: Tue, 05 Aug 2025 02:54:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:724a9a5a8550a2ac70ee17e251dcc870f5fa99365e5fc1c1dae5375fa04da38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde286d1be7b9d4753cb1672690016fb6a312d70e97fb7d3669d190ebcb72cfb`

```dockerfile
```

-	Layers:
	-	`sha256:00a33e4b4307e72a6ce97793cac0053998b17a917357f4b288f27dada631a1c4`  
		Last Modified: Tue, 05 Aug 2025 04:13:54 GMT  
		Size: 2.2 MB (2170516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:230dc24c12e4947978d1acfbe1e8b3d4cfae5dadd3f3bcfb93a947c3dfae9206`  
		Last Modified: Tue, 05 Aug 2025 04:13:55 GMT  
		Size: 31.1 KB (31138 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:3c4f160ff7197d810f2607b14ce371900bcb3f6953e41b9ee52298f7c5808e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76626464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7c166aed76dc8516ce310f9f7263dbb4295b52289ae2d7ba4c1d883ffba2ab5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb504dccc917de6b6b8bbc11ff4b9599d71f3ad971f142f67cc631aea843760`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 3.5 MB (3454743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7532649a0813cdb3165d225287dc7cbef8b4e47991127457849e1947e5549636`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253b9848099c2406835511872822d9dab1ea36834b393e1588c17a784e3bcb1`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973767f0cf0415e63013511841e37ace48afe3d8bbfaafa677dc100c89eb06ec`  
		Last Modified: Tue, 05 Aug 2025 01:42:19 GMT  
		Size: 13.7 MB (13653329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f37d53d2ef75f6d7f5ad4ee6e5eb97589d9dcf67380e28c57d85687f0a1c5c`  
		Last Modified: Tue, 05 Aug 2025 01:42:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3bef5a3676aa8a22d37f4aaaf0f903109f38d4050ea5bbf416baa0f2fdd4e9`  
		Last Modified: Tue, 05 Aug 2025 01:42:20 GMT  
		Size: 20.5 MB (20525567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfec7e98ad7662f3c4c51de1bf161799051d12f213dfd998753921e6a8cbe6d`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa68af9933e1df5a29b63199d57877c41b14c9f12615222a4ae65df1d2b9df`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 19.8 KB (19756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6fec7f9b2035416690d429232af55e7cafdbc99a57c3e473d5b44c4dc43fba`  
		Last Modified: Tue, 05 Aug 2025 01:42:18 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbf0d70d9d667639b695d04960c9fdafdd0aa711ae79b558e2e0959bf5b52f2`  
		Last Modified: Tue, 05 Aug 2025 08:15:54 GMT  
		Size: 34.0 MB (33997952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e41cdc44d3ea60f653b652041902b0f7ce6913b4b4f696e18302e88e07fae1`  
		Last Modified: Tue, 05 Aug 2025 08:15:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69041fc77b646ebd041aa131db64c7ef620778885df078421470efd11443b96e`  
		Last Modified: Tue, 05 Aug 2025 08:16:12 GMT  
		Size: 819.8 KB (819754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44003d492f6c37236ab8b6c7fe36bf2b2315663d300c882c01cd23ecb4b3fc41`  
		Last Modified: Tue, 05 Aug 2025 08:16:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1055e77a40eec0bdcf37449118e6fd349941f80eabd99a2eace84aa30e1a9624`  
		Last Modified: Tue, 05 Aug 2025 08:19:15 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:0574cdeff8c13bd8dc27540e12e375a2ed23c6f50af466c85bb620ffcafe1c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff43b188a76aeb91fd39f263074d4176bb6aa0ba9943fcf9828af05412802d98`

```dockerfile
```

-	Layers:
	-	`sha256:4fa6bd2fdd2921bbdd7a1536f04614c102006e92433191d9fb247915ce218c7d`  
		Last Modified: Tue, 05 Aug 2025 10:13:45 GMT  
		Size: 2.2 MB (2170336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a00361bfe1f892ed0a81ea1695c0a53afec4e7f2e6eaa36bc6767c815614545`  
		Last Modified: Tue, 05 Aug 2025 10:13:45 GMT  
		Size: 31.2 KB (31162 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; 386

```console
$ docker pull composer@sha256:60c5ac09ee8c750da0dfdb0eff146cd8bf4c54556e8839569fcf6aeb97172a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.6 MB (77605363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34011d64fcf79da6600810a2d40db224a5e915e75992144dedcf07cace6ec8f4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe8439d75dd031f7f3a6908ae96e53d52128e10c30e23a158b9b8345d576f43`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 3.5 MB (3516254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dedafe9669d1a09c51f168c3d4db6477986ec7b7f4bb274347c5befbf1ab6e1`  
		Last Modified: Mon, 04 Aug 2025 20:50:20 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a8b0cb75e0335ca0c6f5b93ad9737facd671ebe28fba3a32ced09f40d7920b`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b409694fac1f06392e029aa1cce26b25863976e502862723282bece6849fd`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 13.7 MB (13653332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7d6aac432e4a310a74c720b92ddf62f125372b97cf40257ee5385d2159c3be`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abcffe2eb78cea70305ac08e1e90d0ac3e5de7b2671042ae50d8f9dcc2a38df`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 21.5 MB (21505197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4278be9860874f02951ab37abd3b1f199cca3b88299e7b54e4aec44ae9b6c97a`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dfdfedf576c6450fc46466c1f8e3b5b4d8c16aac720b69705113e7b87b3567`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482cd711b6eff6cb6033c515ddc86de794a4ca97eba0a2ff1d2555201ea9187a`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd134b56d13a4f6807177b03eecdab652ebc25473384d205a8daf16dfda4bcf5`  
		Last Modified: Mon, 04 Aug 2025 20:59:26 GMT  
		Size: 34.4 MB (34436887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c68a1ce12c4e4bba939c6c29025a2f485902fad4b6d39c568de1b9b3162ff7`  
		Last Modified: Mon, 04 Aug 2025 20:59:19 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b522913865a1d331e8bfeea9e5b2137a3817d2acf7d1bbbc5e19d8a4d260173a`  
		Last Modified: Mon, 04 Aug 2025 20:59:20 GMT  
		Size: 834.0 KB (833963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fad9ce6662d1b81415054adf4a9d591ec7be56917a38ef0925edac2ed235865`  
		Last Modified: Mon, 04 Aug 2025 20:59:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef951fd9e1cfe14cfea90e97d9a0f18f146ce92deac5f81466d946df7fa1f7ae`  
		Last Modified: Mon, 04 Aug 2025 20:59:19 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:f58a8b9dadc5978513c1851ed5baf24e2822490cee41bc877f817d0cdb345714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2111db9e30c5c8414e55d63bfec47df9448247e98cbcad57159340fb076b854b`

```dockerfile
```

-	Layers:
	-	`sha256:a27d02cf13fe0b6f438f953ea2492849a73d1ba4706b49e9ffb1e4eb362a0acd`  
		Last Modified: Mon, 04 Aug 2025 22:14:07 GMT  
		Size: 2.2 MB (2170001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb7b9a5a65c882a3b0c974c040fa230739aa45526f3f57ea79e34fbe97cac1ac`  
		Last Modified: Mon, 04 Aug 2025 22:14:08 GMT  
		Size: 31.0 KB (31026 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; ppc64le

```console
$ docker pull composer@sha256:83e8220907da8af905fc35d9e49bf9e0b1a93d4e74e87fc77f6ac09f0b8dd7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.0 MB (78977545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43eea3ec6230204d10b3f53e6f12e1fdf6d4be04743fb80f3503cb2c2f684093`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2149fd89f974e7ea3dea06f37d735922f1379a8f6a3848f9f27b655a231533a`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 13.7 MB (13653344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7733690cb25c9174f17fcd594fb9aa92de487681f9a30a88d38ce0fb49dfc9b7`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56aa0ea4063f0f606994769dabd9afcf81090a22a66567e6f1bbad01c84cef`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 21.9 MB (21877960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555ac5f064703fcb811adc2fc69166c7117941c125b03426671e1d4f55cc4f67`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa79fbfe4077bdecbc88d7a5d32f94313e38f9fcff1170cbba0b60e5f5454ae`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb096667c2eb8e8cc9f745a91245901b951632f05bd4a18c84e5fc700638654e`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1b83dffa45f0edf0a1799b639b0fe41010c6dc26daab3cc2ef4cc0b91d9b0b`  
		Last Modified: Tue, 05 Aug 2025 05:16:22 GMT  
		Size: 35.2 MB (35236910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e32f6aebd439ba8d413a2195d63d2c585e5e02c6dab1edf8a99373046e6e7f3`  
		Last Modified: Tue, 05 Aug 2025 05:16:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e00ed63bcccb55f3efefbaf89c4f412ffc8d9ab4f0f71df72a7e20a0d8e89f`  
		Last Modified: Tue, 05 Aug 2025 05:16:56 GMT  
		Size: 826.7 KB (826725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e084a43876485a7836892164af65fcf58daec99d16aee5e875b17c6699cc2240`  
		Last Modified: Tue, 05 Aug 2025 05:16:55 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3842a5cbf4a762fc4d26cc44efb4e8ef154a366fd70919f4d00cff22acba9da6`  
		Last Modified: Tue, 05 Aug 2025 05:16:55 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:f497f2f6afdef96a45dd910d493c5393b1efce1db44cbf5f3860727a8aed26bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4f7ea4b46b7dc62395bdf42fadd1933af4387e97d3812efce4f2e89cb796eb`

```dockerfile
```

-	Layers:
	-	`sha256:252590f51df0bf3039991e968e670b99f904cd6d69296e06fa238a55edd6d3f7`  
		Last Modified: Tue, 05 Aug 2025 07:13:52 GMT  
		Size: 2.2 MB (2168759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:207712cc1f1f898034931e5b151662e6b825d3e75ed192491872fcfd97611cbb`  
		Last Modified: Tue, 05 Aug 2025 07:13:53 GMT  
		Size: 31.1 KB (31088 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; riscv64

```console
$ docker pull composer@sha256:5c47cd0ab78bf55e8c0699771ffa1bbfe6a415ae688ee4197087dc3c1c135212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73686439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d1b64be83426691fcb9ebe3f1c43ec0faf515ffc4fd0617784a404f1e0b3f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c69a28ac4d61cac15663b00afee7413a9a9efb61c173baf6d196a4a2b9eec`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 13.7 MB (13653334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e800d2c2d3dcabafd275ce5da9cd5b69a400c8d4e434fe0e169de8f847150c16`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc97540dd5b29ed35499d386792721453e9f2993fb6f31092fe292cb6cda3058`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 20.4 MB (20394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d682aa8b41ba1c48a1513a4764d3db005a8137af9425b4d401f86d8da3f88`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b4c9e4ab292bff4638f9d9c3c6bc2450aaf32e67ac31c00ae732b7f092d3c`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb9edc9e8c62872be6f09d92a7e349b9ecbbf22f3ca071428c2f79c001def07`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881222ef14b0d5e786e3466828f16530cdf02394d48ed40521acec353050c3e8`  
		Last Modified: Wed, 06 Aug 2025 09:08:34 GMT  
		Size: 31.1 MB (31108914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c5d76f8d2e998778c7ad2d7c0bbe518c050e6e366cdc8dcc6ea90cc70961`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f64d9925c37219ba496bb0f3a112f0ddd6743c27f243bbcb2064dcacd1e95`  
		Last Modified: Wed, 06 Aug 2025 09:13:41 GMT  
		Size: 1.4 MB (1378072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da33bfefe1d226db28ddd8db4f6499dfcd3044fcdcc81496c6f4f1d17c6fc1f3`  
		Last Modified: Wed, 06 Aug 2025 09:13:39 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b855a283fdae8d1252261d9e6e5428cfd53c375873ded19fa051d52c6863f5d0`  
		Last Modified: Wed, 06 Aug 2025 09:13:40 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:80df035d2a31cf26a4bcfc7cccea03c781b71cec534faf9059071d2c124731e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2198117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60d881f5fed614b6043187222b8cab2cb32bd33e4aa2008fa8809e4422cf856`

```dockerfile
```

-	Layers:
	-	`sha256:2ac86dfcd1990020fe3bc57dc7dfb287b6e442cea1b145c010941cd604adf0bd`  
		Last Modified: Wed, 06 Aug 2025 10:13:53 GMT  
		Size: 2.2 MB (2167026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b704549320424e5cc9064e6db90be4e757c3cda1000de5c296bf35eed006e4bf`  
		Last Modified: Wed, 06 Aug 2025 10:13:53 GMT  
		Size: 31.1 KB (31091 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; s390x

```console
$ docker pull composer@sha256:e319af6c99ace8ffcdf31cbcfad28925be5ed175726acbb14c634fd511eb31c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75135820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22eeadcc2b1f5a3358fe33808193c7aa795d5bc40adb35847a2e531e1cc6ca0c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Mon, 19 May 2025 09:56:14 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Mon, 19 May 2025 09:56:14 GMT
CMD ["/bin/sh"]
# Mon, 19 May 2025 09:56:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 19 May 2025 09:56:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 19 May 2025 09:56:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_VERSION=8.4.11
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Mon, 19 May 2025 09:56:14 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["php" "-a"]
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 19 May 2025 09:56:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 19 May 2025 09:56:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Mon, 19 May 2025 09:56:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 19 May 2025 09:56:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 19 May 2025 09:56:14 GMT
WORKDIR /app
# Mon, 19 May 2025 09:56:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 19 May 2025 09:56:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08eafa4a3224fe6eb688860741f0e8b65ac49b919952d4a7d1e5a4d195e134b`  
		Last Modified: Mon, 04 Aug 2025 22:58:42 GMT  
		Size: 13.7 MB (13653336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796e5c7e7fd28fa790bea89b2528028cbd5ba464a2cb410bd870445103de9197`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd0c014783d431392fbe4b78080b9c1485624e796271f5c4962f96941a32672`  
		Last Modified: Mon, 04 Aug 2025 22:58:56 GMT  
		Size: 21.5 MB (21451616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2a328a5b7b993670851ac5c6d63c129a67f13f999a03570b930367d089028`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5907607760dc2ba6786bf93d6c9d658346353233ad6c45f9d5bb678fb84e4ea`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18809b1760a6fe568eea4d22f4a08260e8eb4844a67a924b8f1ad360fcc505a0`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d55c6b75b483330745503675543c8c8cd53487c52f04fc538ffca072685af4`  
		Last Modified: Tue, 05 Aug 2025 03:05:15 GMT  
		Size: 31.8 MB (31838538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e906a6e05460592955352f726700115f5fd99ecac21d52a8a8f215008ac11b`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9b49835da356bca9922f94f7872ccb8552a010fbc43c8667c952368c079adb`  
		Last Modified: Tue, 05 Aug 2025 03:06:14 GMT  
		Size: 823.2 KB (823158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46c8bef38db4d267aee037560265f54b981b23cc32e5904858281f2519750f9`  
		Last Modified: Tue, 05 Aug 2025 03:06:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abfda908f9b5474ab8fb7498cc9bb8d9b1e8eca9f6b67153a89fdb28edd519d1`  
		Last Modified: Tue, 05 Aug 2025 03:06:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:3ab2a6d9a479a4bdba950876417efeefd7c69f51701461f3932f98744d2e5ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2197872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3718abf288a2413243aaa581f0c551229ed88b72854a72c79b5ee1680297a3a`

```dockerfile
```

-	Layers:
	-	`sha256:ce190a78464044b26a67ff0144c1e419b2c7db13674b7cde77c5b5aaba206b25`  
		Last Modified: Tue, 05 Aug 2025 04:14:11 GMT  
		Size: 2.2 MB (2166820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8472d6be33e2314c1105758de771a4200f91cfcec672f8354098887150c7b875`  
		Last Modified: Tue, 05 Aug 2025 04:14:11 GMT  
		Size: 31.1 KB (31052 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:20462d70afcfa999ad75dbd9333194067f4d869078bdb37430339e8d97e541d6
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

### `composer:2.8` - linux; amd64

```console
$ docker pull composer@sha256:3945507689e27f577e4c251ce0a3f0d5d37b51c11d177874c2e485afd37cd747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76830755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe866d01c638502b5aabe801f86c9dac2b1934bb955d8f290079a12c23d3ecd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b8c404eae668716a1e38e4cfbfa17a24db95c67ac43f1c7fc370b54d3ca087`  
		Last Modified: Mon, 04 Aug 2025 20:49:49 GMT  
		Size: 3.5 MB (3460957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d882c5edba216e9f63d26119702e252a7f88372fa0af1077c58c6f937c29f`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769d794d159afc0f29bb41cae73fa8177791b4078920913550d6035fce888bf2`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3cf3bc6932e6344a1c898a1bdf35235fe0327d7cac86e56f4b07b23b9e9847`  
		Last Modified: Mon, 04 Aug 2025 20:49:51 GMT  
		Size: 13.7 MB (13653337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7066989316ffccd2c577fe6ce99e5bd4047a2f447f99f832d66a2f1cf334e8`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2176a4cebfd98252931aee5773d33b5a3a42d7e11f90f52e09364ad1fa8fd18`  
		Last Modified: Mon, 04 Aug 2025 20:49:52 GMT  
		Size: 21.0 MB (20975718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43e4b7ed65e42eff594acdcad113649b65b82ee4f86ccddb9c65ef1633a2fd7`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d54c809af2e0932d4bc53c9c0fa80cc499fba826b868e3ddc446d3361cb44`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 20.0 KB (19952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2151aa88e776b0b7a7bf7705e4dc7d63b02f2b67ebb32a829a34e18f38c3b1fc`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3d748b962dbf28c3f32f875009988343f709a6675518d6429dc81d248756a1`  
		Last Modified: Mon, 04 Aug 2025 21:00:24 GMT  
		Size: 33.9 MB (33925437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9807502fbc2a249159230ea6e961954135898e05417c88f8defbceb2fa9928f0`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993df12ef1b29b3ae5a8b6bb85419d981c1aef5d61e6725946675969265a84fc`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 970.9 KB (970855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69faa1b1fca1e579936e8775bf5d5dd6bd03432d2c68e19af29d19221bea2415`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d304213f65bda4383fcb1d13533167474be38480be6fdaf430ea96783d494d6d`  
		Last Modified: Mon, 04 Aug 2025 21:00:18 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:7d50db5b0c2bd627980ff70892d0d3534aca40e2a584a4f5796d6d473b80b38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0432d851d822729c57cdaf2c173cbc30284b27d82a0043e6403ab0ef45c0ce3`

```dockerfile
```

-	Layers:
	-	`sha256:25a8fafdd0ae54a46c9aee4ca880d093d50d7829b4ded946d64268ed54ed6951`  
		Last Modified: Mon, 04 Aug 2025 22:13:41 GMT  
		Size: 2.2 MB (2170802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96bb6a558b9c4d973e5da2679996a1a7ba39eb4c414be2cdc2c1c2b83911feda`  
		Last Modified: Mon, 04 Aug 2025 22:13:42 GMT  
		Size: 31.7 KB (31654 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:cbb23c77f4df826d1b8f662c82dc7f1f0c2c0979117ad5c64e1bddb11f00b223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74474554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b5565e8b37ed3e30397a672bd962362b10856219a859f824eaed5f52001e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7494cac4578077d244b00bcd8c4b9cc24cbac12fe484fc52bdb253b7be68d33`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 13.7 MB (13653331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb9d8c4b4750c9afc1de1182d3a39f160769ecb594f5119173d9999fdc1b99`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08da3ca3515f68d5f047717865555b86a20702e1abbb868f91b827eac6e5ebf`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 19.1 MB (19094736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174f8de30188274046eddf1fa9fea9d286fe5b22b08972783323bdc3074e69f9`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890cfd4e2ff1fb6e00ae91a595e532b992ff926f2b1aabb5d5cf4550fc056385`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ba3c18d23646492096ded6ff9adf0df6739c2b4139249d0ae790e82cfb69ae`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab618c8fb396a56d07a5986ec1e2c89587a34750ca91962eb0f8fc69192e86`  
		Last Modified: Mon, 04 Aug 2025 23:52:25 GMT  
		Size: 33.8 MB (33788254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610e01a216465a5a644cfe45ea36450b82393adf820afdeb633ed5876549f9e`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ddb27b58bc85c93cfde9f7f795e727cd01a16c674302be72668df5157c22e7`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 971.0 KB (970991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9086d6cd3389c76fe762d42484c1c888dfeca9c871cb3f8b7b7da3e5e9daed0`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6269c4496e0e22c66528769735b397a32967ed478a0da39ab00af135ae1df3a`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:90dc291226a369e83931948b794817bebe2433c995ccbbdcf54057cd27f5b426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88149dfdda7c8a00cae62b12c288d1042b9d89f9140149d7a3dd74850377f0d9`

```dockerfile
```

-	Layers:
	-	`sha256:65bffdc5d5e71983244c1d19c0e7f2e6f8fcc9d073adfb301077c45674a24633`  
		Last Modified: Tue, 05 Aug 2025 01:13:37 GMT  
		Size: 31.5 KB (31542 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:aea165e2b3f65f9cd6f7a6a2f459d0e0dd57f2dc1168d04dc7bb83815297f470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71258733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc0c514e4ccb94629affdfa6fee21cddaa9a606cde6d5d2b3d7e4f9c2b4e812`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca2e4db931023b2bd56443c80dbf78e53bf1efb748d1e76bf1242168c76cca6`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 13.7 MB (13653322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77469fa7f1256b86a0f5f641b66b80360641be9666ae4294dc5d6be17b7a5d8`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054413e584c9543fe5cdb41980742080a4ae1f7cae6744e77e0218deb7dac34d`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 18.1 MB (18070661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72860d23def789d218635f72e9644f4a04f18a8fa12c536da7af1ffa8743fa3c`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e66e44f6101fa11b28b93eec29aae52f52e35e47962ce16a425ce2822f9f64`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97417a1c0369df9443f468952dc56830ae71371b90f313f4b54c1c3b3f96390`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e233c39dcbf452f1d1e155cfa780907783f14f748767e9311ea6d9865ebc0896`  
		Last Modified: Tue, 05 Aug 2025 02:53:45 GMT  
		Size: 32.1 MB (32068670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45df4acb4b1365a6f7848309ec8384dbef2fded39db7a60a972ed210bacfc2e6`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0f69d706b0cdf49ed91cdd1a1b7e8b969bfe4e3f4cbdacf1230d7a8c536bdc`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 961.8 KB (961837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efde64a5f0035d069cf4f4b2accd54a50d652019c1f2fd0271eceb786e7eb2`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40bff23f29506a22b6724bac2dc8a9824c0aba32267c51a6ac473262c2e6bae`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:c66fb3ea6402a430587463e1bcb0db4d7ebd9212290726253c67df3202c7224e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f4719aff19ca7f9d0eeed9a5eaeeabc532e604eb714685416e18e2797859a9`

```dockerfile
```

-	Layers:
	-	`sha256:c81a4d85161e1d4108c2721183ecd4b588ec6687bca06a85bbdaf51efa44cc36`  
		Last Modified: Tue, 05 Aug 2025 04:14:02 GMT  
		Size: 2.2 MB (2171126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec15c40e803eaf944f6ded66014b9ba769454156b200f0ab3ba2d80341e1c57`  
		Last Modified: Tue, 05 Aug 2025 04:14:03 GMT  
		Size: 31.8 KB (31757 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:08e3389734d346ac8d451fb97c9b278802c73c61f44e439814cdcf0039591d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76777486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbf6534e1e10ffe687e5198e516a78745031e7d63674edace6898059193bcd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb504dccc917de6b6b8bbc11ff4b9599d71f3ad971f142f67cc631aea843760`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 3.5 MB (3454743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7532649a0813cdb3165d225287dc7cbef8b4e47991127457849e1947e5549636`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253b9848099c2406835511872822d9dab1ea36834b393e1588c17a784e3bcb1`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973767f0cf0415e63013511841e37ace48afe3d8bbfaafa677dc100c89eb06ec`  
		Last Modified: Tue, 05 Aug 2025 01:42:19 GMT  
		Size: 13.7 MB (13653329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f37d53d2ef75f6d7f5ad4ee6e5eb97589d9dcf67380e28c57d85687f0a1c5c`  
		Last Modified: Tue, 05 Aug 2025 01:42:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3bef5a3676aa8a22d37f4aaaf0f903109f38d4050ea5bbf416baa0f2fdd4e9`  
		Last Modified: Tue, 05 Aug 2025 01:42:20 GMT  
		Size: 20.5 MB (20525567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfec7e98ad7662f3c4c51de1bf161799051d12f213dfd998753921e6a8cbe6d`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa68af9933e1df5a29b63199d57877c41b14c9f12615222a4ae65df1d2b9df`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 19.8 KB (19756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6fec7f9b2035416690d429232af55e7cafdbc99a57c3e473d5b44c4dc43fba`  
		Last Modified: Tue, 05 Aug 2025 01:42:18 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbf0d70d9d667639b695d04960c9fdafdd0aa711ae79b558e2e0959bf5b52f2`  
		Last Modified: Tue, 05 Aug 2025 08:15:54 GMT  
		Size: 34.0 MB (33997952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e41cdc44d3ea60f653b652041902b0f7ce6913b4b4f696e18302e88e07fae1`  
		Last Modified: Tue, 05 Aug 2025 08:15:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4b9384b9b5dd9ae1d88abf18b42d3a970d84d8913e45e7170fca01c382969b`  
		Last Modified: Tue, 05 Aug 2025 08:15:47 GMT  
		Size: 970.8 KB (970776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3988bc851387ceef0287f5db25480cde4005099a5398d1b1f7cbe49541266834`  
		Last Modified: Tue, 05 Aug 2025 08:15:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e25bb8521481d37023fac2634fdb9f2d972ec7eef18621ea5371fab2e765b1`  
		Last Modified: Tue, 05 Aug 2025 08:15:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:606cae1475f184b8fcf6766e12409fea124e7f126567228b82f74399afea1e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8f91f519d7e4b57e099ebad266b11088f4f8502fe8a9ac82f3744999b5bd16`

```dockerfile
```

-	Layers:
	-	`sha256:8038ff9053185ee45b8d45db485c4408a335878007ac7e71bd5cab69d842dc63`  
		Last Modified: Tue, 05 Aug 2025 10:13:39 GMT  
		Size: 2.2 MB (2170954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d992d60b19bf5a9ddfc63fad4ebe9905a796a336ff427fc16c5709cc28c8b11`  
		Last Modified: Tue, 05 Aug 2025 10:13:40 GMT  
		Size: 31.8 KB (31788 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:d6bc37d9ee867506c3d4365376c7966b3cdece0db1043174f396a2f227975e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77755088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b73057212af6f05544bed4039b36c9affdb62400f54d619dc7f827b0dd7aed5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe8439d75dd031f7f3a6908ae96e53d52128e10c30e23a158b9b8345d576f43`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 3.5 MB (3516254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dedafe9669d1a09c51f168c3d4db6477986ec7b7f4bb274347c5befbf1ab6e1`  
		Last Modified: Mon, 04 Aug 2025 20:50:20 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a8b0cb75e0335ca0c6f5b93ad9737facd671ebe28fba3a32ced09f40d7920b`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b409694fac1f06392e029aa1cce26b25863976e502862723282bece6849fd`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 13.7 MB (13653332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7d6aac432e4a310a74c720b92ddf62f125372b97cf40257ee5385d2159c3be`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abcffe2eb78cea70305ac08e1e90d0ac3e5de7b2671042ae50d8f9dcc2a38df`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 21.5 MB (21505197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4278be9860874f02951ab37abd3b1f199cca3b88299e7b54e4aec44ae9b6c97a`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dfdfedf576c6450fc46466c1f8e3b5b4d8c16aac720b69705113e7b87b3567`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482cd711b6eff6cb6033c515ddc86de794a4ca97eba0a2ff1d2555201ea9187a`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5c79f90b50a32f524d4b2da1607b5941987c9591da01842d7ba5cf1ef442d8`  
		Last Modified: Mon, 04 Aug 2025 20:59:20 GMT  
		Size: 34.4 MB (34436755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfe56d0f83c2b45a04e2d8dfa45f737a5f06068e755d1cf7cf36272df01db4c`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d734b8ae6fdeb107c2533e63ad5f1b473247698e5cca986f3fd8b026bbfbf28e`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffe9aaa7aa6de73af43a17a9193a13f43337de84804c51a167ad83538e69cb6`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324dd6780d35d4d930390f89bb2cc09b28ab0ab8376386c254781771b7a772e6`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:ded8c47f813c8d5533379e04bd78ffd97a169e4a33cbdaaf72f8741cf9ede86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e5c9ceef9330c05579c9fd204d1be12aaab0a29c0fd28347e7736fb826b31b`

```dockerfile
```

-	Layers:
	-	`sha256:3ce986804eb8aa74b49248f92ff30b01ca67114e40d34a1636beedc973d81d8b`  
		Last Modified: Mon, 04 Aug 2025 22:14:12 GMT  
		Size: 2.2 MB (2170585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:650629cff569d1105c7da001ff4f736f229bb18f0241208820506cb6226fc367`  
		Last Modified: Mon, 04 Aug 2025 22:14:13 GMT  
		Size: 31.6 KB (31619 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:57f049c8b47c5775859cbdfa374607111c7d418e22f12cf5bb7920f2063c2aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79128056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a6683e9c665154286e00e0dfea3d0ddaa6fc044afcd7caee6e437d2b39d56e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2149fd89f974e7ea3dea06f37d735922f1379a8f6a3848f9f27b655a231533a`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 13.7 MB (13653344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7733690cb25c9174f17fcd594fb9aa92de487681f9a30a88d38ce0fb49dfc9b7`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56aa0ea4063f0f606994769dabd9afcf81090a22a66567e6f1bbad01c84cef`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 21.9 MB (21877960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555ac5f064703fcb811adc2fc69166c7117941c125b03426671e1d4f55cc4f67`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa79fbfe4077bdecbc88d7a5d32f94313e38f9fcff1170cbba0b60e5f5454ae`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb096667c2eb8e8cc9f745a91245901b951632f05bd4a18c84e5fc700638654e`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1b83dffa45f0edf0a1799b639b0fe41010c6dc26daab3cc2ef4cc0b91d9b0b`  
		Last Modified: Tue, 05 Aug 2025 05:16:22 GMT  
		Size: 35.2 MB (35236910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e32f6aebd439ba8d413a2195d63d2c585e5e02c6dab1edf8a99373046e6e7f3`  
		Last Modified: Tue, 05 Aug 2025 05:16:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaac5d9ba510f90dc7373a9658a66baddb71aceb65465cb13540244ab0b77fc5`  
		Last Modified: Tue, 05 Aug 2025 05:16:18 GMT  
		Size: 977.2 KB (977236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0597ed65ad041e26db8cbc906e55caff1995219723badc8ba3d5ca7c506aca`  
		Last Modified: Tue, 05 Aug 2025 05:16:18 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50957638bb2745278398389025f8d8196d8e51f97b8a359bbe9137f1456beeb8`  
		Last Modified: Tue, 05 Aug 2025 05:16:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:2e96e1493048b9a2ce6ea1ab85b86253fe75966f7fac5c8779e014ddce68a5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017f81ae467c4a4fa2a12508b8f2aa84ea796f1714444da9befbf5d3a8357962`

```dockerfile
```

-	Layers:
	-	`sha256:41fb3e7bf64afe3d05635d6709a31f9a7c26e44042a90671009534606dd1bb67`  
		Last Modified: Tue, 05 Aug 2025 07:13:43 GMT  
		Size: 2.2 MB (2169365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a810c0f0f5c586b41fcc1ccf9e89e585a4869aa9d981b690543569a86675602`  
		Last Modified: Tue, 05 Aug 2025 07:13:44 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:980909ad037a24e51ba3429498490c3843de5323e00ecdf3df7735708c74dbf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73835415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27da9235b3a9747d939dbe21f6ef318657a6b3baca42b6c5664adda60a517bd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c69a28ac4d61cac15663b00afee7413a9a9efb61c173baf6d196a4a2b9eec`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 13.7 MB (13653334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e800d2c2d3dcabafd275ce5da9cd5b69a400c8d4e434fe0e169de8f847150c16`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc97540dd5b29ed35499d386792721453e9f2993fb6f31092fe292cb6cda3058`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 20.4 MB (20394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d682aa8b41ba1c48a1513a4764d3db005a8137af9425b4d401f86d8da3f88`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b4c9e4ab292bff4638f9d9c3c6bc2450aaf32e67ac31c00ae732b7f092d3c`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb9edc9e8c62872be6f09d92a7e349b9ecbbf22f3ca071428c2f79c001def07`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881222ef14b0d5e786e3466828f16530cdf02394d48ed40521acec353050c3e8`  
		Last Modified: Wed, 06 Aug 2025 09:08:34 GMT  
		Size: 31.1 MB (31108914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c5d76f8d2e998778c7ad2d7c0bbe518c050e6e366cdc8dcc6ea90cc70961`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087f1c391e30813fd4fa6ee493863cb0bbe2e4f360450d7ecabaff5de0139545`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 1.5 MB (1527045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f8488d1a46211627180c2fd827b894dab9a4f3b11ffd718270ccb440bf8f59`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1039958b2ef45d29d5ee5f8ed5e67b16fa0024ebdb8988d1f70d1327df8b992`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:f9ced1def07c8e1140a9f4e13ef6f9896310fbbd6ebc4b1b72b91321125c343f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb6869646674227adb986e14bcf7811d8c7fae642eb0b9b47944d54ea73d791`

```dockerfile
```

-	Layers:
	-	`sha256:688626909813c8c53a4d5643a92cc1ef76d6c723c65c626749f6cde3fefd2700`  
		Last Modified: Wed, 06 Aug 2025 10:13:48 GMT  
		Size: 2.2 MB (2167632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d53448c67f2dc151d63d9415a2f4979994344d99f768f96e615bf3d5af0790b6`  
		Last Modified: Wed, 06 Aug 2025 10:13:49 GMT  
		Size: 31.7 KB (31706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:3454652f5c01659d7d14d4484f06c37464ca11b213e78de7ce29ba077e89f36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75286560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5447e24db8ba6387cc17dcb0049fb80a50cbe97103813f4783213211fe95c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08eafa4a3224fe6eb688860741f0e8b65ac49b919952d4a7d1e5a4d195e134b`  
		Last Modified: Mon, 04 Aug 2025 22:58:42 GMT  
		Size: 13.7 MB (13653336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796e5c7e7fd28fa790bea89b2528028cbd5ba464a2cb410bd870445103de9197`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd0c014783d431392fbe4b78080b9c1485624e796271f5c4962f96941a32672`  
		Last Modified: Mon, 04 Aug 2025 22:58:56 GMT  
		Size: 21.5 MB (21451616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2a328a5b7b993670851ac5c6d63c129a67f13f999a03570b930367d089028`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5907607760dc2ba6786bf93d6c9d658346353233ad6c45f9d5bb678fb84e4ea`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18809b1760a6fe568eea4d22f4a08260e8eb4844a67a924b8f1ad360fcc505a0`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d55c6b75b483330745503675543c8c8cd53487c52f04fc538ffca072685af4`  
		Last Modified: Tue, 05 Aug 2025 03:05:15 GMT  
		Size: 31.8 MB (31838538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e906a6e05460592955352f726700115f5fd99ecac21d52a8a8f215008ac11b`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63184a90ffc761dc4e7021b2ac5bdd5b532c00e7ec5b3117482911a54a0da2e4`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 973.9 KB (973898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571c018a34b28319ba20267a7ce0ed4a6a55c45f0d9f82e9bfb0463a01ccbc8a`  
		Last Modified: Tue, 05 Aug 2025 03:05:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f5b12f8a659364b18b513be700392ed488b402212825aa2628511d39a1fdcb`  
		Last Modified: Tue, 05 Aug 2025 03:05:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:0cac2c1bd4b7516f02c4901581db87053d7f13d7162ed5893e2385e01d04ed06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf6d507c9d49db36eb5803a136cba47685933da214626fd6c9169c5b52519c4`

```dockerfile
```

-	Layers:
	-	`sha256:5a2334c87641f2bd18bc7ef2964f426cc33ffda0341112220f04384d1a624de9`  
		Last Modified: Tue, 05 Aug 2025 04:13:53 GMT  
		Size: 2.2 MB (2167414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8221622de3b92e6e87dc965f40bb6cdc356d9db5fa5fc13a4cf4d519f7d968`  
		Last Modified: Tue, 05 Aug 2025 04:13:54 GMT  
		Size: 31.7 KB (31655 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.10`

```console
$ docker pull composer@sha256:20462d70afcfa999ad75dbd9333194067f4d869078bdb37430339e8d97e541d6
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

### `composer:2.8.10` - linux; amd64

```console
$ docker pull composer@sha256:3945507689e27f577e4c251ce0a3f0d5d37b51c11d177874c2e485afd37cd747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76830755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe866d01c638502b5aabe801f86c9dac2b1934bb955d8f290079a12c23d3ecd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b8c404eae668716a1e38e4cfbfa17a24db95c67ac43f1c7fc370b54d3ca087`  
		Last Modified: Mon, 04 Aug 2025 20:49:49 GMT  
		Size: 3.5 MB (3460957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d882c5edba216e9f63d26119702e252a7f88372fa0af1077c58c6f937c29f`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769d794d159afc0f29bb41cae73fa8177791b4078920913550d6035fce888bf2`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3cf3bc6932e6344a1c898a1bdf35235fe0327d7cac86e56f4b07b23b9e9847`  
		Last Modified: Mon, 04 Aug 2025 20:49:51 GMT  
		Size: 13.7 MB (13653337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7066989316ffccd2c577fe6ce99e5bd4047a2f447f99f832d66a2f1cf334e8`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2176a4cebfd98252931aee5773d33b5a3a42d7e11f90f52e09364ad1fa8fd18`  
		Last Modified: Mon, 04 Aug 2025 20:49:52 GMT  
		Size: 21.0 MB (20975718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43e4b7ed65e42eff594acdcad113649b65b82ee4f86ccddb9c65ef1633a2fd7`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d54c809af2e0932d4bc53c9c0fa80cc499fba826b868e3ddc446d3361cb44`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 20.0 KB (19952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2151aa88e776b0b7a7bf7705e4dc7d63b02f2b67ebb32a829a34e18f38c3b1fc`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3d748b962dbf28c3f32f875009988343f709a6675518d6429dc81d248756a1`  
		Last Modified: Mon, 04 Aug 2025 21:00:24 GMT  
		Size: 33.9 MB (33925437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9807502fbc2a249159230ea6e961954135898e05417c88f8defbceb2fa9928f0`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993df12ef1b29b3ae5a8b6bb85419d981c1aef5d61e6725946675969265a84fc`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 970.9 KB (970855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69faa1b1fca1e579936e8775bf5d5dd6bd03432d2c68e19af29d19221bea2415`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d304213f65bda4383fcb1d13533167474be38480be6fdaf430ea96783d494d6d`  
		Last Modified: Mon, 04 Aug 2025 21:00:18 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.10` - unknown; unknown

```console
$ docker pull composer@sha256:7d50db5b0c2bd627980ff70892d0d3534aca40e2a584a4f5796d6d473b80b38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0432d851d822729c57cdaf2c173cbc30284b27d82a0043e6403ab0ef45c0ce3`

```dockerfile
```

-	Layers:
	-	`sha256:25a8fafdd0ae54a46c9aee4ca880d093d50d7829b4ded946d64268ed54ed6951`  
		Last Modified: Mon, 04 Aug 2025 22:13:41 GMT  
		Size: 2.2 MB (2170802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96bb6a558b9c4d973e5da2679996a1a7ba39eb4c414be2cdc2c1c2b83911feda`  
		Last Modified: Mon, 04 Aug 2025 22:13:42 GMT  
		Size: 31.7 KB (31654 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:cbb23c77f4df826d1b8f662c82dc7f1f0c2c0979117ad5c64e1bddb11f00b223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74474554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b5565e8b37ed3e30397a672bd962362b10856219a859f824eaed5f52001e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7494cac4578077d244b00bcd8c4b9cc24cbac12fe484fc52bdb253b7be68d33`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 13.7 MB (13653331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb9d8c4b4750c9afc1de1182d3a39f160769ecb594f5119173d9999fdc1b99`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08da3ca3515f68d5f047717865555b86a20702e1abbb868f91b827eac6e5ebf`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 19.1 MB (19094736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174f8de30188274046eddf1fa9fea9d286fe5b22b08972783323bdc3074e69f9`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890cfd4e2ff1fb6e00ae91a595e532b992ff926f2b1aabb5d5cf4550fc056385`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ba3c18d23646492096ded6ff9adf0df6739c2b4139249d0ae790e82cfb69ae`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab618c8fb396a56d07a5986ec1e2c89587a34750ca91962eb0f8fc69192e86`  
		Last Modified: Mon, 04 Aug 2025 23:52:25 GMT  
		Size: 33.8 MB (33788254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610e01a216465a5a644cfe45ea36450b82393adf820afdeb633ed5876549f9e`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ddb27b58bc85c93cfde9f7f795e727cd01a16c674302be72668df5157c22e7`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 971.0 KB (970991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9086d6cd3389c76fe762d42484c1c888dfeca9c871cb3f8b7b7da3e5e9daed0`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6269c4496e0e22c66528769735b397a32967ed478a0da39ab00af135ae1df3a`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.10` - unknown; unknown

```console
$ docker pull composer@sha256:90dc291226a369e83931948b794817bebe2433c995ccbbdcf54057cd27f5b426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88149dfdda7c8a00cae62b12c288d1042b9d89f9140149d7a3dd74850377f0d9`

```dockerfile
```

-	Layers:
	-	`sha256:65bffdc5d5e71983244c1d19c0e7f2e6f8fcc9d073adfb301077c45674a24633`  
		Last Modified: Tue, 05 Aug 2025 01:13:37 GMT  
		Size: 31.5 KB (31542 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:aea165e2b3f65f9cd6f7a6a2f459d0e0dd57f2dc1168d04dc7bb83815297f470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71258733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc0c514e4ccb94629affdfa6fee21cddaa9a606cde6d5d2b3d7e4f9c2b4e812`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca2e4db931023b2bd56443c80dbf78e53bf1efb748d1e76bf1242168c76cca6`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 13.7 MB (13653322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77469fa7f1256b86a0f5f641b66b80360641be9666ae4294dc5d6be17b7a5d8`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054413e584c9543fe5cdb41980742080a4ae1f7cae6744e77e0218deb7dac34d`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 18.1 MB (18070661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72860d23def789d218635f72e9644f4a04f18a8fa12c536da7af1ffa8743fa3c`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e66e44f6101fa11b28b93eec29aae52f52e35e47962ce16a425ce2822f9f64`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97417a1c0369df9443f468952dc56830ae71371b90f313f4b54c1c3b3f96390`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e233c39dcbf452f1d1e155cfa780907783f14f748767e9311ea6d9865ebc0896`  
		Last Modified: Tue, 05 Aug 2025 02:53:45 GMT  
		Size: 32.1 MB (32068670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45df4acb4b1365a6f7848309ec8384dbef2fded39db7a60a972ed210bacfc2e6`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0f69d706b0cdf49ed91cdd1a1b7e8b969bfe4e3f4cbdacf1230d7a8c536bdc`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 961.8 KB (961837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efde64a5f0035d069cf4f4b2accd54a50d652019c1f2fd0271eceb786e7eb2`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40bff23f29506a22b6724bac2dc8a9824c0aba32267c51a6ac473262c2e6bae`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.10` - unknown; unknown

```console
$ docker pull composer@sha256:c66fb3ea6402a430587463e1bcb0db4d7ebd9212290726253c67df3202c7224e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f4719aff19ca7f9d0eeed9a5eaeeabc532e604eb714685416e18e2797859a9`

```dockerfile
```

-	Layers:
	-	`sha256:c81a4d85161e1d4108c2721183ecd4b588ec6687bca06a85bbdaf51efa44cc36`  
		Last Modified: Tue, 05 Aug 2025 04:14:02 GMT  
		Size: 2.2 MB (2171126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec15c40e803eaf944f6ded66014b9ba769454156b200f0ab3ba2d80341e1c57`  
		Last Modified: Tue, 05 Aug 2025 04:14:03 GMT  
		Size: 31.8 KB (31757 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:08e3389734d346ac8d451fb97c9b278802c73c61f44e439814cdcf0039591d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76777486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbf6534e1e10ffe687e5198e516a78745031e7d63674edace6898059193bcd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb504dccc917de6b6b8bbc11ff4b9599d71f3ad971f142f67cc631aea843760`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 3.5 MB (3454743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7532649a0813cdb3165d225287dc7cbef8b4e47991127457849e1947e5549636`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253b9848099c2406835511872822d9dab1ea36834b393e1588c17a784e3bcb1`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973767f0cf0415e63013511841e37ace48afe3d8bbfaafa677dc100c89eb06ec`  
		Last Modified: Tue, 05 Aug 2025 01:42:19 GMT  
		Size: 13.7 MB (13653329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f37d53d2ef75f6d7f5ad4ee6e5eb97589d9dcf67380e28c57d85687f0a1c5c`  
		Last Modified: Tue, 05 Aug 2025 01:42:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3bef5a3676aa8a22d37f4aaaf0f903109f38d4050ea5bbf416baa0f2fdd4e9`  
		Last Modified: Tue, 05 Aug 2025 01:42:20 GMT  
		Size: 20.5 MB (20525567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfec7e98ad7662f3c4c51de1bf161799051d12f213dfd998753921e6a8cbe6d`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa68af9933e1df5a29b63199d57877c41b14c9f12615222a4ae65df1d2b9df`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 19.8 KB (19756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6fec7f9b2035416690d429232af55e7cafdbc99a57c3e473d5b44c4dc43fba`  
		Last Modified: Tue, 05 Aug 2025 01:42:18 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbf0d70d9d667639b695d04960c9fdafdd0aa711ae79b558e2e0959bf5b52f2`  
		Last Modified: Tue, 05 Aug 2025 08:15:54 GMT  
		Size: 34.0 MB (33997952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e41cdc44d3ea60f653b652041902b0f7ce6913b4b4f696e18302e88e07fae1`  
		Last Modified: Tue, 05 Aug 2025 08:15:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4b9384b9b5dd9ae1d88abf18b42d3a970d84d8913e45e7170fca01c382969b`  
		Last Modified: Tue, 05 Aug 2025 08:15:47 GMT  
		Size: 970.8 KB (970776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3988bc851387ceef0287f5db25480cde4005099a5398d1b1f7cbe49541266834`  
		Last Modified: Tue, 05 Aug 2025 08:15:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e25bb8521481d37023fac2634fdb9f2d972ec7eef18621ea5371fab2e765b1`  
		Last Modified: Tue, 05 Aug 2025 08:15:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.10` - unknown; unknown

```console
$ docker pull composer@sha256:606cae1475f184b8fcf6766e12409fea124e7f126567228b82f74399afea1e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8f91f519d7e4b57e099ebad266b11088f4f8502fe8a9ac82f3744999b5bd16`

```dockerfile
```

-	Layers:
	-	`sha256:8038ff9053185ee45b8d45db485c4408a335878007ac7e71bd5cab69d842dc63`  
		Last Modified: Tue, 05 Aug 2025 10:13:39 GMT  
		Size: 2.2 MB (2170954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d992d60b19bf5a9ddfc63fad4ebe9905a796a336ff427fc16c5709cc28c8b11`  
		Last Modified: Tue, 05 Aug 2025 10:13:40 GMT  
		Size: 31.8 KB (31788 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.10` - linux; 386

```console
$ docker pull composer@sha256:d6bc37d9ee867506c3d4365376c7966b3cdece0db1043174f396a2f227975e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77755088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b73057212af6f05544bed4039b36c9affdb62400f54d619dc7f827b0dd7aed5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe8439d75dd031f7f3a6908ae96e53d52128e10c30e23a158b9b8345d576f43`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 3.5 MB (3516254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dedafe9669d1a09c51f168c3d4db6477986ec7b7f4bb274347c5befbf1ab6e1`  
		Last Modified: Mon, 04 Aug 2025 20:50:20 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a8b0cb75e0335ca0c6f5b93ad9737facd671ebe28fba3a32ced09f40d7920b`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b409694fac1f06392e029aa1cce26b25863976e502862723282bece6849fd`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 13.7 MB (13653332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7d6aac432e4a310a74c720b92ddf62f125372b97cf40257ee5385d2159c3be`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abcffe2eb78cea70305ac08e1e90d0ac3e5de7b2671042ae50d8f9dcc2a38df`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 21.5 MB (21505197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4278be9860874f02951ab37abd3b1f199cca3b88299e7b54e4aec44ae9b6c97a`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dfdfedf576c6450fc46466c1f8e3b5b4d8c16aac720b69705113e7b87b3567`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482cd711b6eff6cb6033c515ddc86de794a4ca97eba0a2ff1d2555201ea9187a`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5c79f90b50a32f524d4b2da1607b5941987c9591da01842d7ba5cf1ef442d8`  
		Last Modified: Mon, 04 Aug 2025 20:59:20 GMT  
		Size: 34.4 MB (34436755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfe56d0f83c2b45a04e2d8dfa45f737a5f06068e755d1cf7cf36272df01db4c`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d734b8ae6fdeb107c2533e63ad5f1b473247698e5cca986f3fd8b026bbfbf28e`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffe9aaa7aa6de73af43a17a9193a13f43337de84804c51a167ad83538e69cb6`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324dd6780d35d4d930390f89bb2cc09b28ab0ab8376386c254781771b7a772e6`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.10` - unknown; unknown

```console
$ docker pull composer@sha256:ded8c47f813c8d5533379e04bd78ffd97a169e4a33cbdaaf72f8741cf9ede86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e5c9ceef9330c05579c9fd204d1be12aaab0a29c0fd28347e7736fb826b31b`

```dockerfile
```

-	Layers:
	-	`sha256:3ce986804eb8aa74b49248f92ff30b01ca67114e40d34a1636beedc973d81d8b`  
		Last Modified: Mon, 04 Aug 2025 22:14:12 GMT  
		Size: 2.2 MB (2170585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:650629cff569d1105c7da001ff4f736f229bb18f0241208820506cb6226fc367`  
		Last Modified: Mon, 04 Aug 2025 22:14:13 GMT  
		Size: 31.6 KB (31619 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.10` - linux; ppc64le

```console
$ docker pull composer@sha256:57f049c8b47c5775859cbdfa374607111c7d418e22f12cf5bb7920f2063c2aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79128056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a6683e9c665154286e00e0dfea3d0ddaa6fc044afcd7caee6e437d2b39d56e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2149fd89f974e7ea3dea06f37d735922f1379a8f6a3848f9f27b655a231533a`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 13.7 MB (13653344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7733690cb25c9174f17fcd594fb9aa92de487681f9a30a88d38ce0fb49dfc9b7`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56aa0ea4063f0f606994769dabd9afcf81090a22a66567e6f1bbad01c84cef`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 21.9 MB (21877960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555ac5f064703fcb811adc2fc69166c7117941c125b03426671e1d4f55cc4f67`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa79fbfe4077bdecbc88d7a5d32f94313e38f9fcff1170cbba0b60e5f5454ae`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb096667c2eb8e8cc9f745a91245901b951632f05bd4a18c84e5fc700638654e`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1b83dffa45f0edf0a1799b639b0fe41010c6dc26daab3cc2ef4cc0b91d9b0b`  
		Last Modified: Tue, 05 Aug 2025 05:16:22 GMT  
		Size: 35.2 MB (35236910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e32f6aebd439ba8d413a2195d63d2c585e5e02c6dab1edf8a99373046e6e7f3`  
		Last Modified: Tue, 05 Aug 2025 05:16:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaac5d9ba510f90dc7373a9658a66baddb71aceb65465cb13540244ab0b77fc5`  
		Last Modified: Tue, 05 Aug 2025 05:16:18 GMT  
		Size: 977.2 KB (977236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0597ed65ad041e26db8cbc906e55caff1995219723badc8ba3d5ca7c506aca`  
		Last Modified: Tue, 05 Aug 2025 05:16:18 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50957638bb2745278398389025f8d8196d8e51f97b8a359bbe9137f1456beeb8`  
		Last Modified: Tue, 05 Aug 2025 05:16:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.10` - unknown; unknown

```console
$ docker pull composer@sha256:2e96e1493048b9a2ce6ea1ab85b86253fe75966f7fac5c8779e014ddce68a5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017f81ae467c4a4fa2a12508b8f2aa84ea796f1714444da9befbf5d3a8357962`

```dockerfile
```

-	Layers:
	-	`sha256:41fb3e7bf64afe3d05635d6709a31f9a7c26e44042a90671009534606dd1bb67`  
		Last Modified: Tue, 05 Aug 2025 07:13:43 GMT  
		Size: 2.2 MB (2169365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a810c0f0f5c586b41fcc1ccf9e89e585a4869aa9d981b690543569a86675602`  
		Last Modified: Tue, 05 Aug 2025 07:13:44 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.10` - linux; riscv64

```console
$ docker pull composer@sha256:980909ad037a24e51ba3429498490c3843de5323e00ecdf3df7735708c74dbf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73835415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27da9235b3a9747d939dbe21f6ef318657a6b3baca42b6c5664adda60a517bd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c69a28ac4d61cac15663b00afee7413a9a9efb61c173baf6d196a4a2b9eec`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 13.7 MB (13653334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e800d2c2d3dcabafd275ce5da9cd5b69a400c8d4e434fe0e169de8f847150c16`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc97540dd5b29ed35499d386792721453e9f2993fb6f31092fe292cb6cda3058`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 20.4 MB (20394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d682aa8b41ba1c48a1513a4764d3db005a8137af9425b4d401f86d8da3f88`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b4c9e4ab292bff4638f9d9c3c6bc2450aaf32e67ac31c00ae732b7f092d3c`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb9edc9e8c62872be6f09d92a7e349b9ecbbf22f3ca071428c2f79c001def07`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881222ef14b0d5e786e3466828f16530cdf02394d48ed40521acec353050c3e8`  
		Last Modified: Wed, 06 Aug 2025 09:08:34 GMT  
		Size: 31.1 MB (31108914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c5d76f8d2e998778c7ad2d7c0bbe518c050e6e366cdc8dcc6ea90cc70961`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087f1c391e30813fd4fa6ee493863cb0bbe2e4f360450d7ecabaff5de0139545`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 1.5 MB (1527045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f8488d1a46211627180c2fd827b894dab9a4f3b11ffd718270ccb440bf8f59`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1039958b2ef45d29d5ee5f8ed5e67b16fa0024ebdb8988d1f70d1327df8b992`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.10` - unknown; unknown

```console
$ docker pull composer@sha256:f9ced1def07c8e1140a9f4e13ef6f9896310fbbd6ebc4b1b72b91321125c343f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb6869646674227adb986e14bcf7811d8c7fae642eb0b9b47944d54ea73d791`

```dockerfile
```

-	Layers:
	-	`sha256:688626909813c8c53a4d5643a92cc1ef76d6c723c65c626749f6cde3fefd2700`  
		Last Modified: Wed, 06 Aug 2025 10:13:48 GMT  
		Size: 2.2 MB (2167632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d53448c67f2dc151d63d9415a2f4979994344d99f768f96e615bf3d5af0790b6`  
		Last Modified: Wed, 06 Aug 2025 10:13:49 GMT  
		Size: 31.7 KB (31706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.10` - linux; s390x

```console
$ docker pull composer@sha256:3454652f5c01659d7d14d4484f06c37464ca11b213e78de7ce29ba077e89f36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75286560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5447e24db8ba6387cc17dcb0049fb80a50cbe97103813f4783213211fe95c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08eafa4a3224fe6eb688860741f0e8b65ac49b919952d4a7d1e5a4d195e134b`  
		Last Modified: Mon, 04 Aug 2025 22:58:42 GMT  
		Size: 13.7 MB (13653336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796e5c7e7fd28fa790bea89b2528028cbd5ba464a2cb410bd870445103de9197`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd0c014783d431392fbe4b78080b9c1485624e796271f5c4962f96941a32672`  
		Last Modified: Mon, 04 Aug 2025 22:58:56 GMT  
		Size: 21.5 MB (21451616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2a328a5b7b993670851ac5c6d63c129a67f13f999a03570b930367d089028`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5907607760dc2ba6786bf93d6c9d658346353233ad6c45f9d5bb678fb84e4ea`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18809b1760a6fe568eea4d22f4a08260e8eb4844a67a924b8f1ad360fcc505a0`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d55c6b75b483330745503675543c8c8cd53487c52f04fc538ffca072685af4`  
		Last Modified: Tue, 05 Aug 2025 03:05:15 GMT  
		Size: 31.8 MB (31838538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e906a6e05460592955352f726700115f5fd99ecac21d52a8a8f215008ac11b`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63184a90ffc761dc4e7021b2ac5bdd5b532c00e7ec5b3117482911a54a0da2e4`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 973.9 KB (973898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571c018a34b28319ba20267a7ce0ed4a6a55c45f0d9f82e9bfb0463a01ccbc8a`  
		Last Modified: Tue, 05 Aug 2025 03:05:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f5b12f8a659364b18b513be700392ed488b402212825aa2628511d39a1fdcb`  
		Last Modified: Tue, 05 Aug 2025 03:05:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.10` - unknown; unknown

```console
$ docker pull composer@sha256:0cac2c1bd4b7516f02c4901581db87053d7f13d7162ed5893e2385e01d04ed06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf6d507c9d49db36eb5803a136cba47685933da214626fd6c9169c5b52519c4`

```dockerfile
```

-	Layers:
	-	`sha256:5a2334c87641f2bd18bc7ef2964f426cc33ffda0341112220f04384d1a624de9`  
		Last Modified: Tue, 05 Aug 2025 04:13:53 GMT  
		Size: 2.2 MB (2167414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8221622de3b92e6e87dc965f40bb6cdc356d9db5fa5fc13a4cf4d519f7d968`  
		Last Modified: Tue, 05 Aug 2025 04:13:54 GMT  
		Size: 31.7 KB (31655 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:20462d70afcfa999ad75dbd9333194067f4d869078bdb37430339e8d97e541d6
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

### `composer:latest` - linux; amd64

```console
$ docker pull composer@sha256:3945507689e27f577e4c251ce0a3f0d5d37b51c11d177874c2e485afd37cd747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76830755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe866d01c638502b5aabe801f86c9dac2b1934bb955d8f290079a12c23d3ecd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b8c404eae668716a1e38e4cfbfa17a24db95c67ac43f1c7fc370b54d3ca087`  
		Last Modified: Mon, 04 Aug 2025 20:49:49 GMT  
		Size: 3.5 MB (3460957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0d882c5edba216e9f63d26119702e252a7f88372fa0af1077c58c6f937c29f`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:769d794d159afc0f29bb41cae73fa8177791b4078920913550d6035fce888bf2`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3cf3bc6932e6344a1c898a1bdf35235fe0327d7cac86e56f4b07b23b9e9847`  
		Last Modified: Mon, 04 Aug 2025 20:49:51 GMT  
		Size: 13.7 MB (13653337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7066989316ffccd2c577fe6ce99e5bd4047a2f447f99f832d66a2f1cf334e8`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2176a4cebfd98252931aee5773d33b5a3a42d7e11f90f52e09364ad1fa8fd18`  
		Last Modified: Mon, 04 Aug 2025 20:49:52 GMT  
		Size: 21.0 MB (20975718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43e4b7ed65e42eff594acdcad113649b65b82ee4f86ccddb9c65ef1633a2fd7`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1d54c809af2e0932d4bc53c9c0fa80cc499fba826b868e3ddc446d3361cb44`  
		Last Modified: Mon, 04 Aug 2025 20:49:47 GMT  
		Size: 20.0 KB (19952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2151aa88e776b0b7a7bf7705e4dc7d63b02f2b67ebb32a829a34e18f38c3b1fc`  
		Last Modified: Mon, 04 Aug 2025 20:49:48 GMT  
		Size: 20.0 KB (19954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3d748b962dbf28c3f32f875009988343f709a6675518d6429dc81d248756a1`  
		Last Modified: Mon, 04 Aug 2025 21:00:24 GMT  
		Size: 33.9 MB (33925437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9807502fbc2a249159230ea6e961954135898e05417c88f8defbceb2fa9928f0`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:993df12ef1b29b3ae5a8b6bb85419d981c1aef5d61e6725946675969265a84fc`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 970.9 KB (970855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69faa1b1fca1e579936e8775bf5d5dd6bd03432d2c68e19af29d19221bea2415`  
		Last Modified: Mon, 04 Aug 2025 21:00:17 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d304213f65bda4383fcb1d13533167474be38480be6fdaf430ea96783d494d6d`  
		Last Modified: Mon, 04 Aug 2025 21:00:18 GMT  
		Size: 91.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:7d50db5b0c2bd627980ff70892d0d3534aca40e2a584a4f5796d6d473b80b38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0432d851d822729c57cdaf2c173cbc30284b27d82a0043e6403ab0ef45c0ce3`

```dockerfile
```

-	Layers:
	-	`sha256:25a8fafdd0ae54a46c9aee4ca880d093d50d7829b4ded946d64268ed54ed6951`  
		Last Modified: Mon, 04 Aug 2025 22:13:41 GMT  
		Size: 2.2 MB (2170802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96bb6a558b9c4d973e5da2679996a1a7ba39eb4c414be2cdc2c1c2b83911feda`  
		Last Modified: Mon, 04 Aug 2025 22:13:42 GMT  
		Size: 31.7 KB (31654 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:cbb23c77f4df826d1b8f662c82dc7f1f0c2c0979117ad5c64e1bddb11f00b223
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74474554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:412b5565e8b37ed3e30397a672bd962362b10856219a859f824eaed5f52001e7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d22834b475ece2203538fb14057fd70a6b00476b61f6902242434b53353f4d0`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 3.4 MB (3422001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f63604d1779bd23de30ef4abf3b540a7b132c0448407347f39a4861ebe61b1`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0566a827016b139c8586e6ca71c129f5fbbe4fc6e3cae54b699905df197b2a33`  
		Last Modified: Tue, 15 Jul 2025 20:02:10 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7494cac4578077d244b00bcd8c4b9cc24cbac12fe484fc52bdb253b7be68d33`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 13.7 MB (13653331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fb9d8c4b4750c9afc1de1182d3a39f160769ecb594f5119173d9999fdc1b99`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08da3ca3515f68d5f047717865555b86a20702e1abbb868f91b827eac6e5ebf`  
		Last Modified: Mon, 04 Aug 2025 21:27:11 GMT  
		Size: 19.1 MB (19094736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174f8de30188274046eddf1fa9fea9d286fe5b22b08972783323bdc3074e69f9`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890cfd4e2ff1fb6e00ae91a595e532b992ff926f2b1aabb5d5cf4550fc056385`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17ba3c18d23646492096ded6ff9adf0df6739c2b4139249d0ae790e82cfb69ae`  
		Last Modified: Mon, 04 Aug 2025 21:27:10 GMT  
		Size: 19.7 KB (19729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aab618c8fb396a56d07a5986ec1e2c89587a34750ca91962eb0f8fc69192e86`  
		Last Modified: Mon, 04 Aug 2025 23:52:25 GMT  
		Size: 33.8 MB (33788254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f610e01a216465a5a644cfe45ea36450b82393adf820afdeb633ed5876549f9e`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ddb27b58bc85c93cfde9f7f795e727cd01a16c674302be72668df5157c22e7`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 971.0 KB (970991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9086d6cd3389c76fe762d42484c1c888dfeca9c871cb3f8b7b7da3e5e9daed0`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6269c4496e0e22c66528769735b397a32967ed478a0da39ab00af135ae1df3a`  
		Last Modified: Mon, 04 Aug 2025 23:52:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:90dc291226a369e83931948b794817bebe2433c995ccbbdcf54057cd27f5b426
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 KB (31542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88149dfdda7c8a00cae62b12c288d1042b9d89f9140149d7a3dd74850377f0d9`

```dockerfile
```

-	Layers:
	-	`sha256:65bffdc5d5e71983244c1d19c0e7f2e6f8fcc9d073adfb301077c45674a24633`  
		Last Modified: Tue, 05 Aug 2025 01:13:37 GMT  
		Size: 31.5 KB (31542 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:aea165e2b3f65f9cd6f7a6a2f459d0e0dd57f2dc1168d04dc7bb83815297f470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71258733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc0c514e4ccb94629affdfa6fee21cddaa9a606cde6d5d2b3d7e4f9c2b4e812`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdac87f9414bf366e318e5481a7ff1ed73cd811cd08fe0b8520657cf9b1a85f5`  
		Last Modified: Tue, 15 Jul 2025 19:40:41 GMT  
		Size: 3.2 MB (3240894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9762a4da160644bcaa3d665d94969930997f9214ad191083373940ee5240dc1`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ebef0b263131dc81229136e7114545e060fdf60de8166dced2089dd8f8c4fd`  
		Last Modified: Tue, 15 Jul 2025 19:40:40 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca2e4db931023b2bd56443c80dbf78e53bf1efb748d1e76bf1242168c76cca6`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 13.7 MB (13653322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77469fa7f1256b86a0f5f641b66b80360641be9666ae4294dc5d6be17b7a5d8`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054413e584c9543fe5cdb41980742080a4ae1f7cae6744e77e0218deb7dac34d`  
		Last Modified: Mon, 04 Aug 2025 23:07:55 GMT  
		Size: 18.1 MB (18070661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72860d23def789d218635f72e9644f4a04f18a8fa12c536da7af1ffa8743fa3c`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e66e44f6101fa11b28b93eec29aae52f52e35e47962ce16a425ce2822f9f64`  
		Last Modified: Mon, 04 Aug 2025 23:07:52 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97417a1c0369df9443f468952dc56830ae71371b90f313f4b54c1c3b3f96390`  
		Last Modified: Mon, 04 Aug 2025 23:07:51 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e233c39dcbf452f1d1e155cfa780907783f14f748767e9311ea6d9865ebc0896`  
		Last Modified: Tue, 05 Aug 2025 02:53:45 GMT  
		Size: 32.1 MB (32068670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45df4acb4b1365a6f7848309ec8384dbef2fded39db7a60a972ed210bacfc2e6`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0f69d706b0cdf49ed91cdd1a1b7e8b969bfe4e3f4cbdacf1230d7a8c536bdc`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 961.8 KB (961837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97efde64a5f0035d069cf4f4b2accd54a50d652019c1f2fd0271eceb786e7eb2`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40bff23f29506a22b6724bac2dc8a9824c0aba32267c51a6ac473262c2e6bae`  
		Last Modified: Tue, 05 Aug 2025 02:53:42 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:c66fb3ea6402a430587463e1bcb0db4d7ebd9212290726253c67df3202c7224e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8f4719aff19ca7f9d0eeed9a5eaeeabc532e604eb714685416e18e2797859a9`

```dockerfile
```

-	Layers:
	-	`sha256:c81a4d85161e1d4108c2721183ecd4b588ec6687bca06a85bbdaf51efa44cc36`  
		Last Modified: Tue, 05 Aug 2025 04:14:02 GMT  
		Size: 2.2 MB (2171126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ec15c40e803eaf944f6ded66014b9ba769454156b200f0ab3ba2d80341e1c57`  
		Last Modified: Tue, 05 Aug 2025 04:14:03 GMT  
		Size: 31.8 KB (31757 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:08e3389734d346ac8d451fb97c9b278802c73c61f44e439814cdcf0039591d63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76777486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccbf6534e1e10ffe687e5198e516a78745031e7d63674edace6898059193bcd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb504dccc917de6b6b8bbc11ff4b9599d71f3ad971f142f67cc631aea843760`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 3.5 MB (3454743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7532649a0813cdb3165d225287dc7cbef8b4e47991127457849e1947e5549636`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e253b9848099c2406835511872822d9dab1ea36834b393e1588c17a784e3bcb1`  
		Last Modified: Tue, 05 Aug 2025 00:49:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:973767f0cf0415e63013511841e37ace48afe3d8bbfaafa677dc100c89eb06ec`  
		Last Modified: Tue, 05 Aug 2025 01:42:19 GMT  
		Size: 13.7 MB (13653329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f37d53d2ef75f6d7f5ad4ee6e5eb97589d9dcf67380e28c57d85687f0a1c5c`  
		Last Modified: Tue, 05 Aug 2025 01:42:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c3bef5a3676aa8a22d37f4aaaf0f903109f38d4050ea5bbf416baa0f2fdd4e9`  
		Last Modified: Tue, 05 Aug 2025 01:42:20 GMT  
		Size: 20.5 MB (20525567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfec7e98ad7662f3c4c51de1bf161799051d12f213dfd998753921e6a8cbe6d`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa68af9933e1df5a29b63199d57877c41b14c9f12615222a4ae65df1d2b9df`  
		Last Modified: Tue, 05 Aug 2025 01:42:17 GMT  
		Size: 19.8 KB (19756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6fec7f9b2035416690d429232af55e7cafdbc99a57c3e473d5b44c4dc43fba`  
		Last Modified: Tue, 05 Aug 2025 01:42:18 GMT  
		Size: 19.8 KB (19751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdbf0d70d9d667639b695d04960c9fdafdd0aa711ae79b558e2e0959bf5b52f2`  
		Last Modified: Tue, 05 Aug 2025 08:15:54 GMT  
		Size: 34.0 MB (33997952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e41cdc44d3ea60f653b652041902b0f7ce6913b4b4f696e18302e88e07fae1`  
		Last Modified: Tue, 05 Aug 2025 08:15:45 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a4b9384b9b5dd9ae1d88abf18b42d3a970d84d8913e45e7170fca01c382969b`  
		Last Modified: Tue, 05 Aug 2025 08:15:47 GMT  
		Size: 970.8 KB (970776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3988bc851387ceef0287f5db25480cde4005099a5398d1b1f7cbe49541266834`  
		Last Modified: Tue, 05 Aug 2025 08:15:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e25bb8521481d37023fac2634fdb9f2d972ec7eef18621ea5371fab2e765b1`  
		Last Modified: Tue, 05 Aug 2025 08:15:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:606cae1475f184b8fcf6766e12409fea124e7f126567228b82f74399afea1e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8f91f519d7e4b57e099ebad266b11088f4f8502fe8a9ac82f3744999b5bd16`

```dockerfile
```

-	Layers:
	-	`sha256:8038ff9053185ee45b8d45db485c4408a335878007ac7e71bd5cab69d842dc63`  
		Last Modified: Tue, 05 Aug 2025 10:13:39 GMT  
		Size: 2.2 MB (2170954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d992d60b19bf5a9ddfc63fad4ebe9905a796a336ff427fc16c5709cc28c8b11`  
		Last Modified: Tue, 05 Aug 2025 10:13:40 GMT  
		Size: 31.8 KB (31788 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:d6bc37d9ee867506c3d4365376c7966b3cdece0db1043174f396a2f227975e2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77755088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b73057212af6f05544bed4039b36c9affdb62400f54d619dc7f827b0dd7aed5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe8439d75dd031f7f3a6908ae96e53d52128e10c30e23a158b9b8345d576f43`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 3.5 MB (3516254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dedafe9669d1a09c51f168c3d4db6477986ec7b7f4bb274347c5befbf1ab6e1`  
		Last Modified: Mon, 04 Aug 2025 20:50:20 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a8b0cb75e0335ca0c6f5b93ad9737facd671ebe28fba3a32ced09f40d7920b`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b409694fac1f06392e029aa1cce26b25863976e502862723282bece6849fd`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 13.7 MB (13653332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7d6aac432e4a310a74c720b92ddf62f125372b97cf40257ee5385d2159c3be`  
		Last Modified: Mon, 04 Aug 2025 20:50:34 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abcffe2eb78cea70305ac08e1e90d0ac3e5de7b2671042ae50d8f9dcc2a38df`  
		Last Modified: Mon, 04 Aug 2025 20:50:38 GMT  
		Size: 21.5 MB (21505197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4278be9860874f02951ab37abd3b1f199cca3b88299e7b54e4aec44ae9b6c97a`  
		Last Modified: Mon, 04 Aug 2025 20:50:35 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dfdfedf576c6450fc46466c1f8e3b5b4d8c16aac720b69705113e7b87b3567`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482cd711b6eff6cb6033c515ddc86de794a4ca97eba0a2ff1d2555201ea9187a`  
		Last Modified: Mon, 04 Aug 2025 20:50:36 GMT  
		Size: 19.9 KB (19928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5c79f90b50a32f524d4b2da1607b5941987c9591da01842d7ba5cf1ef442d8`  
		Last Modified: Mon, 04 Aug 2025 20:59:20 GMT  
		Size: 34.4 MB (34436755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccfe56d0f83c2b45a04e2d8dfa45f737a5f06068e755d1cf7cf36272df01db4c`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d734b8ae6fdeb107c2533e63ad5f1b473247698e5cca986f3fd8b026bbfbf28e`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 983.8 KB (983820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ffe9aaa7aa6de73af43a17a9193a13f43337de84804c51a167ad83538e69cb6`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:324dd6780d35d4d930390f89bb2cc09b28ab0ab8376386c254781771b7a772e6`  
		Last Modified: Mon, 04 Aug 2025 20:59:12 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:ded8c47f813c8d5533379e04bd78ffd97a169e4a33cbdaaf72f8741cf9ede86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2202204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e5c9ceef9330c05579c9fd204d1be12aaab0a29c0fd28347e7736fb826b31b`

```dockerfile
```

-	Layers:
	-	`sha256:3ce986804eb8aa74b49248f92ff30b01ca67114e40d34a1636beedc973d81d8b`  
		Last Modified: Mon, 04 Aug 2025 22:14:12 GMT  
		Size: 2.2 MB (2170585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:650629cff569d1105c7da001ff4f736f229bb18f0241208820506cb6226fc367`  
		Last Modified: Mon, 04 Aug 2025 22:14:13 GMT  
		Size: 31.6 KB (31619 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:57f049c8b47c5775859cbdfa374607111c7d418e22f12cf5bb7920f2063c2aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79128056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a6683e9c665154286e00e0dfea3d0ddaa6fc044afcd7caee6e437d2b39d56e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c06a09b74ec526da3ee14df3d2b5a91f72a4fa277f482bbf918bb4cccb1652b`  
		Last Modified: Tue, 05 Aug 2025 00:06:20 GMT  
		Size: 3.6 MB (3611165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed9e57a166c2abcf7305f3cb2afd6de830c6af45dd6c91b2a8218f7a4912f6c`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47e0e72d666cf9be46385f732d53bc45342fa962757abf4c31f4b45015775159`  
		Last Modified: Tue, 05 Aug 2025 00:06:19 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2149fd89f974e7ea3dea06f37d735922f1379a8f6a3848f9f27b655a231533a`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 13.7 MB (13653344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7733690cb25c9174f17fcd594fb9aa92de487681f9a30a88d38ce0fb49dfc9b7`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56aa0ea4063f0f606994769dabd9afcf81090a22a66567e6f1bbad01c84cef`  
		Last Modified: Tue, 05 Aug 2025 00:46:31 GMT  
		Size: 21.9 MB (21877960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555ac5f064703fcb811adc2fc69166c7117941c125b03426671e1d4f55cc4f67`  
		Last Modified: Tue, 05 Aug 2025 00:46:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa79fbfe4077bdecbc88d7a5d32f94313e38f9fcff1170cbba0b60e5f5454ae`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb096667c2eb8e8cc9f745a91245901b951632f05bd4a18c84e5fc700638654e`  
		Last Modified: Tue, 05 Aug 2025 00:46:30 GMT  
		Size: 19.7 KB (19731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1b83dffa45f0edf0a1799b639b0fe41010c6dc26daab3cc2ef4cc0b91d9b0b`  
		Last Modified: Tue, 05 Aug 2025 05:16:22 GMT  
		Size: 35.2 MB (35236910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e32f6aebd439ba8d413a2195d63d2c585e5e02c6dab1edf8a99373046e6e7f3`  
		Last Modified: Tue, 05 Aug 2025 05:16:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaac5d9ba510f90dc7373a9658a66baddb71aceb65465cb13540244ab0b77fc5`  
		Last Modified: Tue, 05 Aug 2025 05:16:18 GMT  
		Size: 977.2 KB (977236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0597ed65ad041e26db8cbc906e55caff1995219723badc8ba3d5ca7c506aca`  
		Last Modified: Tue, 05 Aug 2025 05:16:18 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50957638bb2745278398389025f8d8196d8e51f97b8a359bbe9137f1456beeb8`  
		Last Modified: Tue, 05 Aug 2025 05:16:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:2e96e1493048b9a2ce6ea1ab85b86253fe75966f7fac5c8779e014ddce68a5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2201068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:017f81ae467c4a4fa2a12508b8f2aa84ea796f1714444da9befbf5d3a8357962`

```dockerfile
```

-	Layers:
	-	`sha256:41fb3e7bf64afe3d05635d6709a31f9a7c26e44042a90671009534606dd1bb67`  
		Last Modified: Tue, 05 Aug 2025 07:13:43 GMT  
		Size: 2.2 MB (2169365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a810c0f0f5c586b41fcc1ccf9e89e585a4869aa9d981b690543569a86675602`  
		Last Modified: Tue, 05 Aug 2025 07:13:44 GMT  
		Size: 31.7 KB (31703 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:980909ad037a24e51ba3429498490c3843de5323e00ecdf3df7735708c74dbf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73835415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27da9235b3a9747d939dbe21f6ef318657a6b3baca42b6c5664adda60a517bd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c293b040c7a67eeac13c53a522990f19f36e1b39939bdc55cbe7dbeefa2c82`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 3.6 MB (3594168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4153c5fef55d21621d3f69b9fd9a25c43bda1995413d8f4dcacf545b0d8d2a0b`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc109449c55003e3c992ac8133ad0a1b0794f6911cb2e1cc81ff0acc6e85daa1`  
		Last Modified: Wed, 16 Jul 2025 04:08:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0c69a28ac4d61cac15663b00afee7413a9a9efb61c173baf6d196a4a2b9eec`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 13.7 MB (13653334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e800d2c2d3dcabafd275ce5da9cd5b69a400c8d4e434fe0e169de8f847150c16`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc97540dd5b29ed35499d386792721453e9f2993fb6f31092fe292cb6cda3058`  
		Last Modified: Tue, 05 Aug 2025 07:03:57 GMT  
		Size: 20.4 MB (20394813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:362d682aa8b41ba1c48a1513a4764d3db005a8137af9425b4d401f86d8da3f88`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59b4c9e4ab292bff4638f9d9c3c6bc2450aaf32e67ac31c00ae732b7f092d3c`  
		Last Modified: Tue, 05 Aug 2025 07:03:55 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb9edc9e8c62872be6f09d92a7e349b9ecbbf22f3ca071428c2f79c001def07`  
		Last Modified: Tue, 05 Aug 2025 07:03:54 GMT  
		Size: 19.7 KB (19736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881222ef14b0d5e786e3466828f16530cdf02394d48ed40521acec353050c3e8`  
		Last Modified: Wed, 06 Aug 2025 09:08:34 GMT  
		Size: 31.1 MB (31108914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e1c5d76f8d2e998778c7ad2d7c0bbe518c050e6e366cdc8dcc6ea90cc70961`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087f1c391e30813fd4fa6ee493863cb0bbe2e4f360450d7ecabaff5de0139545`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 1.5 MB (1527045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32f8488d1a46211627180c2fd827b894dab9a4f3b11ffd718270ccb440bf8f59`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1039958b2ef45d29d5ee5f8ed5e67b16fa0024ebdb8988d1f70d1327df8b992`  
		Last Modified: Wed, 06 Aug 2025 09:08:33 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:f9ced1def07c8e1140a9f4e13ef6f9896310fbbd6ebc4b1b72b91321125c343f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bb6869646674227adb986e14bcf7811d8c7fae642eb0b9b47944d54ea73d791`

```dockerfile
```

-	Layers:
	-	`sha256:688626909813c8c53a4d5643a92cc1ef76d6c723c65c626749f6cde3fefd2700`  
		Last Modified: Wed, 06 Aug 2025 10:13:48 GMT  
		Size: 2.2 MB (2167632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d53448c67f2dc151d63d9415a2f4979994344d99f768f96e615bf3d5af0790b6`  
		Last Modified: Wed, 06 Aug 2025 10:13:49 GMT  
		Size: 31.7 KB (31706 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:3454652f5c01659d7d14d4484f06c37464ca11b213e78de7ce29ba077e89f36e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75286560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5447e24db8ba6387cc17dcb0049fb80a50cbe97103813f4783213211fe95c4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 11 Jul 2025 06:25:48 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["/bin/sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 11 Jul 2025 06:25:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 11 Jul 2025 06:25:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_VERSION=8.4.11
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.11.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.11.tar.xz.asc
# Fri, 11 Jul 2025 06:25:48 GMT
ENV PHP_SHA256=04cd331380a8683a5c2503938eb51764d48d507c53ad4208d2c82e0eed779a00
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["php" "-a"]
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_HOME=/tmp
# Fri, 11 Jul 2025 06:25:48 GMT
ENV COMPOSER_VERSION=2.8.10
# Fri, 11 Jul 2025 06:25:48 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Fri, 11 Jul 2025 06:25:48 GMT
WORKDIR /app
# Fri, 11 Jul 2025 06:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 11 Jul 2025 06:25:48 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d15b60ab2e403d45cb5d55d6ca4fec6dd4b321b0b3cbc9546510731b3196b34`  
		Last Modified: Mon, 04 Aug 2025 22:19:48 GMT  
		Size: 3.7 MB (3679854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3a40b40361a6800f5592be421b6f972babf00ef4514af5b3cbbbecca685cb4`  
		Last Modified: Mon, 04 Aug 2025 22:19:47 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef30c8663103c30e07298c1dfa1db3aff21896305d5331f168c38f508379cdd6`  
		Last Modified: Mon, 04 Aug 2025 22:19:46 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08eafa4a3224fe6eb688860741f0e8b65ac49b919952d4a7d1e5a4d195e134b`  
		Last Modified: Mon, 04 Aug 2025 22:58:42 GMT  
		Size: 13.7 MB (13653336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796e5c7e7fd28fa790bea89b2528028cbd5ba464a2cb410bd870445103de9197`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd0c014783d431392fbe4b78080b9c1485624e796271f5c4962f96941a32672`  
		Last Modified: Mon, 04 Aug 2025 22:58:56 GMT  
		Size: 21.5 MB (21451616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc2a328a5b7b993670851ac5c6d63c129a67f13f999a03570b930367d089028`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5907607760dc2ba6786bf93d6c9d658346353233ad6c45f9d5bb678fb84e4ea`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18809b1760a6fe568eea4d22f4a08260e8eb4844a67a924b8f1ad360fcc505a0`  
		Last Modified: Mon, 04 Aug 2025 22:58:40 GMT  
		Size: 19.7 KB (19741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82d55c6b75b483330745503675543c8c8cd53487c52f04fc538ffca072685af4`  
		Last Modified: Tue, 05 Aug 2025 03:05:15 GMT  
		Size: 31.8 MB (31838538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e906a6e05460592955352f726700115f5fd99ecac21d52a8a8f215008ac11b`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63184a90ffc761dc4e7021b2ac5bdd5b532c00e7ec5b3117482911a54a0da2e4`  
		Last Modified: Tue, 05 Aug 2025 03:05:11 GMT  
		Size: 973.9 KB (973898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571c018a34b28319ba20267a7ce0ed4a6a55c45f0d9f82e9bfb0463a01ccbc8a`  
		Last Modified: Tue, 05 Aug 2025 03:05:13 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f5b12f8a659364b18b513be700392ed488b402212825aa2628511d39a1fdcb`  
		Last Modified: Tue, 05 Aug 2025 03:05:12 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:0cac2c1bd4b7516f02c4901581db87053d7f13d7162ed5893e2385e01d04ed06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2199069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf6d507c9d49db36eb5803a136cba47685933da214626fd6c9169c5b52519c4`

```dockerfile
```

-	Layers:
	-	`sha256:5a2334c87641f2bd18bc7ef2964f426cc33ffda0341112220f04384d1a624de9`  
		Last Modified: Tue, 05 Aug 2025 04:13:53 GMT  
		Size: 2.2 MB (2167414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f8221622de3b92e6e87dc965f40bb6cdc356d9db5fa5fc13a4cf4d519f7d968`  
		Last Modified: Tue, 05 Aug 2025 04:13:54 GMT  
		Size: 31.7 KB (31655 bytes)  
		MIME: application/vnd.in-toto+json
