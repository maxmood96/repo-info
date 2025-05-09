<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.25`](#composer2225)
-	[`composer:2.8`](#composer28)
-	[`composer:2.8.8`](#composer288)
-	[`composer:latest`](#composerlatest)
-	[`composer:lts`](#composerlts)

## `composer:1`

```console
$ docker pull composer@sha256:1f2dffb5e60b2232851e5da51faa5a87b715cd7d3434411bc9ed7ab8fb318a12
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
$ docker pull composer@sha256:0f4c67e6e64d6321482ca6c0093965509d2365644ea1423d05e0745612491779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74274313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4062a1e2997d84b70b4ba69036f6d716e1413e70f0283df7e0d958f57d8e419c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ec51de1f9773447b65e97f0c677dfa7c2c5a643a8e29c2573fa02d440be485`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 3.3 MB (3339405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f347299a473f0f5d9b5f088e95e92fa5f3fdb929eb8c00e8eee8a5e255fa22`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33c8191db1484b005c5fa5405a7076bdae4e90319fa99dc126e7fc70a360264`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a488374895485209654e2f20371d2b15edb0b1e6e389ec7439903ae08bb34`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 13.6 MB (13638342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242d92ffbbeeb68a81285f10e04caea376e536af932c229bac24f4850ead8549`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5f8d392c5efc498dff46eaccd969d3b99752dc1a40cbdbefd63ae52351c93`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 21.0 MB (20961727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69de2e680c8502b2e77e5bfbf4a6121b21f9356fa9b0058eb0967c21456bad`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d926e2db98107193f77ac67f3ebac3c923c205841b5b20f0a86e5c848b2d66`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce880ffb1d3cb33e1a865fd2f05b492474d7197801ef35ea5de68fcd17006a7a`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 31.9 MB (31932770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fb4c279258a28b8cf2f050d72d484d11919bd0c4c3ce9275900c07678241b1`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6418a24afec5c30f1b4e609f196c0de753f9a8e0c56a12bae18732fd086832`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 734.9 KB (734935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd4822b507cb40ebfbcd1328022afc7ce5c839f353a5d7bebee00f367835ec`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f677eb87304cd74f3821d282a00f9c0cd6b4a6ea767d4b8537aacd6106c09`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:781dbf5ecf0c5a65a8c77f473c8c360b44f21408232deccae24abfaf2d1e86aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6246187fd155887e2612892b3299955ed5aa5e72b2bd8f4707c1f7b3a05cb74`

```dockerfile
```

-	Layers:
	-	`sha256:29e1aec381c8a1ad09bfd2c1ac62beaf6f0a23906dd3a96f465500209dcff6c9`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 2.2 MB (2157791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3056a97ef4c62275e5fe7c81289b256c70f367a46c4c049118bdeeea43e44785`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:f1d0220bbd4bff98fbc04df042e0a4a93eb3353969fd81451a4fa2dacaea9121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72539219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222b7e70e02769139002533b8eed20848291be6a79a195df33b4af6572aa805e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce0d04db17a73ca3a7314b885207e80120682c8358368a9254c7f44a7aa2761`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 13.6 MB (13638339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ddeda1f976085a87139c58582b31ac5fd6fc3c900259b39f3163e64bea4ce`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bdf2404f235a46786918527ccb15e5da315bc30edec03f1a23a4d5adbb837c`  
		Last Modified: Thu, 08 May 2025 21:26:22 GMT  
		Size: 19.8 MB (19828990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29e5bd26390c9927b9d705940595b9ccb503518764174068193050a9ee011d3`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837c695d5bcef73c8dfd7be97d8f030b294d365c39fb1ef21f5aec9cebaf695f`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c641fa2ea58cc5073a3f4a40452af3766d1d4eff239fa9c78b7850e692b924`  
		Last Modified: Thu, 08 May 2025 21:56:54 GMT  
		Size: 31.6 MB (31637949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37037a8ef7c2de76decb659167cea10b45dd38661222354aec54af534f7f90e`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff86c18eed79c10a74d1197522cf42536dc5aa3ce2170357d05e02d5ba84c0c4`  
		Last Modified: Thu, 08 May 2025 21:57:31 GMT  
		Size: 735.4 KB (735449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4f0ff217807d5b30a72934277fc9952e68e9ee30ea34fe04850b4b7ab9fea4`  
		Last Modified: Thu, 08 May 2025 21:57:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e3198c4e68f19d71e3441f578b22ede80d1a52712b6bdf192f07f918b47289`  
		Last Modified: Thu, 08 May 2025 21:57:31 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:7b3bc576d829e985480ca4675791c8528a783a38c4d371d57a5db2fd2687190e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90d4f6125a9f566a7bec16427f5757c887d1d5805d2e260f441e0feda3533f1`

```dockerfile
```

-	Layers:
	-	`sha256:69d3a2ca596b8cbbaba446202d30bce8b29c35c2caf834248bcb764d1950acce`  
		Last Modified: Thu, 08 May 2025 21:57:30 GMT  
		Size: 30.3 KB (30296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:843caff2b73baa15c0505e65e3f04e4ff217c519d3fbc60bb1dc04cd95611bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69548231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b852728a94503226eccd2cf97ccb9bea1fbbd675e4404e5b4888f06410820929`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae53c42a3a934e2af6db5b115410a7b4c6a02cd2b122d00b65d1eca1a41169`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 13.6 MB (13638357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10142d79ada8bf8b882c44da37430c2d14e535a18518bf2925f9f960b71e79`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfab14bb194eab55e2e70f9afc13ee33e4dd21aa21350e1374e86f05fb626af`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 18.8 MB (18755156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da76f291cb0bcd5dc8fc90d909e92ab04c17a7553ef5146ab7e325af2708443`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d3e5b7d935e85e9b31895bd1360c16fb666b189cce4d62af34133ff180412`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df80c80dab935ac507aa56dc704c0803d9d2fcf950397319075ec118fc80934`  
		Last Modified: Fri, 09 May 2025 02:56:40 GMT  
		Size: 30.2 MB (30185429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c3a1b4fa684906875f7fd4416d71426ac1aee26864470455b1b9b46d7828d`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad98b7bdd963920e8d2aa877c61dd49507e014c29caef2cbb1d30e7d8bcbb220`  
		Last Modified: Fri, 09 May 2025 02:57:31 GMT  
		Size: 726.0 KB (726042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184d338f49bf9a83a431fd1d913ec8455610f26e653cef26bf7c21f34b2000ec`  
		Last Modified: Fri, 09 May 2025 02:57:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3966652bdd05ee23d88589676e565d4d5f020a8ebddb3f96739160af838aa5f8`  
		Last Modified: Fri, 09 May 2025 02:57:31 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:93da9c0ff3bc3869f678d2eeb4cb4eefcb8ca836a4552bbc1a832c4f87f6d3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce05f151ef8fa03c431fc55b987175152896213bd854e7f0f64aa3dea0ece08d`

```dockerfile
```

-	Layers:
	-	`sha256:7158e1e22f933e338ead7cddeab5933b9173e532a02c5999e0cb2b40f6fa61e6`  
		Last Modified: Fri, 09 May 2025 02:57:30 GMT  
		Size: 2.2 MB (2158107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9f0af9c466c635886e2fdf1663e222e60291a54a101b2146fd8246cf4db82d5`  
		Last Modified: Fri, 09 May 2025 02:57:30 GMT  
		Size: 30.5 KB (30511 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:80c6806a01bb51e046a5c59782505c112a8298724b9be9bc6596c8177bf3a3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74266782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d646a711ad6c20781e47bc4ab0effd6c18e879587de32375e70188b27b5b01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752b27585c21531ef183f9331718681f7d5a399ad1721fe17bf65ec91aa026d`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 3.3 MB (3332291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c504757a74563c6c69cb5f5ab95d450088933adf663323509ef07a437fda44`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64969c8e6dd0ea68ca6e1a455172bdc1ce583b5d543fc3120d33f200e06302a1`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1176f7a4c5fb0e54724b9ad7ea378a6420c35cbfd4d0eeb5e1fef5d9ba7ac`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 13.6 MB (13638372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9788910834fbf94207a3e2b19ab0e6fabbefd4e42d621687e321a1db2f16e53e`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edad5b9c93eee4f4366f3ebeb11225c8f73a2b77b6f9619550727373b01d51f`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 20.5 MB (20506682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aad88073420d66b54ab164736e4f80b7f83ed7afde64e75da65e76a0601f38`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d8baab457dd5125f7b8056acc97da76b6e4aed76359cef6cf89c1be2f9546`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9518d6339aceaab8bbfa04cb293db8787e29591ef024e80b24a882a2c9c8edc0`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 32.0 MB (32036745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e197ccaccec2cf61efc3cdf266d9ef310f66d8e5905a95466247bdefc08c5d4`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041339cf3b7765f89f7a06a66d20ca4f514beb477b3de1192434100f1458eaa0`  
		Last Modified: Fri, 09 May 2025 01:10:49 GMT  
		Size: 735.0 KB (734969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997ba3edba8f59b1e754c8ce9417774952b4b26c318f9ecb09bd8c7f93c61c50`  
		Last Modified: Fri, 09 May 2025 01:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccd51abf26165bd0c932ddbe8e40b0ce8db2744fcab439ed3294ced22fd0542`  
		Last Modified: Fri, 09 May 2025 01:10:49 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:c23808e709498a8ce66df1019fb44e1b0c7e13f73451488586b20acd8e2049c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80761ada1db9def1d994d5056075162af38e85724e76cdf3f5060152676b1b3`

```dockerfile
```

-	Layers:
	-	`sha256:1cd9c65c85a18dc9f83007c5b256b7f0ea90f355d240d3a8553e4a2d37ce48d4`  
		Last Modified: Fri, 09 May 2025 01:10:48 GMT  
		Size: 2.2 MB (2157931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8b4ee9180576d731ede0860a4be552d16258ca83570df0fa58dc2291dee01a0`  
		Last Modified: Fri, 09 May 2025 01:10:48 GMT  
		Size: 30.5 KB (30539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:09d738d324e7358e8718b5f7ea57a746f4dc3f339ef155de256642a69f8bf96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75152758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f4cf43e33194338ba615dd880ce527a12b8bf8cc1d3717b49f884b54f4e9ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0fee7f3118a5985c2f626fb5b6c58f3e09615e2d0e574b152efa48b96dba0`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 3.4 MB (3379885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0859e481ff1d593c72d70f1d40018ee891c8a85aed61e584093925eef0bcab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b986eab8e8b3e0184edeb69c32c4ed3d8588e109c815e0849b82bb054cacab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7b75ef5fb8c211e5b9a329554b4301d5c6eb7ae9c8b76dc280c611f52936f2`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 13.6 MB (13638340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbb0139bcece2c1bb61243f10b29ef44dfb0038edd4f69191a281fb8695da3`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6161bb22ced62e09258a8f26973e62bc0c0b3f09f6fd571bc8cbf3d57d556`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 21.5 MB (21479578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe4c701feaead74489728c530e52569dea2bd050f15b4c2465b658466d6ea38`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aa3b4dea6bd9bd03e0d1ad21c8a068d7303cd61d25541395be92f12129e0a8`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b4c02adc0a7effcc443a0f23a7c458bd7f373f594674c85c29612e9b69169d`  
		Last Modified: Thu, 08 May 2025 21:49:16 GMT  
		Size: 32.4 MB (32419677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164b10f1e3fecdfcbdca38c262d211e9cd19e5376602d901c2600a1fe993cfe0`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dda5b9695333e447d0a7c4f4748401a2b79c927d5727ef067a89fc3793d3b56`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 746.8 KB (746768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeb0ee3f2a513ce981f6712da1e294d7c48715a362dfad8a291bf65215aa3c9`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f677eb87304cd74f3821d282a00f9c0cd6b4a6ea767d4b8537aacd6106c09`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:1f92cfb504783646a2881a10fa7ca7f1e57ead3c343c1d592d7a0ef3b993cbef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9983cf8038dd45e163f112e08e76a5be7b26595d4eff4efbcd99f3c694ebf572`

```dockerfile
```

-	Layers:
	-	`sha256:5ca4157a8a328c2af7d6546f9a59399fc40bf9240afd4854f5a30942b6a31070`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 2.2 MB (2157579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:172e20d08c1bbe37ffcfc9a10f1ff2d6234c75117b69d20e9d2e124b38efd69a`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 30.4 KB (30386 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:424ffeccc9c2c70b1cd6d922530446b3b90a177250b0e46d4adb33bcc5cb218a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77133893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5edab6a4ff0ec5edbbbe7c8110874b686f4cd43a660e9db7555bf574c10792`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e76c061ea4a5ab1435512c8388fd08bd714f08a20a3d13e20958322c1e38c8`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 13.6 MB (13638361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6741176fa79481125f0168dfab2269eb4d272b50ffffa3eb93489fbac4b7e`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baaae08012b74873c8e9eb084b4c040c29cb1b207bf5a13250c34c0533cab9a`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 22.7 MB (22698151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d926e7ce8969775d3b04d34e3a2c99bd3026dadb90880f40e22812f538d9a0c0`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01319ff876f0a90f52b88a0db82b4f34546c97612dc4988123adb15a952cee`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749a6c3d45b6e53322f1fdfcdeff037de2cd648813a8db706c3925473d004f6`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 33.0 MB (32975132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c502c29ed2b1ba6e7fd2c2aa71175f396a9176edb02e55648b6cf8555189787c`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0bec688c7dcf453766099c15c3b8da2376c512ad069fa63310d5cb9cc82ba`  
		Last Modified: Thu, 08 May 2025 23:20:34 GMT  
		Size: 742.1 KB (742090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c235d1d7b2fe242ac49ac0dd27c934595e0d2c297a3abf793b3f7d89013d3`  
		Last Modified: Thu, 08 May 2025 23:20:33 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fc8c13c7d766dbb43871c48ba842a9e8afca0c04966e794d3085f85fdc4880`  
		Last Modified: Thu, 08 May 2025 23:20:33 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:f0f835d0ffedfb730941109b859c5963cd3860254b2247966329c3a531a2b50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993b97a7bbbc6ef55f77d59cbc70d01f9f14ea1e935c3488063374fbbe7b0b18`

```dockerfile
```

-	Layers:
	-	`sha256:3beb8afe05752b3cc2fef829b05837c9a529997560a885e3bcf0fc2d08f38ace`  
		Last Modified: Thu, 08 May 2025 23:20:33 GMT  
		Size: 2.2 MB (2156348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c0304b62dfebf2eac13965ccd918bca1a2b76d7d8cb6f9ff0b914ab0a6381e`  
		Last Modified: Thu, 08 May 2025 23:20:33 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:1c1ee0042173c923770d0e23e6bde4763120d5e18e712f08c90fac69c0d3e732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73417077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53beb463b1f33e7b81cec41725633e81740c4680945ad53a4694aeb7c452e352`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db7ef0a049248006688e39882ca6ced21701e3d55e7cb2f43eb10572e33c7`  
		Last Modified: Fri, 09 May 2025 01:02:09 GMT  
		Size: 13.6 MB (13638347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ccd5673892b28566480f109c15f00e40dac754b53ccd5b997b3b0f7f75b66a`  
		Last Modified: Fri, 09 May 2025 01:02:06 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0f3c897c5b22a06c34b5e67cc4b30c94cf9e55e8b3176d9f4c5f0408e96f1a`  
		Last Modified: Fri, 09 May 2025 01:02:10 GMT  
		Size: 21.2 MB (21162501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef46c091109b0dad546606ab5e3c6ab60d516a7707483f98fa96053dcda29e`  
		Last Modified: Fri, 09 May 2025 01:02:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b931b251640e1d77e3e5386e76828941f021bb5b7fd085a60db7df564d2db`  
		Last Modified: Fri, 09 May 2025 01:02:08 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d591c20251c0df6262a43882dff69cf24f872cb167d9bd70dbe59ce535d6090`  
		Last Modified: Fri, 09 May 2025 16:04:38 GMT  
		Size: 31.0 MB (31044006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56519a808e922477caef5d3ce688e3619da9f0db1b63ff8ca95f3204fd8facec`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027191c585b4f9bbf18caa4794ac5f797b5a97ec36ad1784bc38f9f09090f1af`  
		Last Modified: Fri, 09 May 2025 16:09:43 GMT  
		Size: 733.1 KB (733139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22937d96cf5fb511c65f446d5d98f1aa7e4bde29f13ca21bf1b2e286d2f0f75e`  
		Last Modified: Fri, 09 May 2025 16:09:43 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37cbf32a3d34fe8547b6abcb834f1d4489ed95fe123a474aa51637645a800b1`  
		Last Modified: Fri, 09 May 2025 16:09:43 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:c6582f375eb9c9b2286b9b9b49be48dc9646f381a771347bbc8acb2803319078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6394f221a0ab1860afcb6593842a126ca3b269ce7df49d3e3f97798e89760615`

```dockerfile
```

-	Layers:
	-	`sha256:190c4740fb044750cd91a35e45e3ad39c497ec94216e7f63755deff53ec3eac4`  
		Last Modified: Fri, 09 May 2025 16:09:43 GMT  
		Size: 2.2 MB (2155290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a278b93dba2daada9e316b2788eeb927df0c370186a31232feebf23775be385`  
		Last Modified: Fri, 09 May 2025 16:09:42 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:196413d261e36c6d32f6a1b7e488c9b0e7421317149953ef15fcb0fcba922fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75390492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8429b1a6f22e8ba761457c5c21bbaa6a6affe86ab01a8182cc08ee91cc30494`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b5f11089bad6dd57e7f9c626829578bab2c83d4a9d3e6c9dd1c73eccd0d96`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 13.6 MB (13638363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925304c10005fd175f8945f9b79556931bf8772002494541acf614752b95348`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbdcbc01a58fa9ca47c12882f0c582c63ddf71a40fbf79fa956decd72f0f45`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 22.2 MB (22248891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234da8b1110c7fe66f09e4181941a3db5f83769849d61bd62db5481617b0183`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e59c13cf761428c460597e931fe7482a363b6b0afb29d60205e1fa1bc0d234`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da82aeb01a0294d366bfecf08eef375887e0728de96b73baf2f614fc770d6ee4`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 31.7 MB (31706531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47454c44bffd2e898699df83390dc5586ecf0cdb8cf4e637dfbe6e862166142`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7c1f60d28958552dd5115e8a939ee09597c03bf544b0246cfb20eec9b25ba3`  
		Last Modified: Fri, 09 May 2025 01:21:05 GMT  
		Size: 738.2 KB (738232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07989b8e7844e52f9ba59d42bc09551bb7338b0eac68433e6585127a119b0e5`  
		Last Modified: Fri, 09 May 2025 01:21:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929a49085ad3c137c6b1d488d8122e4179631269e5d564454c4f63d8a7e4ecbb`  
		Last Modified: Fri, 09 May 2025 01:21:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:2ada178a5e2553396e880950ea7a59e890a59379ef244e1dc5ba1b628f5cdcf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd05a2973df0eb021fe768f352d8127e203db74c48984f8bc75494e1af8fc9bb`

```dockerfile
```

-	Layers:
	-	`sha256:a3283ddfd3dc52b6f02f2d11b1454443e9d0fce05ca2a2d23e5e9427bba08f31`  
		Last Modified: Fri, 09 May 2025 01:21:04 GMT  
		Size: 2.2 MB (2155076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:328713a09f398eeca2d5a0a8169e4da8e06abf6184564cf66fb87e8a75e3d405`  
		Last Modified: Fri, 09 May 2025 01:21:04 GMT  
		Size: 30.4 KB (30416 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:1f2dffb5e60b2232851e5da51faa5a87b715cd7d3434411bc9ed7ab8fb318a12
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
$ docker pull composer@sha256:0f4c67e6e64d6321482ca6c0093965509d2365644ea1423d05e0745612491779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74274313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4062a1e2997d84b70b4ba69036f6d716e1413e70f0283df7e0d958f57d8e419c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ec51de1f9773447b65e97f0c677dfa7c2c5a643a8e29c2573fa02d440be485`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 3.3 MB (3339405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f347299a473f0f5d9b5f088e95e92fa5f3fdb929eb8c00e8eee8a5e255fa22`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33c8191db1484b005c5fa5405a7076bdae4e90319fa99dc126e7fc70a360264`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a488374895485209654e2f20371d2b15edb0b1e6e389ec7439903ae08bb34`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 13.6 MB (13638342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242d92ffbbeeb68a81285f10e04caea376e536af932c229bac24f4850ead8549`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5f8d392c5efc498dff46eaccd969d3b99752dc1a40cbdbefd63ae52351c93`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 21.0 MB (20961727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69de2e680c8502b2e77e5bfbf4a6121b21f9356fa9b0058eb0967c21456bad`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d926e2db98107193f77ac67f3ebac3c923c205841b5b20f0a86e5c848b2d66`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce880ffb1d3cb33e1a865fd2f05b492474d7197801ef35ea5de68fcd17006a7a`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 31.9 MB (31932770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fb4c279258a28b8cf2f050d72d484d11919bd0c4c3ce9275900c07678241b1`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6418a24afec5c30f1b4e609f196c0de753f9a8e0c56a12bae18732fd086832`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 734.9 KB (734935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd4822b507cb40ebfbcd1328022afc7ce5c839f353a5d7bebee00f367835ec`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f677eb87304cd74f3821d282a00f9c0cd6b4a6ea767d4b8537aacd6106c09`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:781dbf5ecf0c5a65a8c77f473c8c360b44f21408232deccae24abfaf2d1e86aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6246187fd155887e2612892b3299955ed5aa5e72b2bd8f4707c1f7b3a05cb74`

```dockerfile
```

-	Layers:
	-	`sha256:29e1aec381c8a1ad09bfd2c1ac62beaf6f0a23906dd3a96f465500209dcff6c9`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 2.2 MB (2157791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3056a97ef4c62275e5fe7c81289b256c70f367a46c4c049118bdeeea43e44785`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:f1d0220bbd4bff98fbc04df042e0a4a93eb3353969fd81451a4fa2dacaea9121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72539219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222b7e70e02769139002533b8eed20848291be6a79a195df33b4af6572aa805e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce0d04db17a73ca3a7314b885207e80120682c8358368a9254c7f44a7aa2761`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 13.6 MB (13638339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ddeda1f976085a87139c58582b31ac5fd6fc3c900259b39f3163e64bea4ce`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bdf2404f235a46786918527ccb15e5da315bc30edec03f1a23a4d5adbb837c`  
		Last Modified: Thu, 08 May 2025 21:26:22 GMT  
		Size: 19.8 MB (19828990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29e5bd26390c9927b9d705940595b9ccb503518764174068193050a9ee011d3`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837c695d5bcef73c8dfd7be97d8f030b294d365c39fb1ef21f5aec9cebaf695f`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c641fa2ea58cc5073a3f4a40452af3766d1d4eff239fa9c78b7850e692b924`  
		Last Modified: Thu, 08 May 2025 21:56:54 GMT  
		Size: 31.6 MB (31637949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37037a8ef7c2de76decb659167cea10b45dd38661222354aec54af534f7f90e`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff86c18eed79c10a74d1197522cf42536dc5aa3ce2170357d05e02d5ba84c0c4`  
		Last Modified: Thu, 08 May 2025 21:57:31 GMT  
		Size: 735.4 KB (735449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4f0ff217807d5b30a72934277fc9952e68e9ee30ea34fe04850b4b7ab9fea4`  
		Last Modified: Thu, 08 May 2025 21:57:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e3198c4e68f19d71e3441f578b22ede80d1a52712b6bdf192f07f918b47289`  
		Last Modified: Thu, 08 May 2025 21:57:31 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:7b3bc576d829e985480ca4675791c8528a783a38c4d371d57a5db2fd2687190e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90d4f6125a9f566a7bec16427f5757c887d1d5805d2e260f441e0feda3533f1`

```dockerfile
```

-	Layers:
	-	`sha256:69d3a2ca596b8cbbaba446202d30bce8b29c35c2caf834248bcb764d1950acce`  
		Last Modified: Thu, 08 May 2025 21:57:30 GMT  
		Size: 30.3 KB (30296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:843caff2b73baa15c0505e65e3f04e4ff217c519d3fbc60bb1dc04cd95611bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69548231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b852728a94503226eccd2cf97ccb9bea1fbbd675e4404e5b4888f06410820929`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae53c42a3a934e2af6db5b115410a7b4c6a02cd2b122d00b65d1eca1a41169`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 13.6 MB (13638357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10142d79ada8bf8b882c44da37430c2d14e535a18518bf2925f9f960b71e79`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfab14bb194eab55e2e70f9afc13ee33e4dd21aa21350e1374e86f05fb626af`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 18.8 MB (18755156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da76f291cb0bcd5dc8fc90d909e92ab04c17a7553ef5146ab7e325af2708443`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d3e5b7d935e85e9b31895bd1360c16fb666b189cce4d62af34133ff180412`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df80c80dab935ac507aa56dc704c0803d9d2fcf950397319075ec118fc80934`  
		Last Modified: Fri, 09 May 2025 02:56:40 GMT  
		Size: 30.2 MB (30185429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c3a1b4fa684906875f7fd4416d71426ac1aee26864470455b1b9b46d7828d`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad98b7bdd963920e8d2aa877c61dd49507e014c29caef2cbb1d30e7d8bcbb220`  
		Last Modified: Fri, 09 May 2025 02:57:31 GMT  
		Size: 726.0 KB (726042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184d338f49bf9a83a431fd1d913ec8455610f26e653cef26bf7c21f34b2000ec`  
		Last Modified: Fri, 09 May 2025 02:57:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3966652bdd05ee23d88589676e565d4d5f020a8ebddb3f96739160af838aa5f8`  
		Last Modified: Fri, 09 May 2025 02:57:31 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:93da9c0ff3bc3869f678d2eeb4cb4eefcb8ca836a4552bbc1a832c4f87f6d3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce05f151ef8fa03c431fc55b987175152896213bd854e7f0f64aa3dea0ece08d`

```dockerfile
```

-	Layers:
	-	`sha256:7158e1e22f933e338ead7cddeab5933b9173e532a02c5999e0cb2b40f6fa61e6`  
		Last Modified: Fri, 09 May 2025 02:57:30 GMT  
		Size: 2.2 MB (2158107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9f0af9c466c635886e2fdf1663e222e60291a54a101b2146fd8246cf4db82d5`  
		Last Modified: Fri, 09 May 2025 02:57:30 GMT  
		Size: 30.5 KB (30511 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:80c6806a01bb51e046a5c59782505c112a8298724b9be9bc6596c8177bf3a3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74266782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d646a711ad6c20781e47bc4ab0effd6c18e879587de32375e70188b27b5b01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752b27585c21531ef183f9331718681f7d5a399ad1721fe17bf65ec91aa026d`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 3.3 MB (3332291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c504757a74563c6c69cb5f5ab95d450088933adf663323509ef07a437fda44`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64969c8e6dd0ea68ca6e1a455172bdc1ce583b5d543fc3120d33f200e06302a1`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1176f7a4c5fb0e54724b9ad7ea378a6420c35cbfd4d0eeb5e1fef5d9ba7ac`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 13.6 MB (13638372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9788910834fbf94207a3e2b19ab0e6fabbefd4e42d621687e321a1db2f16e53e`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edad5b9c93eee4f4366f3ebeb11225c8f73a2b77b6f9619550727373b01d51f`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 20.5 MB (20506682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aad88073420d66b54ab164736e4f80b7f83ed7afde64e75da65e76a0601f38`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d8baab457dd5125f7b8056acc97da76b6e4aed76359cef6cf89c1be2f9546`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9518d6339aceaab8bbfa04cb293db8787e29591ef024e80b24a882a2c9c8edc0`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 32.0 MB (32036745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e197ccaccec2cf61efc3cdf266d9ef310f66d8e5905a95466247bdefc08c5d4`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041339cf3b7765f89f7a06a66d20ca4f514beb477b3de1192434100f1458eaa0`  
		Last Modified: Fri, 09 May 2025 01:10:49 GMT  
		Size: 735.0 KB (734969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997ba3edba8f59b1e754c8ce9417774952b4b26c318f9ecb09bd8c7f93c61c50`  
		Last Modified: Fri, 09 May 2025 01:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccd51abf26165bd0c932ddbe8e40b0ce8db2744fcab439ed3294ced22fd0542`  
		Last Modified: Fri, 09 May 2025 01:10:49 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:c23808e709498a8ce66df1019fb44e1b0c7e13f73451488586b20acd8e2049c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80761ada1db9def1d994d5056075162af38e85724e76cdf3f5060152676b1b3`

```dockerfile
```

-	Layers:
	-	`sha256:1cd9c65c85a18dc9f83007c5b256b7f0ea90f355d240d3a8553e4a2d37ce48d4`  
		Last Modified: Fri, 09 May 2025 01:10:48 GMT  
		Size: 2.2 MB (2157931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8b4ee9180576d731ede0860a4be552d16258ca83570df0fa58dc2291dee01a0`  
		Last Modified: Fri, 09 May 2025 01:10:48 GMT  
		Size: 30.5 KB (30539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:09d738d324e7358e8718b5f7ea57a746f4dc3f339ef155de256642a69f8bf96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75152758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f4cf43e33194338ba615dd880ce527a12b8bf8cc1d3717b49f884b54f4e9ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0fee7f3118a5985c2f626fb5b6c58f3e09615e2d0e574b152efa48b96dba0`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 3.4 MB (3379885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0859e481ff1d593c72d70f1d40018ee891c8a85aed61e584093925eef0bcab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b986eab8e8b3e0184edeb69c32c4ed3d8588e109c815e0849b82bb054cacab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7b75ef5fb8c211e5b9a329554b4301d5c6eb7ae9c8b76dc280c611f52936f2`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 13.6 MB (13638340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbb0139bcece2c1bb61243f10b29ef44dfb0038edd4f69191a281fb8695da3`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6161bb22ced62e09258a8f26973e62bc0c0b3f09f6fd571bc8cbf3d57d556`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 21.5 MB (21479578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe4c701feaead74489728c530e52569dea2bd050f15b4c2465b658466d6ea38`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aa3b4dea6bd9bd03e0d1ad21c8a068d7303cd61d25541395be92f12129e0a8`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b4c02adc0a7effcc443a0f23a7c458bd7f373f594674c85c29612e9b69169d`  
		Last Modified: Thu, 08 May 2025 21:49:16 GMT  
		Size: 32.4 MB (32419677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164b10f1e3fecdfcbdca38c262d211e9cd19e5376602d901c2600a1fe993cfe0`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dda5b9695333e447d0a7c4f4748401a2b79c927d5727ef067a89fc3793d3b56`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 746.8 KB (746768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeb0ee3f2a513ce981f6712da1e294d7c48715a362dfad8a291bf65215aa3c9`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f677eb87304cd74f3821d282a00f9c0cd6b4a6ea767d4b8537aacd6106c09`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:1f92cfb504783646a2881a10fa7ca7f1e57ead3c343c1d592d7a0ef3b993cbef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9983cf8038dd45e163f112e08e76a5be7b26595d4eff4efbcd99f3c694ebf572`

```dockerfile
```

-	Layers:
	-	`sha256:5ca4157a8a328c2af7d6546f9a59399fc40bf9240afd4854f5a30942b6a31070`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 2.2 MB (2157579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:172e20d08c1bbe37ffcfc9a10f1ff2d6234c75117b69d20e9d2e124b38efd69a`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 30.4 KB (30386 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:424ffeccc9c2c70b1cd6d922530446b3b90a177250b0e46d4adb33bcc5cb218a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77133893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5edab6a4ff0ec5edbbbe7c8110874b686f4cd43a660e9db7555bf574c10792`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e76c061ea4a5ab1435512c8388fd08bd714f08a20a3d13e20958322c1e38c8`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 13.6 MB (13638361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6741176fa79481125f0168dfab2269eb4d272b50ffffa3eb93489fbac4b7e`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baaae08012b74873c8e9eb084b4c040c29cb1b207bf5a13250c34c0533cab9a`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 22.7 MB (22698151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d926e7ce8969775d3b04d34e3a2c99bd3026dadb90880f40e22812f538d9a0c0`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01319ff876f0a90f52b88a0db82b4f34546c97612dc4988123adb15a952cee`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749a6c3d45b6e53322f1fdfcdeff037de2cd648813a8db706c3925473d004f6`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 33.0 MB (32975132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c502c29ed2b1ba6e7fd2c2aa71175f396a9176edb02e55648b6cf8555189787c`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0bec688c7dcf453766099c15c3b8da2376c512ad069fa63310d5cb9cc82ba`  
		Last Modified: Thu, 08 May 2025 23:20:34 GMT  
		Size: 742.1 KB (742090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c235d1d7b2fe242ac49ac0dd27c934595e0d2c297a3abf793b3f7d89013d3`  
		Last Modified: Thu, 08 May 2025 23:20:33 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fc8c13c7d766dbb43871c48ba842a9e8afca0c04966e794d3085f85fdc4880`  
		Last Modified: Thu, 08 May 2025 23:20:33 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:f0f835d0ffedfb730941109b859c5963cd3860254b2247966329c3a531a2b50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993b97a7bbbc6ef55f77d59cbc70d01f9f14ea1e935c3488063374fbbe7b0b18`

```dockerfile
```

-	Layers:
	-	`sha256:3beb8afe05752b3cc2fef829b05837c9a529997560a885e3bcf0fc2d08f38ace`  
		Last Modified: Thu, 08 May 2025 23:20:33 GMT  
		Size: 2.2 MB (2156348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c0304b62dfebf2eac13965ccd918bca1a2b76d7d8cb6f9ff0b914ab0a6381e`  
		Last Modified: Thu, 08 May 2025 23:20:33 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:1c1ee0042173c923770d0e23e6bde4763120d5e18e712f08c90fac69c0d3e732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73417077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53beb463b1f33e7b81cec41725633e81740c4680945ad53a4694aeb7c452e352`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db7ef0a049248006688e39882ca6ced21701e3d55e7cb2f43eb10572e33c7`  
		Last Modified: Fri, 09 May 2025 01:02:09 GMT  
		Size: 13.6 MB (13638347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ccd5673892b28566480f109c15f00e40dac754b53ccd5b997b3b0f7f75b66a`  
		Last Modified: Fri, 09 May 2025 01:02:06 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0f3c897c5b22a06c34b5e67cc4b30c94cf9e55e8b3176d9f4c5f0408e96f1a`  
		Last Modified: Fri, 09 May 2025 01:02:10 GMT  
		Size: 21.2 MB (21162501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef46c091109b0dad546606ab5e3c6ab60d516a7707483f98fa96053dcda29e`  
		Last Modified: Fri, 09 May 2025 01:02:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b931b251640e1d77e3e5386e76828941f021bb5b7fd085a60db7df564d2db`  
		Last Modified: Fri, 09 May 2025 01:02:08 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d591c20251c0df6262a43882dff69cf24f872cb167d9bd70dbe59ce535d6090`  
		Last Modified: Fri, 09 May 2025 16:04:38 GMT  
		Size: 31.0 MB (31044006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56519a808e922477caef5d3ce688e3619da9f0db1b63ff8ca95f3204fd8facec`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027191c585b4f9bbf18caa4794ac5f797b5a97ec36ad1784bc38f9f09090f1af`  
		Last Modified: Fri, 09 May 2025 16:09:43 GMT  
		Size: 733.1 KB (733139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22937d96cf5fb511c65f446d5d98f1aa7e4bde29f13ca21bf1b2e286d2f0f75e`  
		Last Modified: Fri, 09 May 2025 16:09:43 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37cbf32a3d34fe8547b6abcb834f1d4489ed95fe123a474aa51637645a800b1`  
		Last Modified: Fri, 09 May 2025 16:09:43 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:c6582f375eb9c9b2286b9b9b49be48dc9646f381a771347bbc8acb2803319078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6394f221a0ab1860afcb6593842a126ca3b269ce7df49d3e3f97798e89760615`

```dockerfile
```

-	Layers:
	-	`sha256:190c4740fb044750cd91a35e45e3ad39c497ec94216e7f63755deff53ec3eac4`  
		Last Modified: Fri, 09 May 2025 16:09:43 GMT  
		Size: 2.2 MB (2155290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a278b93dba2daada9e316b2788eeb927df0c370186a31232feebf23775be385`  
		Last Modified: Fri, 09 May 2025 16:09:42 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:196413d261e36c6d32f6a1b7e488c9b0e7421317149953ef15fcb0fcba922fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75390492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8429b1a6f22e8ba761457c5c21bbaa6a6affe86ab01a8182cc08ee91cc30494`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b5f11089bad6dd57e7f9c626829578bab2c83d4a9d3e6c9dd1c73eccd0d96`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 13.6 MB (13638363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925304c10005fd175f8945f9b79556931bf8772002494541acf614752b95348`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbdcbc01a58fa9ca47c12882f0c582c63ddf71a40fbf79fa956decd72f0f45`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 22.2 MB (22248891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234da8b1110c7fe66f09e4181941a3db5f83769849d61bd62db5481617b0183`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e59c13cf761428c460597e931fe7482a363b6b0afb29d60205e1fa1bc0d234`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da82aeb01a0294d366bfecf08eef375887e0728de96b73baf2f614fc770d6ee4`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 31.7 MB (31706531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47454c44bffd2e898699df83390dc5586ecf0cdb8cf4e637dfbe6e862166142`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7c1f60d28958552dd5115e8a939ee09597c03bf544b0246cfb20eec9b25ba3`  
		Last Modified: Fri, 09 May 2025 01:21:05 GMT  
		Size: 738.2 KB (738232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07989b8e7844e52f9ba59d42bc09551bb7338b0eac68433e6585127a119b0e5`  
		Last Modified: Fri, 09 May 2025 01:21:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929a49085ad3c137c6b1d488d8122e4179631269e5d564454c4f63d8a7e4ecbb`  
		Last Modified: Fri, 09 May 2025 01:21:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:2ada178a5e2553396e880950ea7a59e890a59379ef244e1dc5ba1b628f5cdcf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd05a2973df0eb021fe768f352d8127e203db74c48984f8bc75494e1af8fc9bb`

```dockerfile
```

-	Layers:
	-	`sha256:a3283ddfd3dc52b6f02f2d11b1454443e9d0fce05ca2a2d23e5e9427bba08f31`  
		Last Modified: Fri, 09 May 2025 01:21:04 GMT  
		Size: 2.2 MB (2155076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:328713a09f398eeca2d5a0a8169e4da8e06abf6184564cf66fb87e8a75e3d405`  
		Last Modified: Fri, 09 May 2025 01:21:04 GMT  
		Size: 30.4 KB (30416 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:1f2dffb5e60b2232851e5da51faa5a87b715cd7d3434411bc9ed7ab8fb318a12
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
$ docker pull composer@sha256:0f4c67e6e64d6321482ca6c0093965509d2365644ea1423d05e0745612491779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74274313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4062a1e2997d84b70b4ba69036f6d716e1413e70f0283df7e0d958f57d8e419c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ec51de1f9773447b65e97f0c677dfa7c2c5a643a8e29c2573fa02d440be485`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 3.3 MB (3339405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f347299a473f0f5d9b5f088e95e92fa5f3fdb929eb8c00e8eee8a5e255fa22`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33c8191db1484b005c5fa5405a7076bdae4e90319fa99dc126e7fc70a360264`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a488374895485209654e2f20371d2b15edb0b1e6e389ec7439903ae08bb34`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 13.6 MB (13638342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242d92ffbbeeb68a81285f10e04caea376e536af932c229bac24f4850ead8549`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5f8d392c5efc498dff46eaccd969d3b99752dc1a40cbdbefd63ae52351c93`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 21.0 MB (20961727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69de2e680c8502b2e77e5bfbf4a6121b21f9356fa9b0058eb0967c21456bad`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d926e2db98107193f77ac67f3ebac3c923c205841b5b20f0a86e5c848b2d66`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce880ffb1d3cb33e1a865fd2f05b492474d7197801ef35ea5de68fcd17006a7a`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 31.9 MB (31932770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fb4c279258a28b8cf2f050d72d484d11919bd0c4c3ce9275900c07678241b1`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6418a24afec5c30f1b4e609f196c0de753f9a8e0c56a12bae18732fd086832`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 734.9 KB (734935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bedd4822b507cb40ebfbcd1328022afc7ce5c839f353a5d7bebee00f367835ec`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f677eb87304cd74f3821d282a00f9c0cd6b4a6ea767d4b8537aacd6106c09`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:781dbf5ecf0c5a65a8c77f473c8c360b44f21408232deccae24abfaf2d1e86aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6246187fd155887e2612892b3299955ed5aa5e72b2bd8f4707c1f7b3a05cb74`

```dockerfile
```

-	Layers:
	-	`sha256:29e1aec381c8a1ad09bfd2c1ac62beaf6f0a23906dd3a96f465500209dcff6c9`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 2.2 MB (2157791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3056a97ef4c62275e5fe7c81289b256c70f367a46c4c049118bdeeea43e44785`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:f1d0220bbd4bff98fbc04df042e0a4a93eb3353969fd81451a4fa2dacaea9121
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72539219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:222b7e70e02769139002533b8eed20848291be6a79a195df33b4af6572aa805e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce0d04db17a73ca3a7314b885207e80120682c8358368a9254c7f44a7aa2761`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 13.6 MB (13638339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ddeda1f976085a87139c58582b31ac5fd6fc3c900259b39f3163e64bea4ce`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bdf2404f235a46786918527ccb15e5da315bc30edec03f1a23a4d5adbb837c`  
		Last Modified: Thu, 08 May 2025 21:26:22 GMT  
		Size: 19.8 MB (19828990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29e5bd26390c9927b9d705940595b9ccb503518764174068193050a9ee011d3`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837c695d5bcef73c8dfd7be97d8f030b294d365c39fb1ef21f5aec9cebaf695f`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c641fa2ea58cc5073a3f4a40452af3766d1d4eff239fa9c78b7850e692b924`  
		Last Modified: Thu, 08 May 2025 21:56:54 GMT  
		Size: 31.6 MB (31637949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37037a8ef7c2de76decb659167cea10b45dd38661222354aec54af534f7f90e`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff86c18eed79c10a74d1197522cf42536dc5aa3ce2170357d05e02d5ba84c0c4`  
		Last Modified: Thu, 08 May 2025 21:57:31 GMT  
		Size: 735.4 KB (735449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd4f0ff217807d5b30a72934277fc9952e68e9ee30ea34fe04850b4b7ab9fea4`  
		Last Modified: Thu, 08 May 2025 21:57:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18e3198c4e68f19d71e3441f578b22ede80d1a52712b6bdf192f07f918b47289`  
		Last Modified: Thu, 08 May 2025 21:57:31 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:7b3bc576d829e985480ca4675791c8528a783a38c4d371d57a5db2fd2687190e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90d4f6125a9f566a7bec16427f5757c887d1d5805d2e260f441e0feda3533f1`

```dockerfile
```

-	Layers:
	-	`sha256:69d3a2ca596b8cbbaba446202d30bce8b29c35c2caf834248bcb764d1950acce`  
		Last Modified: Thu, 08 May 2025 21:57:30 GMT  
		Size: 30.3 KB (30296 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:843caff2b73baa15c0505e65e3f04e4ff217c519d3fbc60bb1dc04cd95611bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69548231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b852728a94503226eccd2cf97ccb9bea1fbbd675e4404e5b4888f06410820929`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae53c42a3a934e2af6db5b115410a7b4c6a02cd2b122d00b65d1eca1a41169`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 13.6 MB (13638357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10142d79ada8bf8b882c44da37430c2d14e535a18518bf2925f9f960b71e79`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfab14bb194eab55e2e70f9afc13ee33e4dd21aa21350e1374e86f05fb626af`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 18.8 MB (18755156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da76f291cb0bcd5dc8fc90d909e92ab04c17a7553ef5146ab7e325af2708443`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d3e5b7d935e85e9b31895bd1360c16fb666b189cce4d62af34133ff180412`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df80c80dab935ac507aa56dc704c0803d9d2fcf950397319075ec118fc80934`  
		Last Modified: Fri, 09 May 2025 02:56:40 GMT  
		Size: 30.2 MB (30185429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c3a1b4fa684906875f7fd4416d71426ac1aee26864470455b1b9b46d7828d`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad98b7bdd963920e8d2aa877c61dd49507e014c29caef2cbb1d30e7d8bcbb220`  
		Last Modified: Fri, 09 May 2025 02:57:31 GMT  
		Size: 726.0 KB (726042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184d338f49bf9a83a431fd1d913ec8455610f26e653cef26bf7c21f34b2000ec`  
		Last Modified: Fri, 09 May 2025 02:57:31 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3966652bdd05ee23d88589676e565d4d5f020a8ebddb3f96739160af838aa5f8`  
		Last Modified: Fri, 09 May 2025 02:57:31 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:93da9c0ff3bc3869f678d2eeb4cb4eefcb8ca836a4552bbc1a832c4f87f6d3e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce05f151ef8fa03c431fc55b987175152896213bd854e7f0f64aa3dea0ece08d`

```dockerfile
```

-	Layers:
	-	`sha256:7158e1e22f933e338ead7cddeab5933b9173e532a02c5999e0cb2b40f6fa61e6`  
		Last Modified: Fri, 09 May 2025 02:57:30 GMT  
		Size: 2.2 MB (2158107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9f0af9c466c635886e2fdf1663e222e60291a54a101b2146fd8246cf4db82d5`  
		Last Modified: Fri, 09 May 2025 02:57:30 GMT  
		Size: 30.5 KB (30511 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:80c6806a01bb51e046a5c59782505c112a8298724b9be9bc6596c8177bf3a3d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74266782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4d646a711ad6c20781e47bc4ab0effd6c18e879587de32375e70188b27b5b01`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752b27585c21531ef183f9331718681f7d5a399ad1721fe17bf65ec91aa026d`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 3.3 MB (3332291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c504757a74563c6c69cb5f5ab95d450088933adf663323509ef07a437fda44`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64969c8e6dd0ea68ca6e1a455172bdc1ce583b5d543fc3120d33f200e06302a1`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1176f7a4c5fb0e54724b9ad7ea378a6420c35cbfd4d0eeb5e1fef5d9ba7ac`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 13.6 MB (13638372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9788910834fbf94207a3e2b19ab0e6fabbefd4e42d621687e321a1db2f16e53e`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edad5b9c93eee4f4366f3ebeb11225c8f73a2b77b6f9619550727373b01d51f`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 20.5 MB (20506682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aad88073420d66b54ab164736e4f80b7f83ed7afde64e75da65e76a0601f38`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d8baab457dd5125f7b8056acc97da76b6e4aed76359cef6cf89c1be2f9546`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9518d6339aceaab8bbfa04cb293db8787e29591ef024e80b24a882a2c9c8edc0`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 32.0 MB (32036745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e197ccaccec2cf61efc3cdf266d9ef310f66d8e5905a95466247bdefc08c5d4`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041339cf3b7765f89f7a06a66d20ca4f514beb477b3de1192434100f1458eaa0`  
		Last Modified: Fri, 09 May 2025 01:10:49 GMT  
		Size: 735.0 KB (734969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997ba3edba8f59b1e754c8ce9417774952b4b26c318f9ecb09bd8c7f93c61c50`  
		Last Modified: Fri, 09 May 2025 01:10:49 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccd51abf26165bd0c932ddbe8e40b0ce8db2744fcab439ed3294ced22fd0542`  
		Last Modified: Fri, 09 May 2025 01:10:49 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:c23808e709498a8ce66df1019fb44e1b0c7e13f73451488586b20acd8e2049c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f80761ada1db9def1d994d5056075162af38e85724e76cdf3f5060152676b1b3`

```dockerfile
```

-	Layers:
	-	`sha256:1cd9c65c85a18dc9f83007c5b256b7f0ea90f355d240d3a8553e4a2d37ce48d4`  
		Last Modified: Fri, 09 May 2025 01:10:48 GMT  
		Size: 2.2 MB (2157931 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8b4ee9180576d731ede0860a4be552d16258ca83570df0fa58dc2291dee01a0`  
		Last Modified: Fri, 09 May 2025 01:10:48 GMT  
		Size: 30.5 KB (30539 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:09d738d324e7358e8718b5f7ea57a746f4dc3f339ef155de256642a69f8bf96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75152758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2f4cf43e33194338ba615dd880ce527a12b8bf8cc1d3717b49f884b54f4e9ef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0fee7f3118a5985c2f626fb5b6c58f3e09615e2d0e574b152efa48b96dba0`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 3.4 MB (3379885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0859e481ff1d593c72d70f1d40018ee891c8a85aed61e584093925eef0bcab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b986eab8e8b3e0184edeb69c32c4ed3d8588e109c815e0849b82bb054cacab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7b75ef5fb8c211e5b9a329554b4301d5c6eb7ae9c8b76dc280c611f52936f2`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 13.6 MB (13638340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbb0139bcece2c1bb61243f10b29ef44dfb0038edd4f69191a281fb8695da3`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6161bb22ced62e09258a8f26973e62bc0c0b3f09f6fd571bc8cbf3d57d556`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 21.5 MB (21479578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe4c701feaead74489728c530e52569dea2bd050f15b4c2465b658466d6ea38`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aa3b4dea6bd9bd03e0d1ad21c8a068d7303cd61d25541395be92f12129e0a8`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b4c02adc0a7effcc443a0f23a7c458bd7f373f594674c85c29612e9b69169d`  
		Last Modified: Thu, 08 May 2025 21:49:16 GMT  
		Size: 32.4 MB (32419677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164b10f1e3fecdfcbdca38c262d211e9cd19e5376602d901c2600a1fe993cfe0`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dda5b9695333e447d0a7c4f4748401a2b79c927d5727ef067a89fc3793d3b56`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 746.8 KB (746768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeb0ee3f2a513ce981f6712da1e294d7c48715a362dfad8a291bf65215aa3c9`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90f677eb87304cd74f3821d282a00f9c0cd6b4a6ea767d4b8537aacd6106c09`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:1f92cfb504783646a2881a10fa7ca7f1e57ead3c343c1d592d7a0ef3b993cbef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9983cf8038dd45e163f112e08e76a5be7b26595d4eff4efbcd99f3c694ebf572`

```dockerfile
```

-	Layers:
	-	`sha256:5ca4157a8a328c2af7d6546f9a59399fc40bf9240afd4854f5a30942b6a31070`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 2.2 MB (2157579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:172e20d08c1bbe37ffcfc9a10f1ff2d6234c75117b69d20e9d2e124b38efd69a`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 30.4 KB (30386 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:424ffeccc9c2c70b1cd6d922530446b3b90a177250b0e46d4adb33bcc5cb218a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77133893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d5edab6a4ff0ec5edbbbe7c8110874b686f4cd43a660e9db7555bf574c10792`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e76c061ea4a5ab1435512c8388fd08bd714f08a20a3d13e20958322c1e38c8`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 13.6 MB (13638361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6741176fa79481125f0168dfab2269eb4d272b50ffffa3eb93489fbac4b7e`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baaae08012b74873c8e9eb084b4c040c29cb1b207bf5a13250c34c0533cab9a`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 22.7 MB (22698151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d926e7ce8969775d3b04d34e3a2c99bd3026dadb90880f40e22812f538d9a0c0`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01319ff876f0a90f52b88a0db82b4f34546c97612dc4988123adb15a952cee`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749a6c3d45b6e53322f1fdfcdeff037de2cd648813a8db706c3925473d004f6`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 33.0 MB (32975132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c502c29ed2b1ba6e7fd2c2aa71175f396a9176edb02e55648b6cf8555189787c`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a0bec688c7dcf453766099c15c3b8da2376c512ad069fa63310d5cb9cc82ba`  
		Last Modified: Thu, 08 May 2025 23:20:34 GMT  
		Size: 742.1 KB (742090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197c235d1d7b2fe242ac49ac0dd27c934595e0d2c297a3abf793b3f7d89013d3`  
		Last Modified: Thu, 08 May 2025 23:20:33 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fc8c13c7d766dbb43871c48ba842a9e8afca0c04966e794d3085f85fdc4880`  
		Last Modified: Thu, 08 May 2025 23:20:33 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:f0f835d0ffedfb730941109b859c5963cd3860254b2247966329c3a531a2b50b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:993b97a7bbbc6ef55f77d59cbc70d01f9f14ea1e935c3488063374fbbe7b0b18`

```dockerfile
```

-	Layers:
	-	`sha256:3beb8afe05752b3cc2fef829b05837c9a529997560a885e3bcf0fc2d08f38ace`  
		Last Modified: Thu, 08 May 2025 23:20:33 GMT  
		Size: 2.2 MB (2156348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6c0304b62dfebf2eac13965ccd918bca1a2b76d7d8cb6f9ff0b914ab0a6381e`  
		Last Modified: Thu, 08 May 2025 23:20:33 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:1c1ee0042173c923770d0e23e6bde4763120d5e18e712f08c90fac69c0d3e732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73417077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53beb463b1f33e7b81cec41725633e81740c4680945ad53a4694aeb7c452e352`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db7ef0a049248006688e39882ca6ced21701e3d55e7cb2f43eb10572e33c7`  
		Last Modified: Fri, 09 May 2025 01:02:09 GMT  
		Size: 13.6 MB (13638347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ccd5673892b28566480f109c15f00e40dac754b53ccd5b997b3b0f7f75b66a`  
		Last Modified: Fri, 09 May 2025 01:02:06 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0f3c897c5b22a06c34b5e67cc4b30c94cf9e55e8b3176d9f4c5f0408e96f1a`  
		Last Modified: Fri, 09 May 2025 01:02:10 GMT  
		Size: 21.2 MB (21162501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef46c091109b0dad546606ab5e3c6ab60d516a7707483f98fa96053dcda29e`  
		Last Modified: Fri, 09 May 2025 01:02:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b931b251640e1d77e3e5386e76828941f021bb5b7fd085a60db7df564d2db`  
		Last Modified: Fri, 09 May 2025 01:02:08 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d591c20251c0df6262a43882dff69cf24f872cb167d9bd70dbe59ce535d6090`  
		Last Modified: Fri, 09 May 2025 16:04:38 GMT  
		Size: 31.0 MB (31044006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56519a808e922477caef5d3ce688e3619da9f0db1b63ff8ca95f3204fd8facec`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027191c585b4f9bbf18caa4794ac5f797b5a97ec36ad1784bc38f9f09090f1af`  
		Last Modified: Fri, 09 May 2025 16:09:43 GMT  
		Size: 733.1 KB (733139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22937d96cf5fb511c65f446d5d98f1aa7e4bde29f13ca21bf1b2e286d2f0f75e`  
		Last Modified: Fri, 09 May 2025 16:09:43 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37cbf32a3d34fe8547b6abcb834f1d4489ed95fe123a474aa51637645a800b1`  
		Last Modified: Fri, 09 May 2025 16:09:43 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:c6582f375eb9c9b2286b9b9b49be48dc9646f381a771347bbc8acb2803319078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6394f221a0ab1860afcb6593842a126ca3b269ce7df49d3e3f97798e89760615`

```dockerfile
```

-	Layers:
	-	`sha256:190c4740fb044750cd91a35e45e3ad39c497ec94216e7f63755deff53ec3eac4`  
		Last Modified: Fri, 09 May 2025 16:09:43 GMT  
		Size: 2.2 MB (2155290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a278b93dba2daada9e316b2788eeb927df0c370186a31232feebf23775be385`  
		Last Modified: Fri, 09 May 2025 16:09:42 GMT  
		Size: 30.5 KB (30459 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:196413d261e36c6d32f6a1b7e488c9b0e7421317149953ef15fcb0fcba922fb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75390492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8429b1a6f22e8ba761457c5c21bbaa6a6affe86ab01a8182cc08ee91cc30494`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=1.10.27
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b5f11089bad6dd57e7f9c626829578bab2c83d4a9d3e6c9dd1c73eccd0d96`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 13.6 MB (13638363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925304c10005fd175f8945f9b79556931bf8772002494541acf614752b95348`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbdcbc01a58fa9ca47c12882f0c582c63ddf71a40fbf79fa956decd72f0f45`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 22.2 MB (22248891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234da8b1110c7fe66f09e4181941a3db5f83769849d61bd62db5481617b0183`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e59c13cf761428c460597e931fe7482a363b6b0afb29d60205e1fa1bc0d234`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da82aeb01a0294d366bfecf08eef375887e0728de96b73baf2f614fc770d6ee4`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 31.7 MB (31706531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47454c44bffd2e898699df83390dc5586ecf0cdb8cf4e637dfbe6e862166142`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7c1f60d28958552dd5115e8a939ee09597c03bf544b0246cfb20eec9b25ba3`  
		Last Modified: Fri, 09 May 2025 01:21:05 GMT  
		Size: 738.2 KB (738232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07989b8e7844e52f9ba59d42bc09551bb7338b0eac68433e6585127a119b0e5`  
		Last Modified: Fri, 09 May 2025 01:21:05 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:929a49085ad3c137c6b1d488d8122e4179631269e5d564454c4f63d8a7e4ecbb`  
		Last Modified: Fri, 09 May 2025 01:21:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:2ada178a5e2553396e880950ea7a59e890a59379ef244e1dc5ba1b628f5cdcf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd05a2973df0eb021fe768f352d8127e203db74c48984f8bc75494e1af8fc9bb`

```dockerfile
```

-	Layers:
	-	`sha256:a3283ddfd3dc52b6f02f2d11b1454443e9d0fce05ca2a2d23e5e9427bba08f31`  
		Last Modified: Fri, 09 May 2025 01:21:04 GMT  
		Size: 2.2 MB (2155076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:328713a09f398eeca2d5a0a8169e4da8e06abf6184564cf66fb87e8a75e3d405`  
		Last Modified: Fri, 09 May 2025 01:21:04 GMT  
		Size: 30.4 KB (30416 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:3df281ca83119bff1332f0f5f311960cb16b99238f8273acd965be6bd508aa8e
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
$ docker pull composer@sha256:ec31187cf6de8fbb71d2c493ec704f5b76955a3090b3295adf39f0fd5d1eb479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74513054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539808e605ec8fdd3117a80817d3e99ce4af0c3c34ca931e8f23e5aeeb22aea7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ec51de1f9773447b65e97f0c677dfa7c2c5a643a8e29c2573fa02d440be485`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 3.3 MB (3339405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f347299a473f0f5d9b5f088e95e92fa5f3fdb929eb8c00e8eee8a5e255fa22`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33c8191db1484b005c5fa5405a7076bdae4e90319fa99dc126e7fc70a360264`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a488374895485209654e2f20371d2b15edb0b1e6e389ec7439903ae08bb34`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 13.6 MB (13638342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242d92ffbbeeb68a81285f10e04caea376e536af932c229bac24f4850ead8549`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5f8d392c5efc498dff46eaccd969d3b99752dc1a40cbdbefd63ae52351c93`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 21.0 MB (20961727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69de2e680c8502b2e77e5bfbf4a6121b21f9356fa9b0058eb0967c21456bad`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d926e2db98107193f77ac67f3ebac3c923c205841b5b20f0a86e5c848b2d66`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f35e65c467d6a06e463158b71b59b394f945292ceb3f5085e55d3ef27a4da9d`  
		Last Modified: Thu, 08 May 2025 21:49:23 GMT  
		Size: 31.9 MB (31932834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07970fc96919497974b26ac2861318973a76e07ff79f1b64faed95d351083da0`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa5aa8beb42ce23af82c206ab0a95fc0b8426daa93031c684e7d7da64f5415a`  
		Last Modified: Thu, 08 May 2025 21:49:23 GMT  
		Size: 973.6 KB (973600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98df5a35c2fe3e9c05282183b08d8ceb4ec343e2479353c3d9632a64d7e49b6`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67885e2977d33ff647e990ab306798d84593f91d0fb665528f08b8fbaa1ac723`  
		Last Modified: Thu, 08 May 2025 21:49:23 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:1f0f50d68f9860890b7bd409b5b76951479c5c14b8ed9eab06f2c305a52a3a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2d8618c9ebce7af590de1125a08b17d5973e1daa67d8ffe3ee4c3a288764dc`

```dockerfile
```

-	Layers:
	-	`sha256:bfbf90c8d1e9be23a21546ffe91ffc2f2f50be40041df99c9c75cb1b6811922c`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 2.2 MB (2159285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193dd9351255782fb765b8209163883befcc28d1c1b5707d7382f9976ef17dc5`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:a7dff16e0bdc5c9bc5f24d80b850d263b206479078e2c883dc13d4142261a237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72777249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cf8efc80624ecf1ae3f6e2946b2059cebcc02c496ccc6963754e090488fc16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce0d04db17a73ca3a7314b885207e80120682c8358368a9254c7f44a7aa2761`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 13.6 MB (13638339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ddeda1f976085a87139c58582b31ac5fd6fc3c900259b39f3163e64bea4ce`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bdf2404f235a46786918527ccb15e5da315bc30edec03f1a23a4d5adbb837c`  
		Last Modified: Thu, 08 May 2025 21:26:22 GMT  
		Size: 19.8 MB (19828990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29e5bd26390c9927b9d705940595b9ccb503518764174068193050a9ee011d3`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837c695d5bcef73c8dfd7be97d8f030b294d365c39fb1ef21f5aec9cebaf695f`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c641fa2ea58cc5073a3f4a40452af3766d1d4eff239fa9c78b7850e692b924`  
		Last Modified: Thu, 08 May 2025 21:56:54 GMT  
		Size: 31.6 MB (31637949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37037a8ef7c2de76decb659167cea10b45dd38661222354aec54af534f7f90e`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d36a7b322939484d5ee5c8e4d2acf6b7e5d10aa83eba813e5aa7ca50ba2756`  
		Last Modified: Thu, 08 May 2025 21:58:05 GMT  
		Size: 973.5 KB (973470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f863439db685c5d731f58b9e7de989a88fa5b917b13af3f5f2d825a19b4ae3a`  
		Last Modified: Thu, 08 May 2025 21:58:05 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a186e1d7e7ee9e9772006a97e08806d1e5b4089ed1161b0a7cd6e680fa291b`  
		Last Modified: Thu, 08 May 2025 21:58:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:5b47eb452f6d117c416ce8d5e3a6c87296956ef588e545df40795678b3928543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1083c9aa6c3a0ee50d5c3c12d77d92fc773c9f801866daafc72b1de2f336e464`

```dockerfile
```

-	Layers:
	-	`sha256:3e1e0b06eb56f368894bce8fb4cb9415ad55c94f2959e12dafcfd14f064a3f50`  
		Last Modified: Thu, 08 May 2025 21:58:04 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:b14aa8913a1e62db51a228506079460ce6e2033447ed821db51e1762fa8776ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69786310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12189a43195c725265f01f4a102edd3b5c363094476821180a6e4aada55df9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae53c42a3a934e2af6db5b115410a7b4c6a02cd2b122d00b65d1eca1a41169`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 13.6 MB (13638357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10142d79ada8bf8b882c44da37430c2d14e535a18518bf2925f9f960b71e79`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfab14bb194eab55e2e70f9afc13ee33e4dd21aa21350e1374e86f05fb626af`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 18.8 MB (18755156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da76f291cb0bcd5dc8fc90d909e92ab04c17a7553ef5146ab7e325af2708443`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d3e5b7d935e85e9b31895bd1360c16fb666b189cce4d62af34133ff180412`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df80c80dab935ac507aa56dc704c0803d9d2fcf950397319075ec118fc80934`  
		Last Modified: Fri, 09 May 2025 02:56:40 GMT  
		Size: 30.2 MB (30185429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c3a1b4fa684906875f7fd4416d71426ac1aee26864470455b1b9b46d7828d`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0df7a4b2868d4940542adb230523d1e4ed001e3b81e5b207cecf42c343f478`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 964.1 KB (964111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b73a1fcb61a5a282a8c9397a8c576b45fbe6caa25857e13ea650cb4d76322a`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef7526f5b3917e2bc638427511d4989ad3248fae4b127cd3e0d33e74a490514`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:4085cd69ad186b4f31b2d00827f60d3f772d59734d0e19d4d610951d1ab3da6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463b46d8bb3fa777b046df54e8e2a1c586a9ffd3aa84723d00aee9899233ec16`

```dockerfile
```

-	Layers:
	-	`sha256:97eddbfc009a7db168669d971a6e5e733e0fc7795c4e86ab74ef4c3805df0df5`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 2.2 MB (2159609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6143674f1e33328ecad90616b50233ba90952a12cf467628257ba949eb7dd771`  
		Last Modified: Fri, 09 May 2025 02:58:18 GMT  
		Size: 30.8 KB (30808 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:3eb81b210445eab75a9596c806a3723d0154537ffbea44e924dd375bd8d46ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74505054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cc127439d34c6f96676db2c801e18e32fe42a8f19167bee613e3cb32a8bdf8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752b27585c21531ef183f9331718681f7d5a399ad1721fe17bf65ec91aa026d`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 3.3 MB (3332291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c504757a74563c6c69cb5f5ab95d450088933adf663323509ef07a437fda44`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64969c8e6dd0ea68ca6e1a455172bdc1ce583b5d543fc3120d33f200e06302a1`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1176f7a4c5fb0e54724b9ad7ea378a6420c35cbfd4d0eeb5e1fef5d9ba7ac`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 13.6 MB (13638372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9788910834fbf94207a3e2b19ab0e6fabbefd4e42d621687e321a1db2f16e53e`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edad5b9c93eee4f4366f3ebeb11225c8f73a2b77b6f9619550727373b01d51f`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 20.5 MB (20506682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aad88073420d66b54ab164736e4f80b7f83ed7afde64e75da65e76a0601f38`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d8baab457dd5125f7b8056acc97da76b6e4aed76359cef6cf89c1be2f9546`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9518d6339aceaab8bbfa04cb293db8787e29591ef024e80b24a882a2c9c8edc0`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 32.0 MB (32036745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e197ccaccec2cf61efc3cdf266d9ef310f66d8e5905a95466247bdefc08c5d4`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63caa9b8a6f65f98bf399b6c0907858c28d179a339fcecce75876a27f8711118`  
		Last Modified: Fri, 09 May 2025 01:11:24 GMT  
		Size: 973.2 KB (973231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c61d014799dc6bf76eb35626076e710fc5e4dda0e4843cb4c5654377f2392d`  
		Last Modified: Fri, 09 May 2025 01:11:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d41ade31de22ec89775e848aa31682bf031124c7194426184d23e224ab3621`  
		Last Modified: Fri, 09 May 2025 01:11:24 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:6e3b0fecd14009a0ff39e9f8ce6e612b0954f575c01f51f0989e4e62849bc904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac85c03c9804fea2906b6da84c95a285730f93e6e58ea7b21c85819ef99cbad`

```dockerfile
```

-	Layers:
	-	`sha256:9b88aeefeff43c9faec75bbdf559e9d233e3f8a104137975bd17b3c8f38e575d`  
		Last Modified: Fri, 09 May 2025 01:11:23 GMT  
		Size: 2.2 MB (2159437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d477695b3b116918cd550b0c4d81ffbfdc9142b846a0ce5cfe1a10827574c8`  
		Last Modified: Fri, 09 May 2025 01:11:22 GMT  
		Size: 30.8 KB (30841 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:1b5e00fff273c7f8077e9e7e091ee6a8544ca4527c32b4e19652ad679af027ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75393539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b1a4ae43abdf7f81cb2fc374621656b152c7f70595cad0a364c16bbc20ea8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0fee7f3118a5985c2f626fb5b6c58f3e09615e2d0e574b152efa48b96dba0`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 3.4 MB (3379885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0859e481ff1d593c72d70f1d40018ee891c8a85aed61e584093925eef0bcab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b986eab8e8b3e0184edeb69c32c4ed3d8588e109c815e0849b82bb054cacab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7b75ef5fb8c211e5b9a329554b4301d5c6eb7ae9c8b76dc280c611f52936f2`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 13.6 MB (13638340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbb0139bcece2c1bb61243f10b29ef44dfb0038edd4f69191a281fb8695da3`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6161bb22ced62e09258a8f26973e62bc0c0b3f09f6fd571bc8cbf3d57d556`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 21.5 MB (21479578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe4c701feaead74489728c530e52569dea2bd050f15b4c2465b658466d6ea38`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aa3b4dea6bd9bd03e0d1ad21c8a068d7303cd61d25541395be92f12129e0a8`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9d3822fff04ee88d265cf3b2f6fda0935618827f02ccb83caddd149472bfb6`  
		Last Modified: Thu, 08 May 2025 21:49:18 GMT  
		Size: 32.4 MB (32419790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4749bed490bc2e21ca8b7e67d7dca5701af7d8733ff3f555fc28be07dddf67d5`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8991ac628ce8adf7b232be49fdf5f393c12b8036a374619747aa07d1191bf1`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 987.4 KB (987427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67722e7ebd67ddc3ea5804cf2081f36d6624dfd689578ce547276b49702f80d9`  
		Last Modified: Thu, 08 May 2025 21:49:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791cac75c2ce2bdf945782129c08f92674bc6ebae72272ad6dd7372877bd7ca0`  
		Last Modified: Thu, 08 May 2025 21:49:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:38527cd7533c5a71d0bd5adb953746455b3cd43bd38d79e7538ef1d370d857b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22fec3f1104eee0cb88dd02a43136b15cafd5ea020c4a31e3d1d3204f2b2425`

```dockerfile
```

-	Layers:
	-	`sha256:22a0fc51722a9f887d0d979027ed22915615024058d3bf602b7e93f1546298f9`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 2.2 MB (2159068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1463be1cdff852ccf958d429ad3373c183fa577d98d14b778a8846e47cf76edf`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:8b89c42c4af0e06aefd095dbb34c2619855dac845cb2a01d188b3a77c4bb5d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77372105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068ba4fd3895e50862519de9921b88288ba5328fa9baeb66de3c2f38c5387bfe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e76c061ea4a5ab1435512c8388fd08bd714f08a20a3d13e20958322c1e38c8`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 13.6 MB (13638361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6741176fa79481125f0168dfab2269eb4d272b50ffffa3eb93489fbac4b7e`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baaae08012b74873c8e9eb084b4c040c29cb1b207bf5a13250c34c0533cab9a`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 22.7 MB (22698151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d926e7ce8969775d3b04d34e3a2c99bd3026dadb90880f40e22812f538d9a0c0`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01319ff876f0a90f52b88a0db82b4f34546c97612dc4988123adb15a952cee`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749a6c3d45b6e53322f1fdfcdeff037de2cd648813a8db706c3925473d004f6`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 33.0 MB (32975132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c502c29ed2b1ba6e7fd2c2aa71175f396a9176edb02e55648b6cf8555189787c`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0684f605738b7e5978c5a350d7cbb9885d6e9593c7e5eae0ddbc6ce32c02a22e`  
		Last Modified: Thu, 08 May 2025 23:21:27 GMT  
		Size: 980.3 KB (980290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3865705398f20912aedf7e8109210983ab47fc0c7862afae8288b244efbbfbef`  
		Last Modified: Thu, 08 May 2025 23:21:27 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f2b0dbc52dd18eb4223fdbf933144b2bf9e6aa6dcc618cc87532424c5aa68d`  
		Last Modified: Thu, 08 May 2025 23:21:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:8f25a18ddac3fff471eb1d915aa6b545fef585f2ef4a0c6d6ad5937a012071ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5311e03457df6c7d776932408097f223757d845b04c0928ffacab82f34f399a6`

```dockerfile
```

-	Layers:
	-	`sha256:2d792c31a36378da39476236ad13355e8d2ac4418b7aaa84c3bcab1e1a9bcd08`  
		Last Modified: Thu, 08 May 2025 23:21:26 GMT  
		Size: 2.2 MB (2157848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044e4e017f6b8890a5b64a606fa7abbc89bbaf0beae880d8c34c96c26276b056`  
		Last Modified: Thu, 08 May 2025 23:21:26 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:6e9ec48444ac9558ef69eb1c9f824baf5314522f44538a49e4733ad1b3cd30cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73655710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420af2fb4f88c27b8de5e5a3cd3978d65d51761075b4d2e02e117800af46470c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db7ef0a049248006688e39882ca6ced21701e3d55e7cb2f43eb10572e33c7`  
		Last Modified: Fri, 09 May 2025 01:02:09 GMT  
		Size: 13.6 MB (13638347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ccd5673892b28566480f109c15f00e40dac754b53ccd5b997b3b0f7f75b66a`  
		Last Modified: Fri, 09 May 2025 01:02:06 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0f3c897c5b22a06c34b5e67cc4b30c94cf9e55e8b3176d9f4c5f0408e96f1a`  
		Last Modified: Fri, 09 May 2025 01:02:10 GMT  
		Size: 21.2 MB (21162501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef46c091109b0dad546606ab5e3c6ab60d516a7707483f98fa96053dcda29e`  
		Last Modified: Fri, 09 May 2025 01:02:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b931b251640e1d77e3e5386e76828941f021bb5b7fd085a60db7df564d2db`  
		Last Modified: Fri, 09 May 2025 01:02:08 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d591c20251c0df6262a43882dff69cf24f872cb167d9bd70dbe59ce535d6090`  
		Last Modified: Fri, 09 May 2025 16:04:38 GMT  
		Size: 31.0 MB (31044006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56519a808e922477caef5d3ce688e3619da9f0db1b63ff8ca95f3204fd8facec`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ed4acbc6167d6e65bd61a656d64ead373ef36f1602553fbf264731bfa550c`  
		Last Modified: Fri, 09 May 2025 16:15:00 GMT  
		Size: 971.8 KB (971762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04c9848bde98f1cc4f6e54f5b1c32bc5ba6cc29936f7c082af8d2a54e898813`  
		Last Modified: Fri, 09 May 2025 16:14:59 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7822088e7ffa14e2fabd2259297ef14419e9c93f94af3f4eff289969f1b934`  
		Last Modified: Fri, 09 May 2025 16:15:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:da09a3427cf58ee280cd57b40273df9437aead71dd19144d48010936605c4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d48ba38d8d40fa452f8a26f25e490ec24255f7f8c6e719b130360219859b2f`

```dockerfile
```

-	Layers:
	-	`sha256:7a2527bded2278ba5d2f827638d12324fe5fdeb391d080e59130442d5ebe9735`  
		Last Modified: Fri, 09 May 2025 16:14:59 GMT  
		Size: 2.2 MB (2156790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc040a825e20bb854175bac49728f383c6830a0b9c00ae1216afa7558fcfc0fd`  
		Last Modified: Fri, 09 May 2025 16:14:59 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:dfc7fc645d6a07047a78073623daf44350935a34c1c8566c5dcb95ea1ee9228a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75628873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94efc800e610253d603808a8925143397964e88a27a64a89e35a572b016c1201`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b5f11089bad6dd57e7f9c626829578bab2c83d4a9d3e6c9dd1c73eccd0d96`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 13.6 MB (13638363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925304c10005fd175f8945f9b79556931bf8772002494541acf614752b95348`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbdcbc01a58fa9ca47c12882f0c582c63ddf71a40fbf79fa956decd72f0f45`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 22.2 MB (22248891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234da8b1110c7fe66f09e4181941a3db5f83769849d61bd62db5481617b0183`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e59c13cf761428c460597e931fe7482a363b6b0afb29d60205e1fa1bc0d234`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da82aeb01a0294d366bfecf08eef375887e0728de96b73baf2f614fc770d6ee4`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 31.7 MB (31706531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47454c44bffd2e898699df83390dc5586ecf0cdb8cf4e637dfbe6e862166142`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d135b86d58d8377467d55bf776e53000abc3b9d4bfaed27cf9d02c772ce5d0`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 976.6 KB (976603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed9f8099552b00200734259e0b36ab4f94c39d36a77e29f46335351783611e7`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dd9dc76f2c0e4b853173a0da2d6ad8c31b58983ecf0c6dded53de8ad1eadf4`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:2923462ef720cfdb712a7c14681218303b60eb1a65b653f0aa292525ac745924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c62a52a3b3a37c11a1613f5091cac4f0aa9b257b133215d731a3f11e79cb27`

```dockerfile
```

-	Layers:
	-	`sha256:ed73a17c8aee94540dd474fc24fb314abd3e712e9df24917150e0160a6d5839f`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 2.2 MB (2156570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967ce814b657814077f50f73fb82037f671822aeb253504f07e43bf74fc2a3a8`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:0d9ad23e2f335bb8e56e259a26626d14ebad2d877a443142187c01e66333682d
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
$ docker pull composer@sha256:5cebd857e3ad2565b6c39e018c0a65b3a66fbfbd6fbb58740b2ce788c39f249f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74359139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231c9f515480b892e0000d9402534862e6fdf23cebe60072d3a2c64fd0859f3e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ec51de1f9773447b65e97f0c677dfa7c2c5a643a8e29c2573fa02d440be485`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 3.3 MB (3339405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f347299a473f0f5d9b5f088e95e92fa5f3fdb929eb8c00e8eee8a5e255fa22`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33c8191db1484b005c5fa5405a7076bdae4e90319fa99dc126e7fc70a360264`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a488374895485209654e2f20371d2b15edb0b1e6e389ec7439903ae08bb34`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 13.6 MB (13638342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242d92ffbbeeb68a81285f10e04caea376e536af932c229bac24f4850ead8549`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5f8d392c5efc498dff46eaccd969d3b99752dc1a40cbdbefd63ae52351c93`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 21.0 MB (20961727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69de2e680c8502b2e77e5bfbf4a6121b21f9356fa9b0058eb0967c21456bad`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d926e2db98107193f77ac67f3ebac3c923c205841b5b20f0a86e5c848b2d66`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499b35e2befe9a2ab9280b1a602e52457d8ed7f23a90e28ba5c103070decea90`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 31.9 MB (31932681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fb4c279258a28b8cf2f050d72d484d11919bd0c4c3ce9275900c07678241b1`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daa442d79abf31d10e17f14740f25bc7f61abff47dc00e1100471c6c0ab7731`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 819.8 KB (819839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2caefd19b6125c0e3b24e00ee848ae2ef85b2d4cc231044b55e28a7a1052d657`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28726ab0de7dc427015158d773cd922bef15e82c8e80a12f7955f42824dcd0be`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:c72c8e096b9c397677aa31c340536654a174b6044f2c65edffe768a9fcdb81f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d7e1497fea47c02d1e9662679efc0af0be65bc38ee751d93c6c03cc0635c3`

```dockerfile
```

-	Layers:
	-	`sha256:23a61df6af22091ccd1fe95b53e017a7c279324770176b85f12aff52854b8acb`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 2.2 MB (2158991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66264756f1845409e67c618f4a4ca8168ea6639f52322b61ed8c8fb05415ca91`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:4172dc3dc33e54a3baecc3587408f2221e194b270edcf1478b855668a54403e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72623422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e19f9283237934aa53cd3933057376364e6d090563214f7a4ed7c49ea76a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce0d04db17a73ca3a7314b885207e80120682c8358368a9254c7f44a7aa2761`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 13.6 MB (13638339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ddeda1f976085a87139c58582b31ac5fd6fc3c900259b39f3163e64bea4ce`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bdf2404f235a46786918527ccb15e5da315bc30edec03f1a23a4d5adbb837c`  
		Last Modified: Thu, 08 May 2025 21:26:22 GMT  
		Size: 19.8 MB (19828990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29e5bd26390c9927b9d705940595b9ccb503518764174068193050a9ee011d3`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837c695d5bcef73c8dfd7be97d8f030b294d365c39fb1ef21f5aec9cebaf695f`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c641fa2ea58cc5073a3f4a40452af3766d1d4eff239fa9c78b7850e692b924`  
		Last Modified: Thu, 08 May 2025 21:56:54 GMT  
		Size: 31.6 MB (31637949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37037a8ef7c2de76decb659167cea10b45dd38661222354aec54af534f7f90e`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371ff9c022135cc30cc8b926dc250d9bedccaa330fa7b9b49b2180d26579405`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 819.6 KB (819643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dfe2f1ed4b221efdeb64a6cae996ca1e2b81afcaf99fe70e875345becffb14`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fade42309a9a0da019a91c17d77c28a835444792b767ee061b9340a9e98601`  
		Last Modified: Thu, 08 May 2025 21:56:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:ec4d3d379007819868c36dbaa75917c97b6406d4f344ad400c65266f4ed42495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7ec15c414ca787e4ac72f051579b92506a8bf9462509c15877e043fd19c606`

```dockerfile
```

-	Layers:
	-	`sha256:335cd578e45ca45ad6ba03232eade190f053ea93f1d2ad1192b0482130aaf2e3`  
		Last Modified: Thu, 08 May 2025 21:56:52 GMT  
		Size: 30.3 KB (30282 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:a033f1b78facdd5e0a4c5572ab28a12555f6082ba945bd577e20185521f7d8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69632557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2e2fd5ef57b840623eb18bcf85fccaf61c29b60b7c294d5d40961180ff18a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae53c42a3a934e2af6db5b115410a7b4c6a02cd2b122d00b65d1eca1a41169`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 13.6 MB (13638357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10142d79ada8bf8b882c44da37430c2d14e535a18518bf2925f9f960b71e79`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfab14bb194eab55e2e70f9afc13ee33e4dd21aa21350e1374e86f05fb626af`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 18.8 MB (18755156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da76f291cb0bcd5dc8fc90d909e92ab04c17a7553ef5146ab7e325af2708443`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d3e5b7d935e85e9b31895bd1360c16fb666b189cce4d62af34133ff180412`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df80c80dab935ac507aa56dc704c0803d9d2fcf950397319075ec118fc80934`  
		Last Modified: Fri, 09 May 2025 02:56:40 GMT  
		Size: 30.2 MB (30185429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c3a1b4fa684906875f7fd4416d71426ac1aee26864470455b1b9b46d7828d`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8513c8b163ee9709e5b3dc3c4a87f1f4594811ef656312a0af412be48d9a71a3`  
		Last Modified: Fri, 09 May 2025 02:56:39 GMT  
		Size: 810.4 KB (810358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f934f90fc13c2bef368b2a479f52aede5fcc42961f5c81a7db6ff1e6c825dc89`  
		Last Modified: Fri, 09 May 2025 02:56:39 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66be4070bf8d4b80b5a8a8b70270241facc3bf78b63e4af4c22a8e567adb61d`  
		Last Modified: Fri, 09 May 2025 02:56:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:7a9fc43d076b9bda83778bd6c939613f27e5fe5df60c4dd82ec67b96ee1b1fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff36941efce39e79c925e7ca11bc454085ff33081bc3f4f4c8e1caf4f776e548`

```dockerfile
```

-	Layers:
	-	`sha256:53372f3f7fdb0d6d0a5ceb85baad3547326f5c809570f5e0e8d18d07909da27b`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 2.2 MB (2159307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cc2a070c97eb5d5bb8a4d940d24e54abe8bfe8aee9c97b3c8fb0f8eb0385492`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 30.5 KB (30496 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:660a3f96590101779bae7458cc72850e95b0798689489014f57c2f88b66f06a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74351321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1479d7d13817ee69723abf2ab0d58fb9142d8d74aad87e6e04c33b22c11a42bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752b27585c21531ef183f9331718681f7d5a399ad1721fe17bf65ec91aa026d`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 3.3 MB (3332291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c504757a74563c6c69cb5f5ab95d450088933adf663323509ef07a437fda44`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64969c8e6dd0ea68ca6e1a455172bdc1ce583b5d543fc3120d33f200e06302a1`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1176f7a4c5fb0e54724b9ad7ea378a6420c35cbfd4d0eeb5e1fef5d9ba7ac`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 13.6 MB (13638372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9788910834fbf94207a3e2b19ab0e6fabbefd4e42d621687e321a1db2f16e53e`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edad5b9c93eee4f4366f3ebeb11225c8f73a2b77b6f9619550727373b01d51f`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 20.5 MB (20506682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aad88073420d66b54ab164736e4f80b7f83ed7afde64e75da65e76a0601f38`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d8baab457dd5125f7b8056acc97da76b6e4aed76359cef6cf89c1be2f9546`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9518d6339aceaab8bbfa04cb293db8787e29591ef024e80b24a882a2c9c8edc0`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 32.0 MB (32036745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e197ccaccec2cf61efc3cdf266d9ef310f66d8e5905a95466247bdefc08c5d4`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e016548f32a92f4ca21a9b9425d229f0603e50f7331434d48433cf080f21f9d7`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 819.5 KB (819499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918d9b05ba0bc908df65d8242560fbefbfa893916fc6f79a748fd37ea31e7a54`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15dcffea100c734bb9900526c295a50bdf08a6b81c92e61e5a13114d41744a5`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:6657510496ff088eb85b663658ab399924ca08198893202c463c41b3d5e0153c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f18624eaa94a7e36971327a97cbbb1b9daca6359f96e86096b283526218c5`

```dockerfile
```

-	Layers:
	-	`sha256:83b24749f270a87ef6e8438cb57a5a675bbde85039ac32beb1265124878b6ad7`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 2.2 MB (2159131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:488da887497f8349c6b6ffa9c501688798e299f8888b05bcc32bad6f267e3566`  
		Last Modified: Fri, 09 May 2025 01:10:10 GMT  
		Size: 30.5 KB (30525 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:19ea0af1d6d1bf965c8997ebf71e2a92c1313cfe4da8c8647b813f2c0ff4d354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75239586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05421cc0f995b8c637f983dea20efd577dcb54c35443c3e98b1a8a001470e15`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0fee7f3118a5985c2f626fb5b6c58f3e09615e2d0e574b152efa48b96dba0`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 3.4 MB (3379885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0859e481ff1d593c72d70f1d40018ee891c8a85aed61e584093925eef0bcab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b986eab8e8b3e0184edeb69c32c4ed3d8588e109c815e0849b82bb054cacab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7b75ef5fb8c211e5b9a329554b4301d5c6eb7ae9c8b76dc280c611f52936f2`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 13.6 MB (13638340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbb0139bcece2c1bb61243f10b29ef44dfb0038edd4f69191a281fb8695da3`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6161bb22ced62e09258a8f26973e62bc0c0b3f09f6fd571bc8cbf3d57d556`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 21.5 MB (21479578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe4c701feaead74489728c530e52569dea2bd050f15b4c2465b658466d6ea38`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aa3b4dea6bd9bd03e0d1ad21c8a068d7303cd61d25541395be92f12129e0a8`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ebfea0ea0e34c30ea6572f9b90a6a82e0b30799b9188503151036d51972dfc`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 32.4 MB (32419650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a210db33b806b55bf805f429c9afe113595174151758714de88d5944b7601285`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040bd3ee25d7721ce0b770039cc202b97b3485095553647d8ffd0ae391e2455d`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 833.6 KB (833619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5069feb63748d630228815c7019641ca31353671475fdf0d0a501f0fcaebbd1`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89ed163134dd5463572f12e039ed75cf48686e844ba79683f8d79735a5d58b2`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:943f12c594a481ac8feb5cd7d2d84cbf3f2a9ecbe7d80ae95f18599fb2a14d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e6e873d877d21ef07a5f1b9312aa3dd3f5f4f9eb482511f8c09ec0bca70ddc`

```dockerfile
```

-	Layers:
	-	`sha256:b8481db856b3845732b38141065fb355ae9c854c682bd7c3b3c3ab9573541b12`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 2.2 MB (2158779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e205d10e14e98bd5d46cd83ddb52dd8ae5409e379edfb679a5e6bed943f031`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 30.4 KB (30372 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:72c16852f91d422eb2182a913c7a3a2c5a0446ac4ad2f2e89ecf389cdbdcc2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77218301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af02315b6b038713c7e17f053cd7610afb4fb1e720eaf246c39026433a7a407d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e76c061ea4a5ab1435512c8388fd08bd714f08a20a3d13e20958322c1e38c8`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 13.6 MB (13638361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6741176fa79481125f0168dfab2269eb4d272b50ffffa3eb93489fbac4b7e`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baaae08012b74873c8e9eb084b4c040c29cb1b207bf5a13250c34c0533cab9a`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 22.7 MB (22698151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d926e7ce8969775d3b04d34e3a2c99bd3026dadb90880f40e22812f538d9a0c0`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01319ff876f0a90f52b88a0db82b4f34546c97612dc4988123adb15a952cee`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749a6c3d45b6e53322f1fdfcdeff037de2cd648813a8db706c3925473d004f6`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 33.0 MB (32975132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c502c29ed2b1ba6e7fd2c2aa71175f396a9176edb02e55648b6cf8555189787c`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213f256b750bba2e7bd0657305bd6b3c0051bf884d88a9296fdc9e5fb5df62f`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 826.5 KB (826487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438ad093fa93dc3ac1a33833f1f6adfa20ddc4fd7cbc08bc9266819b9912c92d`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb83f031d4063084ee6ad41d77a9aa0230ae6dbac20f8bbfe5791f043904bc`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:0d981092760d9038f57b80e0550f2ea05b8db146ed6d36079978b4a02355c2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65716f79cf32c55b9b9759bc9a6c2e8b065f5e03899cceb829f0d35cccb4475`

```dockerfile
```

-	Layers:
	-	`sha256:e4dc5031f55e1793bea9034ae5f9a97bf7713526046d4a2a48c9f199003ab7bf`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 2.2 MB (2157548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6104183375130c349d21a5b7afadf82202fb96ffdc4fce3c2c738a109b35d8`  
		Last Modified: Thu, 08 May 2025 23:19:33 GMT  
		Size: 30.4 KB (30445 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:3e45c0d2ead036c529d16de92fc3a13fada03e13fd2a7351aa24753702a2924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73501963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c935e3376691c8c19041e652af0227ca18d7f87c3d5c173401d98cc676a3e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db7ef0a049248006688e39882ca6ced21701e3d55e7cb2f43eb10572e33c7`  
		Last Modified: Fri, 09 May 2025 01:02:09 GMT  
		Size: 13.6 MB (13638347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ccd5673892b28566480f109c15f00e40dac754b53ccd5b997b3b0f7f75b66a`  
		Last Modified: Fri, 09 May 2025 01:02:06 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0f3c897c5b22a06c34b5e67cc4b30c94cf9e55e8b3176d9f4c5f0408e96f1a`  
		Last Modified: Fri, 09 May 2025 01:02:10 GMT  
		Size: 21.2 MB (21162501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef46c091109b0dad546606ab5e3c6ab60d516a7707483f98fa96053dcda29e`  
		Last Modified: Fri, 09 May 2025 01:02:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b931b251640e1d77e3e5386e76828941f021bb5b7fd085a60db7df564d2db`  
		Last Modified: Fri, 09 May 2025 01:02:08 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d591c20251c0df6262a43882dff69cf24f872cb167d9bd70dbe59ce535d6090`  
		Last Modified: Fri, 09 May 2025 16:04:38 GMT  
		Size: 31.0 MB (31044006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56519a808e922477caef5d3ce688e3619da9f0db1b63ff8ca95f3204fd8facec`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953bf8c3df77e8fe57b1937cc9526c14a038522a1e5032e3be6045e73ab81ab4`  
		Last Modified: Fri, 09 May 2025 16:04:34 GMT  
		Size: 818.0 KB (818016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367b8cf7cb2461e691341dff2d886fa6f87b6aefb113f08f33cf4788e265d189`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c78c0216cdee6b454c8cdb8863ffd3299bcf91e241029e54f6e1476f4f68c6`  
		Last Modified: Fri, 09 May 2025 16:04:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:fb04fd51471ffe11168d5634d06301443b94c7d57b1b9d0f48873264aaabff64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9682f06ecfbee994a0ed12df837f984963b9d29fa0a9562995b76e035e2346b`

```dockerfile
```

-	Layers:
	-	`sha256:1dc3c19f202f7b1dd1ce67d2c5430e24b2456e53f134af60077f4e606f23c218`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 2.2 MB (2156490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f8042d631bf40f857397cbf513b0b780fd77689f4dae04133f028a038394e6`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 30.4 KB (30444 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:7bfe50b3671831613ee1f293639da1fd1f01fa55d84992aca6751d6e4fbe1a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75475056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c6021afa836797deb5b72b3b47ecbb83eec4fc77622fcf8461a07fb89ab0ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b5f11089bad6dd57e7f9c626829578bab2c83d4a9d3e6c9dd1c73eccd0d96`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 13.6 MB (13638363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925304c10005fd175f8945f9b79556931bf8772002494541acf614752b95348`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbdcbc01a58fa9ca47c12882f0c582c63ddf71a40fbf79fa956decd72f0f45`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 22.2 MB (22248891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234da8b1110c7fe66f09e4181941a3db5f83769849d61bd62db5481617b0183`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e59c13cf761428c460597e931fe7482a363b6b0afb29d60205e1fa1bc0d234`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da82aeb01a0294d366bfecf08eef375887e0728de96b73baf2f614fc770d6ee4`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 31.7 MB (31706531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47454c44bffd2e898699df83390dc5586ecf0cdb8cf4e637dfbe6e862166142`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f001bcf190f1fb778666f3f658ef2ed9f3e7cab2f0dd096abccd8d41e420887`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 822.8 KB (822788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22faf1bf6e162c31468e05c5bed67a6d31776a496807135f9bbb88cd48ec9ba`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1153a0c4e09017b1231e31c9d4696db651f6dd9cbc383d6faee4043eb19125`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:12753622ea89684fc5c480e1298186a4f71e0a052753e875604ef2f466c92ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff5a88081a75b88c0a41714efba5b65b3a2c2ecb54dcd3f0daa936b12dd36c1`

```dockerfile
```

-	Layers:
	-	`sha256:6de6d8da654c798ae27d488e5d2d34ca32633d4669fabc9a2b049fe472f746bc`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 2.2 MB (2156276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d2b7057a9bea3d0eb01c138e28c2600d46bef824398de4a7790959d3fd6b1e`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.25`

```console
$ docker pull composer@sha256:0d9ad23e2f335bb8e56e259a26626d14ebad2d877a443142187c01e66333682d
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
$ docker pull composer@sha256:5cebd857e3ad2565b6c39e018c0a65b3a66fbfbd6fbb58740b2ce788c39f249f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74359139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231c9f515480b892e0000d9402534862e6fdf23cebe60072d3a2c64fd0859f3e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ec51de1f9773447b65e97f0c677dfa7c2c5a643a8e29c2573fa02d440be485`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 3.3 MB (3339405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f347299a473f0f5d9b5f088e95e92fa5f3fdb929eb8c00e8eee8a5e255fa22`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33c8191db1484b005c5fa5405a7076bdae4e90319fa99dc126e7fc70a360264`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a488374895485209654e2f20371d2b15edb0b1e6e389ec7439903ae08bb34`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 13.6 MB (13638342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242d92ffbbeeb68a81285f10e04caea376e536af932c229bac24f4850ead8549`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5f8d392c5efc498dff46eaccd969d3b99752dc1a40cbdbefd63ae52351c93`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 21.0 MB (20961727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69de2e680c8502b2e77e5bfbf4a6121b21f9356fa9b0058eb0967c21456bad`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d926e2db98107193f77ac67f3ebac3c923c205841b5b20f0a86e5c848b2d66`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499b35e2befe9a2ab9280b1a602e52457d8ed7f23a90e28ba5c103070decea90`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 31.9 MB (31932681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fb4c279258a28b8cf2f050d72d484d11919bd0c4c3ce9275900c07678241b1`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daa442d79abf31d10e17f14740f25bc7f61abff47dc00e1100471c6c0ab7731`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 819.8 KB (819839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2caefd19b6125c0e3b24e00ee848ae2ef85b2d4cc231044b55e28a7a1052d657`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28726ab0de7dc427015158d773cd922bef15e82c8e80a12f7955f42824dcd0be`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:c72c8e096b9c397677aa31c340536654a174b6044f2c65edffe768a9fcdb81f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d7e1497fea47c02d1e9662679efc0af0be65bc38ee751d93c6c03cc0635c3`

```dockerfile
```

-	Layers:
	-	`sha256:23a61df6af22091ccd1fe95b53e017a7c279324770176b85f12aff52854b8acb`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 2.2 MB (2158991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66264756f1845409e67c618f4a4ca8168ea6639f52322b61ed8c8fb05415ca91`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v6

```console
$ docker pull composer@sha256:4172dc3dc33e54a3baecc3587408f2221e194b270edcf1478b855668a54403e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72623422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e19f9283237934aa53cd3933057376364e6d090563214f7a4ed7c49ea76a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce0d04db17a73ca3a7314b885207e80120682c8358368a9254c7f44a7aa2761`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 13.6 MB (13638339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ddeda1f976085a87139c58582b31ac5fd6fc3c900259b39f3163e64bea4ce`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bdf2404f235a46786918527ccb15e5da315bc30edec03f1a23a4d5adbb837c`  
		Last Modified: Thu, 08 May 2025 21:26:22 GMT  
		Size: 19.8 MB (19828990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29e5bd26390c9927b9d705940595b9ccb503518764174068193050a9ee011d3`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837c695d5bcef73c8dfd7be97d8f030b294d365c39fb1ef21f5aec9cebaf695f`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c641fa2ea58cc5073a3f4a40452af3766d1d4eff239fa9c78b7850e692b924`  
		Last Modified: Thu, 08 May 2025 21:56:54 GMT  
		Size: 31.6 MB (31637949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37037a8ef7c2de76decb659167cea10b45dd38661222354aec54af534f7f90e`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371ff9c022135cc30cc8b926dc250d9bedccaa330fa7b9b49b2180d26579405`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 819.6 KB (819643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dfe2f1ed4b221efdeb64a6cae996ca1e2b81afcaf99fe70e875345becffb14`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fade42309a9a0da019a91c17d77c28a835444792b767ee061b9340a9e98601`  
		Last Modified: Thu, 08 May 2025 21:56:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:ec4d3d379007819868c36dbaa75917c97b6406d4f344ad400c65266f4ed42495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7ec15c414ca787e4ac72f051579b92506a8bf9462509c15877e043fd19c606`

```dockerfile
```

-	Layers:
	-	`sha256:335cd578e45ca45ad6ba03232eade190f053ea93f1d2ad1192b0482130aaf2e3`  
		Last Modified: Thu, 08 May 2025 21:56:52 GMT  
		Size: 30.3 KB (30282 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v7

```console
$ docker pull composer@sha256:a033f1b78facdd5e0a4c5572ab28a12555f6082ba945bd577e20185521f7d8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69632557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2e2fd5ef57b840623eb18bcf85fccaf61c29b60b7c294d5d40961180ff18a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae53c42a3a934e2af6db5b115410a7b4c6a02cd2b122d00b65d1eca1a41169`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 13.6 MB (13638357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10142d79ada8bf8b882c44da37430c2d14e535a18518bf2925f9f960b71e79`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfab14bb194eab55e2e70f9afc13ee33e4dd21aa21350e1374e86f05fb626af`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 18.8 MB (18755156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da76f291cb0bcd5dc8fc90d909e92ab04c17a7553ef5146ab7e325af2708443`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d3e5b7d935e85e9b31895bd1360c16fb666b189cce4d62af34133ff180412`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df80c80dab935ac507aa56dc704c0803d9d2fcf950397319075ec118fc80934`  
		Last Modified: Fri, 09 May 2025 02:56:40 GMT  
		Size: 30.2 MB (30185429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c3a1b4fa684906875f7fd4416d71426ac1aee26864470455b1b9b46d7828d`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8513c8b163ee9709e5b3dc3c4a87f1f4594811ef656312a0af412be48d9a71a3`  
		Last Modified: Fri, 09 May 2025 02:56:39 GMT  
		Size: 810.4 KB (810358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f934f90fc13c2bef368b2a479f52aede5fcc42961f5c81a7db6ff1e6c825dc89`  
		Last Modified: Fri, 09 May 2025 02:56:39 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66be4070bf8d4b80b5a8a8b70270241facc3bf78b63e4af4c22a8e567adb61d`  
		Last Modified: Fri, 09 May 2025 02:56:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:7a9fc43d076b9bda83778bd6c939613f27e5fe5df60c4dd82ec67b96ee1b1fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff36941efce39e79c925e7ca11bc454085ff33081bc3f4f4c8e1caf4f776e548`

```dockerfile
```

-	Layers:
	-	`sha256:53372f3f7fdb0d6d0a5ceb85baad3547326f5c809570f5e0e8d18d07909da27b`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 2.2 MB (2159307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cc2a070c97eb5d5bb8a4d940d24e54abe8bfe8aee9c97b3c8fb0f8eb0385492`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 30.5 KB (30496 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:660a3f96590101779bae7458cc72850e95b0798689489014f57c2f88b66f06a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74351321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1479d7d13817ee69723abf2ab0d58fb9142d8d74aad87e6e04c33b22c11a42bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752b27585c21531ef183f9331718681f7d5a399ad1721fe17bf65ec91aa026d`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 3.3 MB (3332291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c504757a74563c6c69cb5f5ab95d450088933adf663323509ef07a437fda44`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64969c8e6dd0ea68ca6e1a455172bdc1ce583b5d543fc3120d33f200e06302a1`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1176f7a4c5fb0e54724b9ad7ea378a6420c35cbfd4d0eeb5e1fef5d9ba7ac`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 13.6 MB (13638372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9788910834fbf94207a3e2b19ab0e6fabbefd4e42d621687e321a1db2f16e53e`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edad5b9c93eee4f4366f3ebeb11225c8f73a2b77b6f9619550727373b01d51f`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 20.5 MB (20506682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aad88073420d66b54ab164736e4f80b7f83ed7afde64e75da65e76a0601f38`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d8baab457dd5125f7b8056acc97da76b6e4aed76359cef6cf89c1be2f9546`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9518d6339aceaab8bbfa04cb293db8787e29591ef024e80b24a882a2c9c8edc0`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 32.0 MB (32036745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e197ccaccec2cf61efc3cdf266d9ef310f66d8e5905a95466247bdefc08c5d4`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e016548f32a92f4ca21a9b9425d229f0603e50f7331434d48433cf080f21f9d7`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 819.5 KB (819499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918d9b05ba0bc908df65d8242560fbefbfa893916fc6f79a748fd37ea31e7a54`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15dcffea100c734bb9900526c295a50bdf08a6b81c92e61e5a13114d41744a5`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:6657510496ff088eb85b663658ab399924ca08198893202c463c41b3d5e0153c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f18624eaa94a7e36971327a97cbbb1b9daca6359f96e86096b283526218c5`

```dockerfile
```

-	Layers:
	-	`sha256:83b24749f270a87ef6e8438cb57a5a675bbde85039ac32beb1265124878b6ad7`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 2.2 MB (2159131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:488da887497f8349c6b6ffa9c501688798e299f8888b05bcc32bad6f267e3566`  
		Last Modified: Fri, 09 May 2025 01:10:10 GMT  
		Size: 30.5 KB (30525 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; 386

```console
$ docker pull composer@sha256:19ea0af1d6d1bf965c8997ebf71e2a92c1313cfe4da8c8647b813f2c0ff4d354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75239586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05421cc0f995b8c637f983dea20efd577dcb54c35443c3e98b1a8a001470e15`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0fee7f3118a5985c2f626fb5b6c58f3e09615e2d0e574b152efa48b96dba0`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 3.4 MB (3379885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0859e481ff1d593c72d70f1d40018ee891c8a85aed61e584093925eef0bcab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b986eab8e8b3e0184edeb69c32c4ed3d8588e109c815e0849b82bb054cacab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7b75ef5fb8c211e5b9a329554b4301d5c6eb7ae9c8b76dc280c611f52936f2`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 13.6 MB (13638340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbb0139bcece2c1bb61243f10b29ef44dfb0038edd4f69191a281fb8695da3`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6161bb22ced62e09258a8f26973e62bc0c0b3f09f6fd571bc8cbf3d57d556`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 21.5 MB (21479578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe4c701feaead74489728c530e52569dea2bd050f15b4c2465b658466d6ea38`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aa3b4dea6bd9bd03e0d1ad21c8a068d7303cd61d25541395be92f12129e0a8`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ebfea0ea0e34c30ea6572f9b90a6a82e0b30799b9188503151036d51972dfc`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 32.4 MB (32419650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a210db33b806b55bf805f429c9afe113595174151758714de88d5944b7601285`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040bd3ee25d7721ce0b770039cc202b97b3485095553647d8ffd0ae391e2455d`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 833.6 KB (833619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5069feb63748d630228815c7019641ca31353671475fdf0d0a501f0fcaebbd1`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89ed163134dd5463572f12e039ed75cf48686e844ba79683f8d79735a5d58b2`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:943f12c594a481ac8feb5cd7d2d84cbf3f2a9ecbe7d80ae95f18599fb2a14d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e6e873d877d21ef07a5f1b9312aa3dd3f5f4f9eb482511f8c09ec0bca70ddc`

```dockerfile
```

-	Layers:
	-	`sha256:b8481db856b3845732b38141065fb355ae9c854c682bd7c3b3c3ab9573541b12`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 2.2 MB (2158779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e205d10e14e98bd5d46cd83ddb52dd8ae5409e379edfb679a5e6bed943f031`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 30.4 KB (30372 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; ppc64le

```console
$ docker pull composer@sha256:72c16852f91d422eb2182a913c7a3a2c5a0446ac4ad2f2e89ecf389cdbdcc2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77218301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af02315b6b038713c7e17f053cd7610afb4fb1e720eaf246c39026433a7a407d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e76c061ea4a5ab1435512c8388fd08bd714f08a20a3d13e20958322c1e38c8`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 13.6 MB (13638361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6741176fa79481125f0168dfab2269eb4d272b50ffffa3eb93489fbac4b7e`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baaae08012b74873c8e9eb084b4c040c29cb1b207bf5a13250c34c0533cab9a`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 22.7 MB (22698151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d926e7ce8969775d3b04d34e3a2c99bd3026dadb90880f40e22812f538d9a0c0`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01319ff876f0a90f52b88a0db82b4f34546c97612dc4988123adb15a952cee`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749a6c3d45b6e53322f1fdfcdeff037de2cd648813a8db706c3925473d004f6`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 33.0 MB (32975132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c502c29ed2b1ba6e7fd2c2aa71175f396a9176edb02e55648b6cf8555189787c`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213f256b750bba2e7bd0657305bd6b3c0051bf884d88a9296fdc9e5fb5df62f`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 826.5 KB (826487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438ad093fa93dc3ac1a33833f1f6adfa20ddc4fd7cbc08bc9266819b9912c92d`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb83f031d4063084ee6ad41d77a9aa0230ae6dbac20f8bbfe5791f043904bc`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:0d981092760d9038f57b80e0550f2ea05b8db146ed6d36079978b4a02355c2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65716f79cf32c55b9b9759bc9a6c2e8b065f5e03899cceb829f0d35cccb4475`

```dockerfile
```

-	Layers:
	-	`sha256:e4dc5031f55e1793bea9034ae5f9a97bf7713526046d4a2a48c9f199003ab7bf`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 2.2 MB (2157548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6104183375130c349d21a5b7afadf82202fb96ffdc4fce3c2c738a109b35d8`  
		Last Modified: Thu, 08 May 2025 23:19:33 GMT  
		Size: 30.4 KB (30445 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; riscv64

```console
$ docker pull composer@sha256:3e45c0d2ead036c529d16de92fc3a13fada03e13fd2a7351aa24753702a2924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73501963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c935e3376691c8c19041e652af0227ca18d7f87c3d5c173401d98cc676a3e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db7ef0a049248006688e39882ca6ced21701e3d55e7cb2f43eb10572e33c7`  
		Last Modified: Fri, 09 May 2025 01:02:09 GMT  
		Size: 13.6 MB (13638347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ccd5673892b28566480f109c15f00e40dac754b53ccd5b997b3b0f7f75b66a`  
		Last Modified: Fri, 09 May 2025 01:02:06 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0f3c897c5b22a06c34b5e67cc4b30c94cf9e55e8b3176d9f4c5f0408e96f1a`  
		Last Modified: Fri, 09 May 2025 01:02:10 GMT  
		Size: 21.2 MB (21162501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef46c091109b0dad546606ab5e3c6ab60d516a7707483f98fa96053dcda29e`  
		Last Modified: Fri, 09 May 2025 01:02:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b931b251640e1d77e3e5386e76828941f021bb5b7fd085a60db7df564d2db`  
		Last Modified: Fri, 09 May 2025 01:02:08 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d591c20251c0df6262a43882dff69cf24f872cb167d9bd70dbe59ce535d6090`  
		Last Modified: Fri, 09 May 2025 16:04:38 GMT  
		Size: 31.0 MB (31044006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56519a808e922477caef5d3ce688e3619da9f0db1b63ff8ca95f3204fd8facec`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953bf8c3df77e8fe57b1937cc9526c14a038522a1e5032e3be6045e73ab81ab4`  
		Last Modified: Fri, 09 May 2025 16:04:34 GMT  
		Size: 818.0 KB (818016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367b8cf7cb2461e691341dff2d886fa6f87b6aefb113f08f33cf4788e265d189`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c78c0216cdee6b454c8cdb8863ffd3299bcf91e241029e54f6e1476f4f68c6`  
		Last Modified: Fri, 09 May 2025 16:04:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:fb04fd51471ffe11168d5634d06301443b94c7d57b1b9d0f48873264aaabff64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9682f06ecfbee994a0ed12df837f984963b9d29fa0a9562995b76e035e2346b`

```dockerfile
```

-	Layers:
	-	`sha256:1dc3c19f202f7b1dd1ce67d2c5430e24b2456e53f134af60077f4e606f23c218`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 2.2 MB (2156490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f8042d631bf40f857397cbf513b0b780fd77689f4dae04133f028a038394e6`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 30.4 KB (30444 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; s390x

```console
$ docker pull composer@sha256:7bfe50b3671831613ee1f293639da1fd1f01fa55d84992aca6751d6e4fbe1a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75475056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c6021afa836797deb5b72b3b47ecbb83eec4fc77622fcf8461a07fb89ab0ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b5f11089bad6dd57e7f9c626829578bab2c83d4a9d3e6c9dd1c73eccd0d96`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 13.6 MB (13638363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925304c10005fd175f8945f9b79556931bf8772002494541acf614752b95348`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbdcbc01a58fa9ca47c12882f0c582c63ddf71a40fbf79fa956decd72f0f45`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 22.2 MB (22248891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234da8b1110c7fe66f09e4181941a3db5f83769849d61bd62db5481617b0183`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e59c13cf761428c460597e931fe7482a363b6b0afb29d60205e1fa1bc0d234`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da82aeb01a0294d366bfecf08eef375887e0728de96b73baf2f614fc770d6ee4`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 31.7 MB (31706531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47454c44bffd2e898699df83390dc5586ecf0cdb8cf4e637dfbe6e862166142`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f001bcf190f1fb778666f3f658ef2ed9f3e7cab2f0dd096abccd8d41e420887`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 822.8 KB (822788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22faf1bf6e162c31468e05c5bed67a6d31776a496807135f9bbb88cd48ec9ba`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1153a0c4e09017b1231e31c9d4696db651f6dd9cbc383d6faee4043eb19125`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:12753622ea89684fc5c480e1298186a4f71e0a052753e875604ef2f466c92ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff5a88081a75b88c0a41714efba5b65b3a2c2ecb54dcd3f0daa936b12dd36c1`

```dockerfile
```

-	Layers:
	-	`sha256:6de6d8da654c798ae27d488e5d2d34ca32633d4669fabc9a2b049fe472f746bc`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 2.2 MB (2156276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d2b7057a9bea3d0eb01c138e28c2600d46bef824398de4a7790959d3fd6b1e`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:3df281ca83119bff1332f0f5f311960cb16b99238f8273acd965be6bd508aa8e
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
$ docker pull composer@sha256:ec31187cf6de8fbb71d2c493ec704f5b76955a3090b3295adf39f0fd5d1eb479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74513054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539808e605ec8fdd3117a80817d3e99ce4af0c3c34ca931e8f23e5aeeb22aea7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ec51de1f9773447b65e97f0c677dfa7c2c5a643a8e29c2573fa02d440be485`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 3.3 MB (3339405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f347299a473f0f5d9b5f088e95e92fa5f3fdb929eb8c00e8eee8a5e255fa22`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33c8191db1484b005c5fa5405a7076bdae4e90319fa99dc126e7fc70a360264`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a488374895485209654e2f20371d2b15edb0b1e6e389ec7439903ae08bb34`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 13.6 MB (13638342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242d92ffbbeeb68a81285f10e04caea376e536af932c229bac24f4850ead8549`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5f8d392c5efc498dff46eaccd969d3b99752dc1a40cbdbefd63ae52351c93`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 21.0 MB (20961727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69de2e680c8502b2e77e5bfbf4a6121b21f9356fa9b0058eb0967c21456bad`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d926e2db98107193f77ac67f3ebac3c923c205841b5b20f0a86e5c848b2d66`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f35e65c467d6a06e463158b71b59b394f945292ceb3f5085e55d3ef27a4da9d`  
		Last Modified: Thu, 08 May 2025 21:49:23 GMT  
		Size: 31.9 MB (31932834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07970fc96919497974b26ac2861318973a76e07ff79f1b64faed95d351083da0`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa5aa8beb42ce23af82c206ab0a95fc0b8426daa93031c684e7d7da64f5415a`  
		Last Modified: Thu, 08 May 2025 21:49:23 GMT  
		Size: 973.6 KB (973600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98df5a35c2fe3e9c05282183b08d8ceb4ec343e2479353c3d9632a64d7e49b6`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67885e2977d33ff647e990ab306798d84593f91d0fb665528f08b8fbaa1ac723`  
		Last Modified: Thu, 08 May 2025 21:49:23 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:1f0f50d68f9860890b7bd409b5b76951479c5c14b8ed9eab06f2c305a52a3a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2d8618c9ebce7af590de1125a08b17d5973e1daa67d8ffe3ee4c3a288764dc`

```dockerfile
```

-	Layers:
	-	`sha256:bfbf90c8d1e9be23a21546ffe91ffc2f2f50be40041df99c9c75cb1b6811922c`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 2.2 MB (2159285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193dd9351255782fb765b8209163883befcc28d1c1b5707d7382f9976ef17dc5`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:a7dff16e0bdc5c9bc5f24d80b850d263b206479078e2c883dc13d4142261a237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72777249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cf8efc80624ecf1ae3f6e2946b2059cebcc02c496ccc6963754e090488fc16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce0d04db17a73ca3a7314b885207e80120682c8358368a9254c7f44a7aa2761`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 13.6 MB (13638339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ddeda1f976085a87139c58582b31ac5fd6fc3c900259b39f3163e64bea4ce`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bdf2404f235a46786918527ccb15e5da315bc30edec03f1a23a4d5adbb837c`  
		Last Modified: Thu, 08 May 2025 21:26:22 GMT  
		Size: 19.8 MB (19828990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29e5bd26390c9927b9d705940595b9ccb503518764174068193050a9ee011d3`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837c695d5bcef73c8dfd7be97d8f030b294d365c39fb1ef21f5aec9cebaf695f`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c641fa2ea58cc5073a3f4a40452af3766d1d4eff239fa9c78b7850e692b924`  
		Last Modified: Thu, 08 May 2025 21:56:54 GMT  
		Size: 31.6 MB (31637949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37037a8ef7c2de76decb659167cea10b45dd38661222354aec54af534f7f90e`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d36a7b322939484d5ee5c8e4d2acf6b7e5d10aa83eba813e5aa7ca50ba2756`  
		Last Modified: Thu, 08 May 2025 21:58:05 GMT  
		Size: 973.5 KB (973470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f863439db685c5d731f58b9e7de989a88fa5b917b13af3f5f2d825a19b4ae3a`  
		Last Modified: Thu, 08 May 2025 21:58:05 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a186e1d7e7ee9e9772006a97e08806d1e5b4089ed1161b0a7cd6e680fa291b`  
		Last Modified: Thu, 08 May 2025 21:58:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:5b47eb452f6d117c416ce8d5e3a6c87296956ef588e545df40795678b3928543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1083c9aa6c3a0ee50d5c3c12d77d92fc773c9f801866daafc72b1de2f336e464`

```dockerfile
```

-	Layers:
	-	`sha256:3e1e0b06eb56f368894bce8fb4cb9415ad55c94f2959e12dafcfd14f064a3f50`  
		Last Modified: Thu, 08 May 2025 21:58:04 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:b14aa8913a1e62db51a228506079460ce6e2033447ed821db51e1762fa8776ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69786310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12189a43195c725265f01f4a102edd3b5c363094476821180a6e4aada55df9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae53c42a3a934e2af6db5b115410a7b4c6a02cd2b122d00b65d1eca1a41169`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 13.6 MB (13638357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10142d79ada8bf8b882c44da37430c2d14e535a18518bf2925f9f960b71e79`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfab14bb194eab55e2e70f9afc13ee33e4dd21aa21350e1374e86f05fb626af`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 18.8 MB (18755156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da76f291cb0bcd5dc8fc90d909e92ab04c17a7553ef5146ab7e325af2708443`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d3e5b7d935e85e9b31895bd1360c16fb666b189cce4d62af34133ff180412`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df80c80dab935ac507aa56dc704c0803d9d2fcf950397319075ec118fc80934`  
		Last Modified: Fri, 09 May 2025 02:56:40 GMT  
		Size: 30.2 MB (30185429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c3a1b4fa684906875f7fd4416d71426ac1aee26864470455b1b9b46d7828d`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0df7a4b2868d4940542adb230523d1e4ed001e3b81e5b207cecf42c343f478`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 964.1 KB (964111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b73a1fcb61a5a282a8c9397a8c576b45fbe6caa25857e13ea650cb4d76322a`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef7526f5b3917e2bc638427511d4989ad3248fae4b127cd3e0d33e74a490514`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:4085cd69ad186b4f31b2d00827f60d3f772d59734d0e19d4d610951d1ab3da6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463b46d8bb3fa777b046df54e8e2a1c586a9ffd3aa84723d00aee9899233ec16`

```dockerfile
```

-	Layers:
	-	`sha256:97eddbfc009a7db168669d971a6e5e733e0fc7795c4e86ab74ef4c3805df0df5`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 2.2 MB (2159609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6143674f1e33328ecad90616b50233ba90952a12cf467628257ba949eb7dd771`  
		Last Modified: Fri, 09 May 2025 02:58:18 GMT  
		Size: 30.8 KB (30808 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:3eb81b210445eab75a9596c806a3723d0154537ffbea44e924dd375bd8d46ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74505054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cc127439d34c6f96676db2c801e18e32fe42a8f19167bee613e3cb32a8bdf8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752b27585c21531ef183f9331718681f7d5a399ad1721fe17bf65ec91aa026d`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 3.3 MB (3332291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c504757a74563c6c69cb5f5ab95d450088933adf663323509ef07a437fda44`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64969c8e6dd0ea68ca6e1a455172bdc1ce583b5d543fc3120d33f200e06302a1`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1176f7a4c5fb0e54724b9ad7ea378a6420c35cbfd4d0eeb5e1fef5d9ba7ac`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 13.6 MB (13638372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9788910834fbf94207a3e2b19ab0e6fabbefd4e42d621687e321a1db2f16e53e`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edad5b9c93eee4f4366f3ebeb11225c8f73a2b77b6f9619550727373b01d51f`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 20.5 MB (20506682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aad88073420d66b54ab164736e4f80b7f83ed7afde64e75da65e76a0601f38`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d8baab457dd5125f7b8056acc97da76b6e4aed76359cef6cf89c1be2f9546`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9518d6339aceaab8bbfa04cb293db8787e29591ef024e80b24a882a2c9c8edc0`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 32.0 MB (32036745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e197ccaccec2cf61efc3cdf266d9ef310f66d8e5905a95466247bdefc08c5d4`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63caa9b8a6f65f98bf399b6c0907858c28d179a339fcecce75876a27f8711118`  
		Last Modified: Fri, 09 May 2025 01:11:24 GMT  
		Size: 973.2 KB (973231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c61d014799dc6bf76eb35626076e710fc5e4dda0e4843cb4c5654377f2392d`  
		Last Modified: Fri, 09 May 2025 01:11:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d41ade31de22ec89775e848aa31682bf031124c7194426184d23e224ab3621`  
		Last Modified: Fri, 09 May 2025 01:11:24 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:6e3b0fecd14009a0ff39e9f8ce6e612b0954f575c01f51f0989e4e62849bc904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac85c03c9804fea2906b6da84c95a285730f93e6e58ea7b21c85819ef99cbad`

```dockerfile
```

-	Layers:
	-	`sha256:9b88aeefeff43c9faec75bbdf559e9d233e3f8a104137975bd17b3c8f38e575d`  
		Last Modified: Fri, 09 May 2025 01:11:23 GMT  
		Size: 2.2 MB (2159437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d477695b3b116918cd550b0c4d81ffbfdc9142b846a0ce5cfe1a10827574c8`  
		Last Modified: Fri, 09 May 2025 01:11:22 GMT  
		Size: 30.8 KB (30841 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:1b5e00fff273c7f8077e9e7e091ee6a8544ca4527c32b4e19652ad679af027ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75393539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b1a4ae43abdf7f81cb2fc374621656b152c7f70595cad0a364c16bbc20ea8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0fee7f3118a5985c2f626fb5b6c58f3e09615e2d0e574b152efa48b96dba0`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 3.4 MB (3379885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0859e481ff1d593c72d70f1d40018ee891c8a85aed61e584093925eef0bcab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b986eab8e8b3e0184edeb69c32c4ed3d8588e109c815e0849b82bb054cacab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7b75ef5fb8c211e5b9a329554b4301d5c6eb7ae9c8b76dc280c611f52936f2`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 13.6 MB (13638340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbb0139bcece2c1bb61243f10b29ef44dfb0038edd4f69191a281fb8695da3`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6161bb22ced62e09258a8f26973e62bc0c0b3f09f6fd571bc8cbf3d57d556`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 21.5 MB (21479578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe4c701feaead74489728c530e52569dea2bd050f15b4c2465b658466d6ea38`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aa3b4dea6bd9bd03e0d1ad21c8a068d7303cd61d25541395be92f12129e0a8`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9d3822fff04ee88d265cf3b2f6fda0935618827f02ccb83caddd149472bfb6`  
		Last Modified: Thu, 08 May 2025 21:49:18 GMT  
		Size: 32.4 MB (32419790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4749bed490bc2e21ca8b7e67d7dca5701af7d8733ff3f555fc28be07dddf67d5`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8991ac628ce8adf7b232be49fdf5f393c12b8036a374619747aa07d1191bf1`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 987.4 KB (987427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67722e7ebd67ddc3ea5804cf2081f36d6624dfd689578ce547276b49702f80d9`  
		Last Modified: Thu, 08 May 2025 21:49:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791cac75c2ce2bdf945782129c08f92674bc6ebae72272ad6dd7372877bd7ca0`  
		Last Modified: Thu, 08 May 2025 21:49:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:38527cd7533c5a71d0bd5adb953746455b3cd43bd38d79e7538ef1d370d857b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22fec3f1104eee0cb88dd02a43136b15cafd5ea020c4a31e3d1d3204f2b2425`

```dockerfile
```

-	Layers:
	-	`sha256:22a0fc51722a9f887d0d979027ed22915615024058d3bf602b7e93f1546298f9`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 2.2 MB (2159068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1463be1cdff852ccf958d429ad3373c183fa577d98d14b778a8846e47cf76edf`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:8b89c42c4af0e06aefd095dbb34c2619855dac845cb2a01d188b3a77c4bb5d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77372105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068ba4fd3895e50862519de9921b88288ba5328fa9baeb66de3c2f38c5387bfe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e76c061ea4a5ab1435512c8388fd08bd714f08a20a3d13e20958322c1e38c8`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 13.6 MB (13638361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6741176fa79481125f0168dfab2269eb4d272b50ffffa3eb93489fbac4b7e`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baaae08012b74873c8e9eb084b4c040c29cb1b207bf5a13250c34c0533cab9a`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 22.7 MB (22698151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d926e7ce8969775d3b04d34e3a2c99bd3026dadb90880f40e22812f538d9a0c0`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01319ff876f0a90f52b88a0db82b4f34546c97612dc4988123adb15a952cee`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749a6c3d45b6e53322f1fdfcdeff037de2cd648813a8db706c3925473d004f6`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 33.0 MB (32975132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c502c29ed2b1ba6e7fd2c2aa71175f396a9176edb02e55648b6cf8555189787c`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0684f605738b7e5978c5a350d7cbb9885d6e9593c7e5eae0ddbc6ce32c02a22e`  
		Last Modified: Thu, 08 May 2025 23:21:27 GMT  
		Size: 980.3 KB (980290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3865705398f20912aedf7e8109210983ab47fc0c7862afae8288b244efbbfbef`  
		Last Modified: Thu, 08 May 2025 23:21:27 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f2b0dbc52dd18eb4223fdbf933144b2bf9e6aa6dcc618cc87532424c5aa68d`  
		Last Modified: Thu, 08 May 2025 23:21:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:8f25a18ddac3fff471eb1d915aa6b545fef585f2ef4a0c6d6ad5937a012071ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5311e03457df6c7d776932408097f223757d845b04c0928ffacab82f34f399a6`

```dockerfile
```

-	Layers:
	-	`sha256:2d792c31a36378da39476236ad13355e8d2ac4418b7aaa84c3bcab1e1a9bcd08`  
		Last Modified: Thu, 08 May 2025 23:21:26 GMT  
		Size: 2.2 MB (2157848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044e4e017f6b8890a5b64a606fa7abbc89bbaf0beae880d8c34c96c26276b056`  
		Last Modified: Thu, 08 May 2025 23:21:26 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:6e9ec48444ac9558ef69eb1c9f824baf5314522f44538a49e4733ad1b3cd30cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73655710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420af2fb4f88c27b8de5e5a3cd3978d65d51761075b4d2e02e117800af46470c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db7ef0a049248006688e39882ca6ced21701e3d55e7cb2f43eb10572e33c7`  
		Last Modified: Fri, 09 May 2025 01:02:09 GMT  
		Size: 13.6 MB (13638347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ccd5673892b28566480f109c15f00e40dac754b53ccd5b997b3b0f7f75b66a`  
		Last Modified: Fri, 09 May 2025 01:02:06 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0f3c897c5b22a06c34b5e67cc4b30c94cf9e55e8b3176d9f4c5f0408e96f1a`  
		Last Modified: Fri, 09 May 2025 01:02:10 GMT  
		Size: 21.2 MB (21162501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef46c091109b0dad546606ab5e3c6ab60d516a7707483f98fa96053dcda29e`  
		Last Modified: Fri, 09 May 2025 01:02:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b931b251640e1d77e3e5386e76828941f021bb5b7fd085a60db7df564d2db`  
		Last Modified: Fri, 09 May 2025 01:02:08 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d591c20251c0df6262a43882dff69cf24f872cb167d9bd70dbe59ce535d6090`  
		Last Modified: Fri, 09 May 2025 16:04:38 GMT  
		Size: 31.0 MB (31044006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56519a808e922477caef5d3ce688e3619da9f0db1b63ff8ca95f3204fd8facec`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ed4acbc6167d6e65bd61a656d64ead373ef36f1602553fbf264731bfa550c`  
		Last Modified: Fri, 09 May 2025 16:15:00 GMT  
		Size: 971.8 KB (971762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04c9848bde98f1cc4f6e54f5b1c32bc5ba6cc29936f7c082af8d2a54e898813`  
		Last Modified: Fri, 09 May 2025 16:14:59 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7822088e7ffa14e2fabd2259297ef14419e9c93f94af3f4eff289969f1b934`  
		Last Modified: Fri, 09 May 2025 16:15:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:da09a3427cf58ee280cd57b40273df9437aead71dd19144d48010936605c4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d48ba38d8d40fa452f8a26f25e490ec24255f7f8c6e719b130360219859b2f`

```dockerfile
```

-	Layers:
	-	`sha256:7a2527bded2278ba5d2f827638d12324fe5fdeb391d080e59130442d5ebe9735`  
		Last Modified: Fri, 09 May 2025 16:14:59 GMT  
		Size: 2.2 MB (2156790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc040a825e20bb854175bac49728f383c6830a0b9c00ae1216afa7558fcfc0fd`  
		Last Modified: Fri, 09 May 2025 16:14:59 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:dfc7fc645d6a07047a78073623daf44350935a34c1c8566c5dcb95ea1ee9228a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75628873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94efc800e610253d603808a8925143397964e88a27a64a89e35a572b016c1201`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b5f11089bad6dd57e7f9c626829578bab2c83d4a9d3e6c9dd1c73eccd0d96`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 13.6 MB (13638363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925304c10005fd175f8945f9b79556931bf8772002494541acf614752b95348`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbdcbc01a58fa9ca47c12882f0c582c63ddf71a40fbf79fa956decd72f0f45`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 22.2 MB (22248891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234da8b1110c7fe66f09e4181941a3db5f83769849d61bd62db5481617b0183`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e59c13cf761428c460597e931fe7482a363b6b0afb29d60205e1fa1bc0d234`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da82aeb01a0294d366bfecf08eef375887e0728de96b73baf2f614fc770d6ee4`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 31.7 MB (31706531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47454c44bffd2e898699df83390dc5586ecf0cdb8cf4e637dfbe6e862166142`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d135b86d58d8377467d55bf776e53000abc3b9d4bfaed27cf9d02c772ce5d0`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 976.6 KB (976603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed9f8099552b00200734259e0b36ab4f94c39d36a77e29f46335351783611e7`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dd9dc76f2c0e4b853173a0da2d6ad8c31b58983ecf0c6dded53de8ad1eadf4`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:2923462ef720cfdb712a7c14681218303b60eb1a65b653f0aa292525ac745924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c62a52a3b3a37c11a1613f5091cac4f0aa9b257b133215d731a3f11e79cb27`

```dockerfile
```

-	Layers:
	-	`sha256:ed73a17c8aee94540dd474fc24fb314abd3e712e9df24917150e0160a6d5839f`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 2.2 MB (2156570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967ce814b657814077f50f73fb82037f671822aeb253504f07e43bf74fc2a3a8`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.8`

```console
$ docker pull composer@sha256:3df281ca83119bff1332f0f5f311960cb16b99238f8273acd965be6bd508aa8e
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

### `composer:2.8.8` - linux; amd64

```console
$ docker pull composer@sha256:ec31187cf6de8fbb71d2c493ec704f5b76955a3090b3295adf39f0fd5d1eb479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74513054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539808e605ec8fdd3117a80817d3e99ce4af0c3c34ca931e8f23e5aeeb22aea7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ec51de1f9773447b65e97f0c677dfa7c2c5a643a8e29c2573fa02d440be485`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 3.3 MB (3339405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f347299a473f0f5d9b5f088e95e92fa5f3fdb929eb8c00e8eee8a5e255fa22`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33c8191db1484b005c5fa5405a7076bdae4e90319fa99dc126e7fc70a360264`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a488374895485209654e2f20371d2b15edb0b1e6e389ec7439903ae08bb34`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 13.6 MB (13638342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242d92ffbbeeb68a81285f10e04caea376e536af932c229bac24f4850ead8549`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5f8d392c5efc498dff46eaccd969d3b99752dc1a40cbdbefd63ae52351c93`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 21.0 MB (20961727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69de2e680c8502b2e77e5bfbf4a6121b21f9356fa9b0058eb0967c21456bad`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d926e2db98107193f77ac67f3ebac3c923c205841b5b20f0a86e5c848b2d66`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f35e65c467d6a06e463158b71b59b394f945292ceb3f5085e55d3ef27a4da9d`  
		Last Modified: Thu, 08 May 2025 21:49:23 GMT  
		Size: 31.9 MB (31932834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07970fc96919497974b26ac2861318973a76e07ff79f1b64faed95d351083da0`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa5aa8beb42ce23af82c206ab0a95fc0b8426daa93031c684e7d7da64f5415a`  
		Last Modified: Thu, 08 May 2025 21:49:23 GMT  
		Size: 973.6 KB (973600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98df5a35c2fe3e9c05282183b08d8ceb4ec343e2479353c3d9632a64d7e49b6`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67885e2977d33ff647e990ab306798d84593f91d0fb665528f08b8fbaa1ac723`  
		Last Modified: Thu, 08 May 2025 21:49:23 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:1f0f50d68f9860890b7bd409b5b76951479c5c14b8ed9eab06f2c305a52a3a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2d8618c9ebce7af590de1125a08b17d5973e1daa67d8ffe3ee4c3a288764dc`

```dockerfile
```

-	Layers:
	-	`sha256:bfbf90c8d1e9be23a21546ffe91ffc2f2f50be40041df99c9c75cb1b6811922c`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 2.2 MB (2159285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193dd9351255782fb765b8209163883befcc28d1c1b5707d7382f9976ef17dc5`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:a7dff16e0bdc5c9bc5f24d80b850d263b206479078e2c883dc13d4142261a237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72777249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cf8efc80624ecf1ae3f6e2946b2059cebcc02c496ccc6963754e090488fc16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce0d04db17a73ca3a7314b885207e80120682c8358368a9254c7f44a7aa2761`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 13.6 MB (13638339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ddeda1f976085a87139c58582b31ac5fd6fc3c900259b39f3163e64bea4ce`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bdf2404f235a46786918527ccb15e5da315bc30edec03f1a23a4d5adbb837c`  
		Last Modified: Thu, 08 May 2025 21:26:22 GMT  
		Size: 19.8 MB (19828990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29e5bd26390c9927b9d705940595b9ccb503518764174068193050a9ee011d3`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837c695d5bcef73c8dfd7be97d8f030b294d365c39fb1ef21f5aec9cebaf695f`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c641fa2ea58cc5073a3f4a40452af3766d1d4eff239fa9c78b7850e692b924`  
		Last Modified: Thu, 08 May 2025 21:56:54 GMT  
		Size: 31.6 MB (31637949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37037a8ef7c2de76decb659167cea10b45dd38661222354aec54af534f7f90e`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d36a7b322939484d5ee5c8e4d2acf6b7e5d10aa83eba813e5aa7ca50ba2756`  
		Last Modified: Thu, 08 May 2025 21:58:05 GMT  
		Size: 973.5 KB (973470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f863439db685c5d731f58b9e7de989a88fa5b917b13af3f5f2d825a19b4ae3a`  
		Last Modified: Thu, 08 May 2025 21:58:05 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a186e1d7e7ee9e9772006a97e08806d1e5b4089ed1161b0a7cd6e680fa291b`  
		Last Modified: Thu, 08 May 2025 21:58:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:5b47eb452f6d117c416ce8d5e3a6c87296956ef588e545df40795678b3928543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1083c9aa6c3a0ee50d5c3c12d77d92fc773c9f801866daafc72b1de2f336e464`

```dockerfile
```

-	Layers:
	-	`sha256:3e1e0b06eb56f368894bce8fb4cb9415ad55c94f2959e12dafcfd14f064a3f50`  
		Last Modified: Thu, 08 May 2025 21:58:04 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:b14aa8913a1e62db51a228506079460ce6e2033447ed821db51e1762fa8776ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69786310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12189a43195c725265f01f4a102edd3b5c363094476821180a6e4aada55df9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae53c42a3a934e2af6db5b115410a7b4c6a02cd2b122d00b65d1eca1a41169`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 13.6 MB (13638357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10142d79ada8bf8b882c44da37430c2d14e535a18518bf2925f9f960b71e79`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfab14bb194eab55e2e70f9afc13ee33e4dd21aa21350e1374e86f05fb626af`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 18.8 MB (18755156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da76f291cb0bcd5dc8fc90d909e92ab04c17a7553ef5146ab7e325af2708443`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d3e5b7d935e85e9b31895bd1360c16fb666b189cce4d62af34133ff180412`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df80c80dab935ac507aa56dc704c0803d9d2fcf950397319075ec118fc80934`  
		Last Modified: Fri, 09 May 2025 02:56:40 GMT  
		Size: 30.2 MB (30185429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c3a1b4fa684906875f7fd4416d71426ac1aee26864470455b1b9b46d7828d`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0df7a4b2868d4940542adb230523d1e4ed001e3b81e5b207cecf42c343f478`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 964.1 KB (964111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b73a1fcb61a5a282a8c9397a8c576b45fbe6caa25857e13ea650cb4d76322a`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef7526f5b3917e2bc638427511d4989ad3248fae4b127cd3e0d33e74a490514`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:4085cd69ad186b4f31b2d00827f60d3f772d59734d0e19d4d610951d1ab3da6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463b46d8bb3fa777b046df54e8e2a1c586a9ffd3aa84723d00aee9899233ec16`

```dockerfile
```

-	Layers:
	-	`sha256:97eddbfc009a7db168669d971a6e5e733e0fc7795c4e86ab74ef4c3805df0df5`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 2.2 MB (2159609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6143674f1e33328ecad90616b50233ba90952a12cf467628257ba949eb7dd771`  
		Last Modified: Fri, 09 May 2025 02:58:18 GMT  
		Size: 30.8 KB (30808 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:3eb81b210445eab75a9596c806a3723d0154537ffbea44e924dd375bd8d46ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74505054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cc127439d34c6f96676db2c801e18e32fe42a8f19167bee613e3cb32a8bdf8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752b27585c21531ef183f9331718681f7d5a399ad1721fe17bf65ec91aa026d`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 3.3 MB (3332291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c504757a74563c6c69cb5f5ab95d450088933adf663323509ef07a437fda44`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64969c8e6dd0ea68ca6e1a455172bdc1ce583b5d543fc3120d33f200e06302a1`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1176f7a4c5fb0e54724b9ad7ea378a6420c35cbfd4d0eeb5e1fef5d9ba7ac`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 13.6 MB (13638372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9788910834fbf94207a3e2b19ab0e6fabbefd4e42d621687e321a1db2f16e53e`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edad5b9c93eee4f4366f3ebeb11225c8f73a2b77b6f9619550727373b01d51f`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 20.5 MB (20506682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aad88073420d66b54ab164736e4f80b7f83ed7afde64e75da65e76a0601f38`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d8baab457dd5125f7b8056acc97da76b6e4aed76359cef6cf89c1be2f9546`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9518d6339aceaab8bbfa04cb293db8787e29591ef024e80b24a882a2c9c8edc0`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 32.0 MB (32036745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e197ccaccec2cf61efc3cdf266d9ef310f66d8e5905a95466247bdefc08c5d4`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63caa9b8a6f65f98bf399b6c0907858c28d179a339fcecce75876a27f8711118`  
		Last Modified: Fri, 09 May 2025 01:11:24 GMT  
		Size: 973.2 KB (973231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c61d014799dc6bf76eb35626076e710fc5e4dda0e4843cb4c5654377f2392d`  
		Last Modified: Fri, 09 May 2025 01:11:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d41ade31de22ec89775e848aa31682bf031124c7194426184d23e224ab3621`  
		Last Modified: Fri, 09 May 2025 01:11:24 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:6e3b0fecd14009a0ff39e9f8ce6e612b0954f575c01f51f0989e4e62849bc904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac85c03c9804fea2906b6da84c95a285730f93e6e58ea7b21c85819ef99cbad`

```dockerfile
```

-	Layers:
	-	`sha256:9b88aeefeff43c9faec75bbdf559e9d233e3f8a104137975bd17b3c8f38e575d`  
		Last Modified: Fri, 09 May 2025 01:11:23 GMT  
		Size: 2.2 MB (2159437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d477695b3b116918cd550b0c4d81ffbfdc9142b846a0ce5cfe1a10827574c8`  
		Last Modified: Fri, 09 May 2025 01:11:22 GMT  
		Size: 30.8 KB (30841 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; 386

```console
$ docker pull composer@sha256:1b5e00fff273c7f8077e9e7e091ee6a8544ca4527c32b4e19652ad679af027ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75393539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b1a4ae43abdf7f81cb2fc374621656b152c7f70595cad0a364c16bbc20ea8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0fee7f3118a5985c2f626fb5b6c58f3e09615e2d0e574b152efa48b96dba0`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 3.4 MB (3379885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0859e481ff1d593c72d70f1d40018ee891c8a85aed61e584093925eef0bcab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b986eab8e8b3e0184edeb69c32c4ed3d8588e109c815e0849b82bb054cacab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7b75ef5fb8c211e5b9a329554b4301d5c6eb7ae9c8b76dc280c611f52936f2`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 13.6 MB (13638340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbb0139bcece2c1bb61243f10b29ef44dfb0038edd4f69191a281fb8695da3`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6161bb22ced62e09258a8f26973e62bc0c0b3f09f6fd571bc8cbf3d57d556`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 21.5 MB (21479578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe4c701feaead74489728c530e52569dea2bd050f15b4c2465b658466d6ea38`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aa3b4dea6bd9bd03e0d1ad21c8a068d7303cd61d25541395be92f12129e0a8`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9d3822fff04ee88d265cf3b2f6fda0935618827f02ccb83caddd149472bfb6`  
		Last Modified: Thu, 08 May 2025 21:49:18 GMT  
		Size: 32.4 MB (32419790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4749bed490bc2e21ca8b7e67d7dca5701af7d8733ff3f555fc28be07dddf67d5`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8991ac628ce8adf7b232be49fdf5f393c12b8036a374619747aa07d1191bf1`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 987.4 KB (987427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67722e7ebd67ddc3ea5804cf2081f36d6624dfd689578ce547276b49702f80d9`  
		Last Modified: Thu, 08 May 2025 21:49:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791cac75c2ce2bdf945782129c08f92674bc6ebae72272ad6dd7372877bd7ca0`  
		Last Modified: Thu, 08 May 2025 21:49:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:38527cd7533c5a71d0bd5adb953746455b3cd43bd38d79e7538ef1d370d857b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22fec3f1104eee0cb88dd02a43136b15cafd5ea020c4a31e3d1d3204f2b2425`

```dockerfile
```

-	Layers:
	-	`sha256:22a0fc51722a9f887d0d979027ed22915615024058d3bf602b7e93f1546298f9`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 2.2 MB (2159068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1463be1cdff852ccf958d429ad3373c183fa577d98d14b778a8846e47cf76edf`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; ppc64le

```console
$ docker pull composer@sha256:8b89c42c4af0e06aefd095dbb34c2619855dac845cb2a01d188b3a77c4bb5d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77372105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068ba4fd3895e50862519de9921b88288ba5328fa9baeb66de3c2f38c5387bfe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e76c061ea4a5ab1435512c8388fd08bd714f08a20a3d13e20958322c1e38c8`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 13.6 MB (13638361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6741176fa79481125f0168dfab2269eb4d272b50ffffa3eb93489fbac4b7e`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baaae08012b74873c8e9eb084b4c040c29cb1b207bf5a13250c34c0533cab9a`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 22.7 MB (22698151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d926e7ce8969775d3b04d34e3a2c99bd3026dadb90880f40e22812f538d9a0c0`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01319ff876f0a90f52b88a0db82b4f34546c97612dc4988123adb15a952cee`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749a6c3d45b6e53322f1fdfcdeff037de2cd648813a8db706c3925473d004f6`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 33.0 MB (32975132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c502c29ed2b1ba6e7fd2c2aa71175f396a9176edb02e55648b6cf8555189787c`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0684f605738b7e5978c5a350d7cbb9885d6e9593c7e5eae0ddbc6ce32c02a22e`  
		Last Modified: Thu, 08 May 2025 23:21:27 GMT  
		Size: 980.3 KB (980290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3865705398f20912aedf7e8109210983ab47fc0c7862afae8288b244efbbfbef`  
		Last Modified: Thu, 08 May 2025 23:21:27 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f2b0dbc52dd18eb4223fdbf933144b2bf9e6aa6dcc618cc87532424c5aa68d`  
		Last Modified: Thu, 08 May 2025 23:21:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:8f25a18ddac3fff471eb1d915aa6b545fef585f2ef4a0c6d6ad5937a012071ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5311e03457df6c7d776932408097f223757d845b04c0928ffacab82f34f399a6`

```dockerfile
```

-	Layers:
	-	`sha256:2d792c31a36378da39476236ad13355e8d2ac4418b7aaa84c3bcab1e1a9bcd08`  
		Last Modified: Thu, 08 May 2025 23:21:26 GMT  
		Size: 2.2 MB (2157848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044e4e017f6b8890a5b64a606fa7abbc89bbaf0beae880d8c34c96c26276b056`  
		Last Modified: Thu, 08 May 2025 23:21:26 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; riscv64

```console
$ docker pull composer@sha256:6e9ec48444ac9558ef69eb1c9f824baf5314522f44538a49e4733ad1b3cd30cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73655710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420af2fb4f88c27b8de5e5a3cd3978d65d51761075b4d2e02e117800af46470c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db7ef0a049248006688e39882ca6ced21701e3d55e7cb2f43eb10572e33c7`  
		Last Modified: Fri, 09 May 2025 01:02:09 GMT  
		Size: 13.6 MB (13638347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ccd5673892b28566480f109c15f00e40dac754b53ccd5b997b3b0f7f75b66a`  
		Last Modified: Fri, 09 May 2025 01:02:06 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0f3c897c5b22a06c34b5e67cc4b30c94cf9e55e8b3176d9f4c5f0408e96f1a`  
		Last Modified: Fri, 09 May 2025 01:02:10 GMT  
		Size: 21.2 MB (21162501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef46c091109b0dad546606ab5e3c6ab60d516a7707483f98fa96053dcda29e`  
		Last Modified: Fri, 09 May 2025 01:02:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b931b251640e1d77e3e5386e76828941f021bb5b7fd085a60db7df564d2db`  
		Last Modified: Fri, 09 May 2025 01:02:08 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d591c20251c0df6262a43882dff69cf24f872cb167d9bd70dbe59ce535d6090`  
		Last Modified: Fri, 09 May 2025 16:04:38 GMT  
		Size: 31.0 MB (31044006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56519a808e922477caef5d3ce688e3619da9f0db1b63ff8ca95f3204fd8facec`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ed4acbc6167d6e65bd61a656d64ead373ef36f1602553fbf264731bfa550c`  
		Last Modified: Fri, 09 May 2025 16:15:00 GMT  
		Size: 971.8 KB (971762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04c9848bde98f1cc4f6e54f5b1c32bc5ba6cc29936f7c082af8d2a54e898813`  
		Last Modified: Fri, 09 May 2025 16:14:59 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7822088e7ffa14e2fabd2259297ef14419e9c93f94af3f4eff289969f1b934`  
		Last Modified: Fri, 09 May 2025 16:15:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:da09a3427cf58ee280cd57b40273df9437aead71dd19144d48010936605c4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d48ba38d8d40fa452f8a26f25e490ec24255f7f8c6e719b130360219859b2f`

```dockerfile
```

-	Layers:
	-	`sha256:7a2527bded2278ba5d2f827638d12324fe5fdeb391d080e59130442d5ebe9735`  
		Last Modified: Fri, 09 May 2025 16:14:59 GMT  
		Size: 2.2 MB (2156790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc040a825e20bb854175bac49728f383c6830a0b9c00ae1216afa7558fcfc0fd`  
		Last Modified: Fri, 09 May 2025 16:14:59 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8.8` - linux; s390x

```console
$ docker pull composer@sha256:dfc7fc645d6a07047a78073623daf44350935a34c1c8566c5dcb95ea1ee9228a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75628873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94efc800e610253d603808a8925143397964e88a27a64a89e35a572b016c1201`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b5f11089bad6dd57e7f9c626829578bab2c83d4a9d3e6c9dd1c73eccd0d96`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 13.6 MB (13638363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925304c10005fd175f8945f9b79556931bf8772002494541acf614752b95348`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbdcbc01a58fa9ca47c12882f0c582c63ddf71a40fbf79fa956decd72f0f45`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 22.2 MB (22248891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234da8b1110c7fe66f09e4181941a3db5f83769849d61bd62db5481617b0183`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e59c13cf761428c460597e931fe7482a363b6b0afb29d60205e1fa1bc0d234`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da82aeb01a0294d366bfecf08eef375887e0728de96b73baf2f614fc770d6ee4`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 31.7 MB (31706531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47454c44bffd2e898699df83390dc5586ecf0cdb8cf4e637dfbe6e862166142`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d135b86d58d8377467d55bf776e53000abc3b9d4bfaed27cf9d02c772ce5d0`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 976.6 KB (976603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed9f8099552b00200734259e0b36ab4f94c39d36a77e29f46335351783611e7`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dd9dc76f2c0e4b853173a0da2d6ad8c31b58983ecf0c6dded53de8ad1eadf4`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8.8` - unknown; unknown

```console
$ docker pull composer@sha256:2923462ef720cfdb712a7c14681218303b60eb1a65b653f0aa292525ac745924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c62a52a3b3a37c11a1613f5091cac4f0aa9b257b133215d731a3f11e79cb27`

```dockerfile
```

-	Layers:
	-	`sha256:ed73a17c8aee94540dd474fc24fb314abd3e712e9df24917150e0160a6d5839f`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 2.2 MB (2156570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967ce814b657814077f50f73fb82037f671822aeb253504f07e43bf74fc2a3a8`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:latest`

```console
$ docker pull composer@sha256:3df281ca83119bff1332f0f5f311960cb16b99238f8273acd965be6bd508aa8e
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
$ docker pull composer@sha256:ec31187cf6de8fbb71d2c493ec704f5b76955a3090b3295adf39f0fd5d1eb479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74513054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539808e605ec8fdd3117a80817d3e99ce4af0c3c34ca931e8f23e5aeeb22aea7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ec51de1f9773447b65e97f0c677dfa7c2c5a643a8e29c2573fa02d440be485`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 3.3 MB (3339405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f347299a473f0f5d9b5f088e95e92fa5f3fdb929eb8c00e8eee8a5e255fa22`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33c8191db1484b005c5fa5405a7076bdae4e90319fa99dc126e7fc70a360264`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a488374895485209654e2f20371d2b15edb0b1e6e389ec7439903ae08bb34`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 13.6 MB (13638342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242d92ffbbeeb68a81285f10e04caea376e536af932c229bac24f4850ead8549`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5f8d392c5efc498dff46eaccd969d3b99752dc1a40cbdbefd63ae52351c93`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 21.0 MB (20961727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69de2e680c8502b2e77e5bfbf4a6121b21f9356fa9b0058eb0967c21456bad`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d926e2db98107193f77ac67f3ebac3c923c205841b5b20f0a86e5c848b2d66`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f35e65c467d6a06e463158b71b59b394f945292ceb3f5085e55d3ef27a4da9d`  
		Last Modified: Thu, 08 May 2025 21:49:23 GMT  
		Size: 31.9 MB (31932834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07970fc96919497974b26ac2861318973a76e07ff79f1b64faed95d351083da0`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa5aa8beb42ce23af82c206ab0a95fc0b8426daa93031c684e7d7da64f5415a`  
		Last Modified: Thu, 08 May 2025 21:49:23 GMT  
		Size: 973.6 KB (973600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98df5a35c2fe3e9c05282183b08d8ceb4ec343e2479353c3d9632a64d7e49b6`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67885e2977d33ff647e990ab306798d84593f91d0fb665528f08b8fbaa1ac723`  
		Last Modified: Thu, 08 May 2025 21:49:23 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:1f0f50d68f9860890b7bd409b5b76951479c5c14b8ed9eab06f2c305a52a3a20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af2d8618c9ebce7af590de1125a08b17d5973e1daa67d8ffe3ee4c3a288764dc`

```dockerfile
```

-	Layers:
	-	`sha256:bfbf90c8d1e9be23a21546ffe91ffc2f2f50be40041df99c9c75cb1b6811922c`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 2.2 MB (2159285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:193dd9351255782fb765b8209163883befcc28d1c1b5707d7382f9976ef17dc5`  
		Last Modified: Thu, 08 May 2025 21:49:22 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:a7dff16e0bdc5c9bc5f24d80b850d263b206479078e2c883dc13d4142261a237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72777249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23cf8efc80624ecf1ae3f6e2946b2059cebcc02c496ccc6963754e090488fc16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce0d04db17a73ca3a7314b885207e80120682c8358368a9254c7f44a7aa2761`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 13.6 MB (13638339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ddeda1f976085a87139c58582b31ac5fd6fc3c900259b39f3163e64bea4ce`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bdf2404f235a46786918527ccb15e5da315bc30edec03f1a23a4d5adbb837c`  
		Last Modified: Thu, 08 May 2025 21:26:22 GMT  
		Size: 19.8 MB (19828990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29e5bd26390c9927b9d705940595b9ccb503518764174068193050a9ee011d3`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837c695d5bcef73c8dfd7be97d8f030b294d365c39fb1ef21f5aec9cebaf695f`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c641fa2ea58cc5073a3f4a40452af3766d1d4eff239fa9c78b7850e692b924`  
		Last Modified: Thu, 08 May 2025 21:56:54 GMT  
		Size: 31.6 MB (31637949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37037a8ef7c2de76decb659167cea10b45dd38661222354aec54af534f7f90e`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d36a7b322939484d5ee5c8e4d2acf6b7e5d10aa83eba813e5aa7ca50ba2756`  
		Last Modified: Thu, 08 May 2025 21:58:05 GMT  
		Size: 973.5 KB (973470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f863439db685c5d731f58b9e7de989a88fa5b917b13af3f5f2d825a19b4ae3a`  
		Last Modified: Thu, 08 May 2025 21:58:05 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a186e1d7e7ee9e9772006a97e08806d1e5b4089ed1161b0a7cd6e680fa291b`  
		Last Modified: Thu, 08 May 2025 21:58:05 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:5b47eb452f6d117c416ce8d5e3a6c87296956ef588e545df40795678b3928543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1083c9aa6c3a0ee50d5c3c12d77d92fc773c9f801866daafc72b1de2f336e464`

```dockerfile
```

-	Layers:
	-	`sha256:3e1e0b06eb56f368894bce8fb4cb9415ad55c94f2959e12dafcfd14f064a3f50`  
		Last Modified: Thu, 08 May 2025 21:58:04 GMT  
		Size: 30.6 KB (30594 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:b14aa8913a1e62db51a228506079460ce6e2033447ed821db51e1762fa8776ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69786310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12189a43195c725265f01f4a102edd3b5c363094476821180a6e4aada55df9d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae53c42a3a934e2af6db5b115410a7b4c6a02cd2b122d00b65d1eca1a41169`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 13.6 MB (13638357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10142d79ada8bf8b882c44da37430c2d14e535a18518bf2925f9f960b71e79`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfab14bb194eab55e2e70f9afc13ee33e4dd21aa21350e1374e86f05fb626af`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 18.8 MB (18755156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da76f291cb0bcd5dc8fc90d909e92ab04c17a7553ef5146ab7e325af2708443`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d3e5b7d935e85e9b31895bd1360c16fb666b189cce4d62af34133ff180412`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df80c80dab935ac507aa56dc704c0803d9d2fcf950397319075ec118fc80934`  
		Last Modified: Fri, 09 May 2025 02:56:40 GMT  
		Size: 30.2 MB (30185429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c3a1b4fa684906875f7fd4416d71426ac1aee26864470455b1b9b46d7828d`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba0df7a4b2868d4940542adb230523d1e4ed001e3b81e5b207cecf42c343f478`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 964.1 KB (964111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b73a1fcb61a5a282a8c9397a8c576b45fbe6caa25857e13ea650cb4d76322a`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ef7526f5b3917e2bc638427511d4989ad3248fae4b127cd3e0d33e74a490514`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:4085cd69ad186b4f31b2d00827f60d3f772d59734d0e19d4d610951d1ab3da6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:463b46d8bb3fa777b046df54e8e2a1c586a9ffd3aa84723d00aee9899233ec16`

```dockerfile
```

-	Layers:
	-	`sha256:97eddbfc009a7db168669d971a6e5e733e0fc7795c4e86ab74ef4c3805df0df5`  
		Last Modified: Fri, 09 May 2025 02:58:19 GMT  
		Size: 2.2 MB (2159609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6143674f1e33328ecad90616b50233ba90952a12cf467628257ba949eb7dd771`  
		Last Modified: Fri, 09 May 2025 02:58:18 GMT  
		Size: 30.8 KB (30808 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:3eb81b210445eab75a9596c806a3723d0154537ffbea44e924dd375bd8d46ef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74505054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61cc127439d34c6f96676db2c801e18e32fe42a8f19167bee613e3cb32a8bdf8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752b27585c21531ef183f9331718681f7d5a399ad1721fe17bf65ec91aa026d`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 3.3 MB (3332291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c504757a74563c6c69cb5f5ab95d450088933adf663323509ef07a437fda44`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64969c8e6dd0ea68ca6e1a455172bdc1ce583b5d543fc3120d33f200e06302a1`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1176f7a4c5fb0e54724b9ad7ea378a6420c35cbfd4d0eeb5e1fef5d9ba7ac`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 13.6 MB (13638372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9788910834fbf94207a3e2b19ab0e6fabbefd4e42d621687e321a1db2f16e53e`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edad5b9c93eee4f4366f3ebeb11225c8f73a2b77b6f9619550727373b01d51f`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 20.5 MB (20506682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aad88073420d66b54ab164736e4f80b7f83ed7afde64e75da65e76a0601f38`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d8baab457dd5125f7b8056acc97da76b6e4aed76359cef6cf89c1be2f9546`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9518d6339aceaab8bbfa04cb293db8787e29591ef024e80b24a882a2c9c8edc0`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 32.0 MB (32036745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e197ccaccec2cf61efc3cdf266d9ef310f66d8e5905a95466247bdefc08c5d4`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63caa9b8a6f65f98bf399b6c0907858c28d179a339fcecce75876a27f8711118`  
		Last Modified: Fri, 09 May 2025 01:11:24 GMT  
		Size: 973.2 KB (973231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c61d014799dc6bf76eb35626076e710fc5e4dda0e4843cb4c5654377f2392d`  
		Last Modified: Fri, 09 May 2025 01:11:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d41ade31de22ec89775e848aa31682bf031124c7194426184d23e224ab3621`  
		Last Modified: Fri, 09 May 2025 01:11:24 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:6e3b0fecd14009a0ff39e9f8ce6e612b0954f575c01f51f0989e4e62849bc904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eac85c03c9804fea2906b6da84c95a285730f93e6e58ea7b21c85819ef99cbad`

```dockerfile
```

-	Layers:
	-	`sha256:9b88aeefeff43c9faec75bbdf559e9d233e3f8a104137975bd17b3c8f38e575d`  
		Last Modified: Fri, 09 May 2025 01:11:23 GMT  
		Size: 2.2 MB (2159437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72d477695b3b116918cd550b0c4d81ffbfdc9142b846a0ce5cfe1a10827574c8`  
		Last Modified: Fri, 09 May 2025 01:11:22 GMT  
		Size: 30.8 KB (30841 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:1b5e00fff273c7f8077e9e7e091ee6a8544ca4527c32b4e19652ad679af027ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75393539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b1a4ae43abdf7f81cb2fc374621656b152c7f70595cad0a364c16bbc20ea8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0fee7f3118a5985c2f626fb5b6c58f3e09615e2d0e574b152efa48b96dba0`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 3.4 MB (3379885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0859e481ff1d593c72d70f1d40018ee891c8a85aed61e584093925eef0bcab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b986eab8e8b3e0184edeb69c32c4ed3d8588e109c815e0849b82bb054cacab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7b75ef5fb8c211e5b9a329554b4301d5c6eb7ae9c8b76dc280c611f52936f2`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 13.6 MB (13638340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbb0139bcece2c1bb61243f10b29ef44dfb0038edd4f69191a281fb8695da3`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6161bb22ced62e09258a8f26973e62bc0c0b3f09f6fd571bc8cbf3d57d556`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 21.5 MB (21479578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe4c701feaead74489728c530e52569dea2bd050f15b4c2465b658466d6ea38`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aa3b4dea6bd9bd03e0d1ad21c8a068d7303cd61d25541395be92f12129e0a8`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9d3822fff04ee88d265cf3b2f6fda0935618827f02ccb83caddd149472bfb6`  
		Last Modified: Thu, 08 May 2025 21:49:18 GMT  
		Size: 32.4 MB (32419790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4749bed490bc2e21ca8b7e67d7dca5701af7d8733ff3f555fc28be07dddf67d5`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8991ac628ce8adf7b232be49fdf5f393c12b8036a374619747aa07d1191bf1`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 987.4 KB (987427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67722e7ebd67ddc3ea5804cf2081f36d6624dfd689578ce547276b49702f80d9`  
		Last Modified: Thu, 08 May 2025 21:49:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791cac75c2ce2bdf945782129c08f92674bc6ebae72272ad6dd7372877bd7ca0`  
		Last Modified: Thu, 08 May 2025 21:49:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:38527cd7533c5a71d0bd5adb953746455b3cd43bd38d79e7538ef1d370d857b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e22fec3f1104eee0cb88dd02a43136b15cafd5ea020c4a31e3d1d3204f2b2425`

```dockerfile
```

-	Layers:
	-	`sha256:22a0fc51722a9f887d0d979027ed22915615024058d3bf602b7e93f1546298f9`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 2.2 MB (2159068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1463be1cdff852ccf958d429ad3373c183fa577d98d14b778a8846e47cf76edf`  
		Last Modified: Thu, 08 May 2025 21:49:17 GMT  
		Size: 30.7 KB (30671 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:8b89c42c4af0e06aefd095dbb34c2619855dac845cb2a01d188b3a77c4bb5d49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77372105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068ba4fd3895e50862519de9921b88288ba5328fa9baeb66de3c2f38c5387bfe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e76c061ea4a5ab1435512c8388fd08bd714f08a20a3d13e20958322c1e38c8`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 13.6 MB (13638361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6741176fa79481125f0168dfab2269eb4d272b50ffffa3eb93489fbac4b7e`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baaae08012b74873c8e9eb084b4c040c29cb1b207bf5a13250c34c0533cab9a`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 22.7 MB (22698151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d926e7ce8969775d3b04d34e3a2c99bd3026dadb90880f40e22812f538d9a0c0`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01319ff876f0a90f52b88a0db82b4f34546c97612dc4988123adb15a952cee`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749a6c3d45b6e53322f1fdfcdeff037de2cd648813a8db706c3925473d004f6`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 33.0 MB (32975132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c502c29ed2b1ba6e7fd2c2aa71175f396a9176edb02e55648b6cf8555189787c`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0684f605738b7e5978c5a350d7cbb9885d6e9593c7e5eae0ddbc6ce32c02a22e`  
		Last Modified: Thu, 08 May 2025 23:21:27 GMT  
		Size: 980.3 KB (980290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3865705398f20912aedf7e8109210983ab47fc0c7862afae8288b244efbbfbef`  
		Last Modified: Thu, 08 May 2025 23:21:27 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f2b0dbc52dd18eb4223fdbf933144b2bf9e6aa6dcc618cc87532424c5aa68d`  
		Last Modified: Thu, 08 May 2025 23:21:27 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:8f25a18ddac3fff471eb1d915aa6b545fef585f2ef4a0c6d6ad5937a012071ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5311e03457df6c7d776932408097f223757d845b04c0928ffacab82f34f399a6`

```dockerfile
```

-	Layers:
	-	`sha256:2d792c31a36378da39476236ad13355e8d2ac4418b7aaa84c3bcab1e1a9bcd08`  
		Last Modified: Thu, 08 May 2025 23:21:26 GMT  
		Size: 2.2 MB (2157848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:044e4e017f6b8890a5b64a606fa7abbc89bbaf0beae880d8c34c96c26276b056`  
		Last Modified: Thu, 08 May 2025 23:21:26 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:6e9ec48444ac9558ef69eb1c9f824baf5314522f44538a49e4733ad1b3cd30cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73655710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:420af2fb4f88c27b8de5e5a3cd3978d65d51761075b4d2e02e117800af46470c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db7ef0a049248006688e39882ca6ced21701e3d55e7cb2f43eb10572e33c7`  
		Last Modified: Fri, 09 May 2025 01:02:09 GMT  
		Size: 13.6 MB (13638347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ccd5673892b28566480f109c15f00e40dac754b53ccd5b997b3b0f7f75b66a`  
		Last Modified: Fri, 09 May 2025 01:02:06 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0f3c897c5b22a06c34b5e67cc4b30c94cf9e55e8b3176d9f4c5f0408e96f1a`  
		Last Modified: Fri, 09 May 2025 01:02:10 GMT  
		Size: 21.2 MB (21162501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef46c091109b0dad546606ab5e3c6ab60d516a7707483f98fa96053dcda29e`  
		Last Modified: Fri, 09 May 2025 01:02:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b931b251640e1d77e3e5386e76828941f021bb5b7fd085a60db7df564d2db`  
		Last Modified: Fri, 09 May 2025 01:02:08 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d591c20251c0df6262a43882dff69cf24f872cb167d9bd70dbe59ce535d6090`  
		Last Modified: Fri, 09 May 2025 16:04:38 GMT  
		Size: 31.0 MB (31044006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56519a808e922477caef5d3ce688e3619da9f0db1b63ff8ca95f3204fd8facec`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6ed4acbc6167d6e65bd61a656d64ead373ef36f1602553fbf264731bfa550c`  
		Last Modified: Fri, 09 May 2025 16:15:00 GMT  
		Size: 971.8 KB (971762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04c9848bde98f1cc4f6e54f5b1c32bc5ba6cc29936f7c082af8d2a54e898813`  
		Last Modified: Fri, 09 May 2025 16:14:59 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7822088e7ffa14e2fabd2259297ef14419e9c93f94af3f4eff289969f1b934`  
		Last Modified: Fri, 09 May 2025 16:15:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:da09a3427cf58ee280cd57b40273df9437aead71dd19144d48010936605c4653
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d48ba38d8d40fa452f8a26f25e490ec24255f7f8c6e719b130360219859b2f`

```dockerfile
```

-	Layers:
	-	`sha256:7a2527bded2278ba5d2f827638d12324fe5fdeb391d080e59130442d5ebe9735`  
		Last Modified: Fri, 09 May 2025 16:14:59 GMT  
		Size: 2.2 MB (2156790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc040a825e20bb854175bac49728f383c6830a0b9c00ae1216afa7558fcfc0fd`  
		Last Modified: Fri, 09 May 2025 16:14:59 GMT  
		Size: 30.8 KB (30755 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:dfc7fc645d6a07047a78073623daf44350935a34c1c8566c5dcb95ea1ee9228a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75628873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94efc800e610253d603808a8925143397964e88a27a64a89e35a572b016c1201`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Apr 2025 06:51:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 07 Apr 2025 06:51:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_VERSION=8.4.7
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Mon, 07 Apr 2025 06:51:49 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["php" "-a"]
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_HOME=/tmp
# Mon, 07 Apr 2025 06:51:49 GMT
ENV COMPOSER_VERSION=2.8.8
# Mon, 07 Apr 2025 06:51:49 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Mon, 07 Apr 2025 06:51:49 GMT
WORKDIR /app
# Mon, 07 Apr 2025 06:51:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 07 Apr 2025 06:51:49 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b5f11089bad6dd57e7f9c626829578bab2c83d4a9d3e6c9dd1c73eccd0d96`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 13.6 MB (13638363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925304c10005fd175f8945f9b79556931bf8772002494541acf614752b95348`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbdcbc01a58fa9ca47c12882f0c582c63ddf71a40fbf79fa956decd72f0f45`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 22.2 MB (22248891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234da8b1110c7fe66f09e4181941a3db5f83769849d61bd62db5481617b0183`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e59c13cf761428c460597e931fe7482a363b6b0afb29d60205e1fa1bc0d234`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da82aeb01a0294d366bfecf08eef375887e0728de96b73baf2f614fc770d6ee4`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 31.7 MB (31706531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47454c44bffd2e898699df83390dc5586ecf0cdb8cf4e637dfbe6e862166142`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d135b86d58d8377467d55bf776e53000abc3b9d4bfaed27cf9d02c772ce5d0`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 976.6 KB (976603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed9f8099552b00200734259e0b36ab4f94c39d36a77e29f46335351783611e7`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dd9dc76f2c0e4b853173a0da2d6ad8c31b58983ecf0c6dded53de8ad1eadf4`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:2923462ef720cfdb712a7c14681218303b60eb1a65b653f0aa292525ac745924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c62a52a3b3a37c11a1613f5091cac4f0aa9b257b133215d731a3f11e79cb27`

```dockerfile
```

-	Layers:
	-	`sha256:ed73a17c8aee94540dd474fc24fb314abd3e712e9df24917150e0160a6d5839f`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 2.2 MB (2156570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:967ce814b657814077f50f73fb82037f671822aeb253504f07e43bf74fc2a3a8`  
		Last Modified: Fri, 09 May 2025 01:21:46 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:lts`

```console
$ docker pull composer@sha256:0d9ad23e2f335bb8e56e259a26626d14ebad2d877a443142187c01e66333682d
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

### `composer:lts` - linux; amd64

```console
$ docker pull composer@sha256:5cebd857e3ad2565b6c39e018c0a65b3a66fbfbd6fbb58740b2ce788c39f249f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74359139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231c9f515480b892e0000d9402534862e6fdf23cebe60072d3a2c64fd0859f3e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ec51de1f9773447b65e97f0c677dfa7c2c5a643a8e29c2573fa02d440be485`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 3.3 MB (3339405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f347299a473f0f5d9b5f088e95e92fa5f3fdb929eb8c00e8eee8a5e255fa22`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a33c8191db1484b005c5fa5405a7076bdae4e90319fa99dc126e7fc70a360264`  
		Last Modified: Thu, 08 May 2025 21:29:34 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a488374895485209654e2f20371d2b15edb0b1e6e389ec7439903ae08bb34`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 13.6 MB (13638342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:242d92ffbbeeb68a81285f10e04caea376e536af932c229bac24f4850ead8549`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5f8d392c5efc498dff46eaccd969d3b99752dc1a40cbdbefd63ae52351c93`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 21.0 MB (20961727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d69de2e680c8502b2e77e5bfbf4a6121b21f9356fa9b0058eb0967c21456bad`  
		Last Modified: Thu, 08 May 2025 21:29:35 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d926e2db98107193f77ac67f3ebac3c923c205841b5b20f0a86e5c848b2d66`  
		Last Modified: Thu, 08 May 2025 21:29:36 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499b35e2befe9a2ab9280b1a602e52457d8ed7f23a90e28ba5c103070decea90`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 31.9 MB (31932681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fb4c279258a28b8cf2f050d72d484d11919bd0c4c3ce9275900c07678241b1`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daa442d79abf31d10e17f14740f25bc7f61abff47dc00e1100471c6c0ab7731`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 819.8 KB (819839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2caefd19b6125c0e3b24e00ee848ae2ef85b2d4cc231044b55e28a7a1052d657`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28726ab0de7dc427015158d773cd922bef15e82c8e80a12f7955f42824dcd0be`  
		Last Modified: Thu, 08 May 2025 21:49:15 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:c72c8e096b9c397677aa31c340536654a174b6044f2c65edffe768a9fcdb81f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3d7e1497fea47c02d1e9662679efc0af0be65bc38ee751d93c6c03cc0635c3`

```dockerfile
```

-	Layers:
	-	`sha256:23a61df6af22091ccd1fe95b53e017a7c279324770176b85f12aff52854b8acb`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 2.2 MB (2158991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66264756f1845409e67c618f4a4ca8168ea6639f52322b61ed8c8fb05415ca91`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:4172dc3dc33e54a3baecc3587408f2221e194b270edcf1478b855668a54403e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72623422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5e19f9283237934aa53cd3933057376364e6d090563214f7a4ed7c49ea76a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 18:28:03 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:02:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce0d04db17a73ca3a7314b885207e80120682c8358368a9254c7f44a7aa2761`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 13.6 MB (13638339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74ddeda1f976085a87139c58582b31ac5fd6fc3c900259b39f3163e64bea4ce`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bdf2404f235a46786918527ccb15e5da315bc30edec03f1a23a4d5adbb837c`  
		Last Modified: Thu, 08 May 2025 21:26:22 GMT  
		Size: 19.8 MB (19828990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29e5bd26390c9927b9d705940595b9ccb503518764174068193050a9ee011d3`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837c695d5bcef73c8dfd7be97d8f030b294d365c39fb1ef21f5aec9cebaf695f`  
		Last Modified: Thu, 08 May 2025 21:26:21 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c641fa2ea58cc5073a3f4a40452af3766d1d4eff239fa9c78b7850e692b924`  
		Last Modified: Thu, 08 May 2025 21:56:54 GMT  
		Size: 31.6 MB (31637949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37037a8ef7c2de76decb659167cea10b45dd38661222354aec54af534f7f90e`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9371ff9c022135cc30cc8b926dc250d9bedccaa330fa7b9b49b2180d26579405`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 819.6 KB (819643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dfe2f1ed4b221efdeb64a6cae996ca1e2b81afcaf99fe70e875345becffb14`  
		Last Modified: Thu, 08 May 2025 21:56:53 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fade42309a9a0da019a91c17d77c28a835444792b767ee061b9340a9e98601`  
		Last Modified: Thu, 08 May 2025 21:56:49 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:ec4d3d379007819868c36dbaa75917c97b6406d4f344ad400c65266f4ed42495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 KB (30282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7ec15c414ca787e4ac72f051579b92506a8bf9462509c15877e043fd19c606`

```dockerfile
```

-	Layers:
	-	`sha256:335cd578e45ca45ad6ba03232eade190f053ea93f1d2ad1192b0482130aaf2e3`  
		Last Modified: Thu, 08 May 2025 21:56:52 GMT  
		Size: 30.3 KB (30282 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:a033f1b78facdd5e0a4c5572ab28a12555f6082ba945bd577e20185521f7d8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69632557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2e2fd5ef57b840623eb18bcf85fccaf61c29b60b7c294d5d40961180ff18a7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 19:44:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49ae53c42a3a934e2af6db5b115410a7b4c6a02cd2b122d00b65d1eca1a41169`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 13.6 MB (13638357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf10142d79ada8bf8b882c44da37430c2d14e535a18518bf2925f9f960b71e79`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfab14bb194eab55e2e70f9afc13ee33e4dd21aa21350e1374e86f05fb626af`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 18.8 MB (18755156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da76f291cb0bcd5dc8fc90d909e92ab04c17a7553ef5146ab7e325af2708443`  
		Last Modified: Thu, 08 May 2025 23:22:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5d3e5b7d935e85e9b31895bd1360c16fb666b189cce4d62af34133ff180412`  
		Last Modified: Thu, 08 May 2025 23:22:18 GMT  
		Size: 19.9 KB (19871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df80c80dab935ac507aa56dc704c0803d9d2fcf950397319075ec118fc80934`  
		Last Modified: Fri, 09 May 2025 02:56:40 GMT  
		Size: 30.2 MB (30185429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c3a1b4fa684906875f7fd4416d71426ac1aee26864470455b1b9b46d7828d`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8513c8b163ee9709e5b3dc3c4a87f1f4594811ef656312a0af412be48d9a71a3`  
		Last Modified: Fri, 09 May 2025 02:56:39 GMT  
		Size: 810.4 KB (810358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f934f90fc13c2bef368b2a479f52aede5fcc42961f5c81a7db6ff1e6c825dc89`  
		Last Modified: Fri, 09 May 2025 02:56:39 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66be4070bf8d4b80b5a8a8b70270241facc3bf78b63e4af4c22a8e567adb61d`  
		Last Modified: Fri, 09 May 2025 02:56:39 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:7a9fc43d076b9bda83778bd6c939613f27e5fe5df60c4dd82ec67b96ee1b1fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff36941efce39e79c925e7ca11bc454085ff33081bc3f4f4c8e1caf4f776e548`

```dockerfile
```

-	Layers:
	-	`sha256:53372f3f7fdb0d6d0a5ceb85baad3547326f5c809570f5e0e8d18d07909da27b`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 2.2 MB (2159307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cc2a070c97eb5d5bb8a4d940d24e54abe8bfe8aee9c97b3c8fb0f8eb0385492`  
		Last Modified: Fri, 09 May 2025 02:56:38 GMT  
		Size: 30.5 KB (30496 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:660a3f96590101779bae7458cc72850e95b0798689489014f57c2f88b66f06a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74351321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1479d7d13817ee69723abf2ab0d58fb9142d8d74aad87e6e04c33b22c11a42bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5752b27585c21531ef183f9331718681f7d5a399ad1721fe17bf65ec91aa026d`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 3.3 MB (3332291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c504757a74563c6c69cb5f5ab95d450088933adf663323509ef07a437fda44`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64969c8e6dd0ea68ca6e1a455172bdc1ce583b5d543fc3120d33f200e06302a1`  
		Last Modified: Thu, 08 May 2025 22:34:00 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc1176f7a4c5fb0e54724b9ad7ea378a6420c35cbfd4d0eeb5e1fef5d9ba7ac`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 13.6 MB (13638372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9788910834fbf94207a3e2b19ab0e6fabbefd4e42d621687e321a1db2f16e53e`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edad5b9c93eee4f4366f3ebeb11225c8f73a2b77b6f9619550727373b01d51f`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 20.5 MB (20506682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aad88073420d66b54ab164736e4f80b7f83ed7afde64e75da65e76a0601f38`  
		Last Modified: Thu, 08 May 2025 22:34:01 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70d8baab457dd5125f7b8056acc97da76b6e4aed76359cef6cf89c1be2f9546`  
		Last Modified: Thu, 08 May 2025 22:34:02 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9518d6339aceaab8bbfa04cb293db8787e29591ef024e80b24a882a2c9c8edc0`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 32.0 MB (32036745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e197ccaccec2cf61efc3cdf266d9ef310f66d8e5905a95466247bdefc08c5d4`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e016548f32a92f4ca21a9b9425d229f0603e50f7331434d48433cf080f21f9d7`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 819.5 KB (819499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918d9b05ba0bc908df65d8242560fbefbfa893916fc6f79a748fd37ea31e7a54`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15dcffea100c734bb9900526c295a50bdf08a6b81c92e61e5a13114d41744a5`  
		Last Modified: Fri, 09 May 2025 01:10:12 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:6657510496ff088eb85b663658ab399924ca08198893202c463c41b3d5e0153c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760f18624eaa94a7e36971327a97cbbb1b9daca6359f96e86096b283526218c5`

```dockerfile
```

-	Layers:
	-	`sha256:83b24749f270a87ef6e8438cb57a5a675bbde85039ac32beb1265124878b6ad7`  
		Last Modified: Fri, 09 May 2025 01:10:11 GMT  
		Size: 2.2 MB (2159131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:488da887497f8349c6b6ffa9c501688798e299f8888b05bcc32bad6f267e3566`  
		Last Modified: Fri, 09 May 2025 01:10:10 GMT  
		Size: 30.5 KB (30525 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:19ea0af1d6d1bf965c8997ebf71e2a92c1313cfe4da8c8647b813f2c0ff4d354
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75239586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05421cc0f995b8c637f983dea20efd577dcb54c35443c3e98b1a8a001470e15`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a0fee7f3118a5985c2f626fb5b6c58f3e09615e2d0e574b152efa48b96dba0`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 3.4 MB (3379885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e0859e481ff1d593c72d70f1d40018ee891c8a85aed61e584093925eef0bcab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b986eab8e8b3e0184edeb69c32c4ed3d8588e109c815e0849b82bb054cacab`  
		Last Modified: Thu, 08 May 2025 21:29:59 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c7b75ef5fb8c211e5b9a329554b4301d5c6eb7ae9c8b76dc280c611f52936f2`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 13.6 MB (13638340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36cbb0139bcece2c1bb61243f10b29ef44dfb0038edd4f69191a281fb8695da3`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc6161bb22ced62e09258a8f26973e62bc0c0b3f09f6fd571bc8cbf3d57d556`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 21.5 MB (21479578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fe4c701feaead74489728c530e52569dea2bd050f15b4c2465b658466d6ea38`  
		Last Modified: Thu, 08 May 2025 21:30:00 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87aa3b4dea6bd9bd03e0d1ad21c8a068d7303cd61d25541395be92f12129e0a8`  
		Last Modified: Thu, 08 May 2025 21:30:01 GMT  
		Size: 20.0 KB (20049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ebfea0ea0e34c30ea6572f9b90a6a82e0b30799b9188503151036d51972dfc`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 32.4 MB (32419650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a210db33b806b55bf805f429c9afe113595174151758714de88d5944b7601285`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040bd3ee25d7721ce0b770039cc202b97b3485095553647d8ffd0ae391e2455d`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 833.6 KB (833619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5069feb63748d630228815c7019641ca31353671475fdf0d0a501f0fcaebbd1`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89ed163134dd5463572f12e039ed75cf48686e844ba79683f8d79735a5d58b2`  
		Last Modified: Thu, 08 May 2025 21:49:14 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:943f12c594a481ac8feb5cd7d2d84cbf3f2a9ecbe7d80ae95f18599fb2a14d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2e6e873d877d21ef07a5f1b9312aa3dd3f5f4f9eb482511f8c09ec0bca70ddc`

```dockerfile
```

-	Layers:
	-	`sha256:b8481db856b3845732b38141065fb355ae9c854c682bd7c3b3c3ab9573541b12`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 2.2 MB (2158779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56e205d10e14e98bd5d46cd83ddb52dd8ae5409e379edfb679a5e6bed943f031`  
		Last Modified: Thu, 08 May 2025 21:49:13 GMT  
		Size: 30.4 KB (30372 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:72c16852f91d422eb2182a913c7a3a2c5a0446ac4ad2f2e89ecf389cdbdcc2c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77218301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af02315b6b038713c7e17f053cd7610afb4fb1e720eaf246c39026433a7a407d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 12:05:34 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 19:49:03 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 19:49:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e76c061ea4a5ab1435512c8388fd08bd714f08a20a3d13e20958322c1e38c8`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 13.6 MB (13638361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd6741176fa79481125f0168dfab2269eb4d272b50ffffa3eb93489fbac4b7e`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0baaae08012b74873c8e9eb084b4c040c29cb1b207bf5a13250c34c0533cab9a`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 22.7 MB (22698151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d926e7ce8969775d3b04d34e3a2c99bd3026dadb90880f40e22812f538d9a0c0`  
		Last Modified: Thu, 08 May 2025 22:06:19 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a01319ff876f0a90f52b88a0db82b4f34546c97612dc4988123adb15a952cee`  
		Last Modified: Thu, 08 May 2025 22:06:20 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749a6c3d45b6e53322f1fdfcdeff037de2cd648813a8db706c3925473d004f6`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 33.0 MB (32975132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c502c29ed2b1ba6e7fd2c2aa71175f396a9176edb02e55648b6cf8555189787c`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1213f256b750bba2e7bd0657305bd6b3c0051bf884d88a9296fdc9e5fb5df62f`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 826.5 KB (826487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438ad093fa93dc3ac1a33833f1f6adfa20ddc4fd7cbc08bc9266819b9912c92d`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fb83f031d4063084ee6ad41d77a9aa0230ae6dbac20f8bbfe5791f043904bc`  
		Last Modified: Thu, 08 May 2025 23:19:35 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:0d981092760d9038f57b80e0550f2ea05b8db146ed6d36079978b4a02355c2a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65716f79cf32c55b9b9759bc9a6c2e8b065f5e03899cceb829f0d35cccb4475`

```dockerfile
```

-	Layers:
	-	`sha256:e4dc5031f55e1793bea9034ae5f9a97bf7713526046d4a2a48c9f199003ab7bf`  
		Last Modified: Thu, 08 May 2025 23:19:34 GMT  
		Size: 2.2 MB (2157548 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b6104183375130c349d21a5b7afadf82202fb96ffdc4fce3c2c738a109b35d8`  
		Last Modified: Thu, 08 May 2025 23:19:33 GMT  
		Size: 30.4 KB (30445 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:3e45c0d2ead036c529d16de92fc3a13fada03e13fd2a7351aa24753702a2924e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.5 MB (73501963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c935e3376691c8c19041e652af0227ca18d7f87c3d5c173401d98cc676a3e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 18:56:36 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 00:30:36 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 00:30:35 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8db7ef0a049248006688e39882ca6ced21701e3d55e7cb2f43eb10572e33c7`  
		Last Modified: Fri, 09 May 2025 01:02:09 GMT  
		Size: 13.6 MB (13638347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ccd5673892b28566480f109c15f00e40dac754b53ccd5b997b3b0f7f75b66a`  
		Last Modified: Fri, 09 May 2025 01:02:06 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0f3c897c5b22a06c34b5e67cc4b30c94cf9e55e8b3176d9f4c5f0408e96f1a`  
		Last Modified: Fri, 09 May 2025 01:02:10 GMT  
		Size: 21.2 MB (21162501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ef46c091109b0dad546606ab5e3c6ab60d516a7707483f98fa96053dcda29e`  
		Last Modified: Fri, 09 May 2025 01:02:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509b931b251640e1d77e3e5386e76828941f021bb5b7fd085a60db7df564d2db`  
		Last Modified: Fri, 09 May 2025 01:02:08 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d591c20251c0df6262a43882dff69cf24f872cb167d9bd70dbe59ce535d6090`  
		Last Modified: Fri, 09 May 2025 16:04:38 GMT  
		Size: 31.0 MB (31044006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56519a808e922477caef5d3ce688e3619da9f0db1b63ff8ca95f3204fd8facec`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 259.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953bf8c3df77e8fe57b1937cc9526c14a038522a1e5032e3be6045e73ab81ab4`  
		Last Modified: Fri, 09 May 2025 16:04:34 GMT  
		Size: 818.0 KB (818016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367b8cf7cb2461e691341dff2d886fa6f87b6aefb113f08f33cf4788e265d189`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c78c0216cdee6b454c8cdb8863ffd3299bcf91e241029e54f6e1476f4f68c6`  
		Last Modified: Fri, 09 May 2025 16:04:34 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:fb04fd51471ffe11168d5634d06301443b94c7d57b1b9d0f48873264aaabff64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9682f06ecfbee994a0ed12df837f984963b9d29fa0a9562995b76e035e2346b`

```dockerfile
```

-	Layers:
	-	`sha256:1dc3c19f202f7b1dd1ce67d2c5430e24b2456e53f134af60077f4e606f23c218`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 2.2 MB (2156490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7f8042d631bf40f857397cbf513b0b780fd77689f4dae04133f028a038394e6`  
		Last Modified: Fri, 09 May 2025 16:04:33 GMT  
		Size: 30.4 KB (30444 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:7bfe50b3671831613ee1f293639da1fd1f01fa55d84992aca6751d6e4fbe1a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75475056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2c6021afa836797deb5b72b3b47ecbb83eec4fc77622fcf8461a07fb89ab0ca`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Tue, 14 Jan 2025 08:39:14 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["/bin/sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 14 Jan 2025 08:39:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 14 Jan 2025 08:39:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_VERSION=8.4.7
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.7.tar.xz.asc
# Tue, 14 Jan 2025 08:39:14 GMT
ENV PHP_SHA256=e29f4c23be2816ed005aa3f06bbb8eae0f22cc133863862e893515fc841e65e3
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["php" "-a"]
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     7zip     bash     coreutils     git     make     mercurial     openssh-client     patch     subversion     tini     unzip     zip # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_HOME=/tmp
# Tue, 14 Jan 2025 08:39:14 GMT
ENV COMPOSER_VERSION=2.2.25
# Tue, 14 Jan 2025 08:39:14 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Tue, 14 Jan 2025 08:39:14 GMT
WORKDIR /app
# Tue, 14 Jan 2025 08:39:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Jan 2025 08:39:14 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 12:05:25 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa956d396b0345789b0b8754caea46d8279eb9aaef195e5c0751997771bc98b`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 3.6 MB (3566207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aa28a25dd21eb15acefc90a9671a91830929d27b461de939eaa00e611391d4d`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd758f782beaedae4bd78b431d2d8eec0ec738f9e5330203a2fb129e7a6b5dda`  
		Last Modified: Fri, 14 Feb 2025 19:52:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4b5f11089bad6dd57e7f9c626829578bab2c83d4a9d3e6c9dd1c73eccd0d96`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 13.6 MB (13638363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b925304c10005fd175f8945f9b79556931bf8772002494541acf614752b95348`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dbdcbc01a58fa9ca47c12882f0c582c63ddf71a40fbf79fa956decd72f0f45`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 22.2 MB (22248891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7234da8b1110c7fe66f09e4181941a3db5f83769849d61bd62db5481617b0183`  
		Last Modified: Thu, 08 May 2025 22:09:14 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e59c13cf761428c460597e931fe7482a363b6b0afb29d60205e1fa1bc0d234`  
		Last Modified: Thu, 08 May 2025 22:09:15 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da82aeb01a0294d366bfecf08eef375887e0728de96b73baf2f614fc770d6ee4`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 31.7 MB (31706531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47454c44bffd2e898699df83390dc5586ecf0cdb8cf4e637dfbe6e862166142`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f001bcf190f1fb778666f3f658ef2ed9f3e7cab2f0dd096abccd8d41e420887`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 822.8 KB (822788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22faf1bf6e162c31468e05c5bed67a6d31776a496807135f9bbb88cd48ec9ba`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1153a0c4e09017b1231e31c9d4696db651f6dd9cbc383d6faee4043eb19125`  
		Last Modified: Fri, 09 May 2025 01:20:24 GMT  
		Size: 92.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:12753622ea89684fc5c480e1298186a4f71e0a052753e875604ef2f466c92ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bff5a88081a75b88c0a41714efba5b65b3a2c2ecb54dcd3f0daa936b12dd36c1`

```dockerfile
```

-	Layers:
	-	`sha256:6de6d8da654c798ae27d488e5d2d34ca32633d4669fabc9a2b049fe472f746bc`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 2.2 MB (2156276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d2b7057a9bea3d0eb01c138e28c2600d46bef824398de4a7790959d3fd6b1e`  
		Last Modified: Fri, 09 May 2025 01:20:23 GMT  
		Size: 30.4 KB (30403 bytes)  
		MIME: application/vnd.in-toto+json
