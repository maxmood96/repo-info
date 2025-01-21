<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `composer`

-	[`composer:1`](#composer1)
-	[`composer:1.10`](#composer110)
-	[`composer:1.10.27`](#composer11027)
-	[`composer:2`](#composer2)
-	[`composer:2.2`](#composer22)
-	[`composer:2.2.25`](#composer2225)
-	[`composer:2.8`](#composer28)
-	[`composer:2.8.5`](#composer285)
-	[`composer:latest`](#composerlatest)
-	[`composer:lts`](#composerlts)

## `composer:1`

```console
$ docker pull composer@sha256:09bc7fee35a9138e8fd8c270a778dcee00a8593b4c59001ea54186ec153b3725
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
$ docker pull composer@sha256:768215cde03ed7f4d09c35404b056c78653cb3eb5993ffe627c960b82e840fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74635922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2877408cd5e3b4152f4f6d1a0611bc007583a47ba7e476a1b009d61576769601`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79c0dc8060e2f059662ca297aa3feae6b3652e5ce0ab171e72b087bec9eb496`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 3.3 MB (3333627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c72c57155ad8b911527445f9878aaf9a4be98da1365dc25227d456bbc357591`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235f6cd368cc120d2abc4c6cb424fde285daf59e2c3f78c72eaa5d14143b8ca`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abdd5367cc40b78b668ff086497ce457af0e483ed80d43df0d8939be0777869`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 13.6 MB (13591519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774922f802bd2f5aeddab05459b4faa03b0664c923d4d04e30d5a5d016662437`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245938a8f085f24c8cf3660fa4370cfad0223a42c79a99e915bbe89ff2910aeb`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.9 MB (20889503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893a8e1213f3e7623f34d6436a30f720ae4cb772c2bdb4e1308dd1333693fee2`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd82ceb5444495c6039a1591b24bb6cde1dd739805a599f07047bbac0e1e9ef`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4e043d9e29c69239ba1132e2798df426a1fdfd2810df74d28f1f634fc52781`  
		Last Modified: Fri, 17 Jan 2025 18:29:26 GMT  
		Size: 31.9 MB (31897535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3ac59736f5bfc588754b0cdb23c4908b225c6f7513e4b36f979806350dc13`  
		Last Modified: Fri, 17 Jan 2025 18:29:25 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91eef26589c2e0534fdaf247c9dedb7ccefe830751f9a9592ddf5f3b6a9b12e7`  
		Last Modified: Fri, 17 Jan 2025 18:29:25 GMT  
		Size: 1.3 MB (1257146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6798583195f68cec585365a4e55a39f4cc42c0d68844ce31f316ee6345adec`  
		Last Modified: Fri, 17 Jan 2025 18:29:25 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039d761834a9bc230994f8758a9ce0d6fce13e09040f053b05f1c6c0cbbb311b`  
		Last Modified: Fri, 17 Jan 2025 18:29:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:970c4faaee6feee3e5579e424615c069cd40c05afd7afc41423a33b6f34b58fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189b197a6c0e473d9324b110fbb641b4e9d6ac53df3337561c6ea9b1f3fc2906`

```dockerfile
```

-	Layers:
	-	`sha256:b0d4fe55feef5e24aabd607f549b5f70314ad8f83fae06efb004d3a44c8c5bba`  
		Last Modified: Fri, 17 Jan 2025 18:29:24 GMT  
		Size: 2.2 MB (2157759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee887a60bd6d5b4ade8cda77941cfd7777c0865a8335d4c00813f5dc793309e6`  
		Last Modified: Fri, 17 Jan 2025 18:29:24 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v6

```console
$ docker pull composer@sha256:e7d25df986db56a16c42bf9d1146d18cf46c0831ef1d7f1b4f0b90be0f3b3e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70684825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f083abe1f39fc1ed772ef6dd504c615898b51b4eb02dbf8dcccc1bb082e7e169`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 08 Jan 2025 18:49:59 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c35832122daf4e6cfd46f0be114a1c6d91b28caceb8f9b86ccb0253e0678632`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 13.6 MB (13591522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abac4d6df3f8471bdecc32831cfc97f2c065ebc58af29566d6e67161775d19e0`  
		Last Modified: Fri, 17 Jan 2025 17:36:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2e9c673c0e2f9934f576e177ae7ca6da19e281e8237523ec2deaddd3b94bb9`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.0 MB (19026889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fed1b7e2d514321545f15b0b6088794d7792c9f6d76c05ea93a61a505107b0`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f1b1f6a6b1a43d58472514b514bd3dc9e1bea6c950d8157396f5af086179d`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1602695904d94b7c906ed6ec74d99f418f62b6c4568fbbad2ab38440a9d1523f`  
		Last Modified: Fri, 17 Jan 2025 18:28:47 GMT  
		Size: 30.6 MB (30642262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e61ca26b0794a9473633a58d896e1b0db4d23c3019d4bf7c5501224de9ae50`  
		Last Modified: Fri, 17 Jan 2025 18:28:46 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5059976bdb25c5aaa39cfcac2c9eb8816257c984039a88f8d7cb1b415d2e5126`  
		Last Modified: Fri, 17 Jan 2025 18:29:22 GMT  
		Size: 735.1 KB (735085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceec54fcb2477b469f9dca645219b218dc16b9abef7401105c9053f18e97c13`  
		Last Modified: Thu, 12 Dec 2024 01:10:16 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250d615bccc5eb6d9bdac6d6c423eeeeb190758abb44c2f0824e8bdf282080e7`  
		Last Modified: Fri, 17 Jan 2025 18:29:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:dd71c89033641a4688e1e9decb2306a4345b7402cc85996dddbed7af6f4d085f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ed269b877f1428a0d110692457a0acca5a18c895d6c1fe8479f3f120f0fc35`

```dockerfile
```

-	Layers:
	-	`sha256:c7cc6ca60272946a2a64e5825627c05fad96a03fa341a71d2839f3f85ce42bf4`  
		Last Modified: Fri, 17 Jan 2025 18:29:21 GMT  
		Size: 30.5 KB (30543 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm variant v7

```console
$ docker pull composer@sha256:8b3b0f6f411a9e87e16f33e755595580999498ccf68531b8cfdaf0dfeb4ced77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68714221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e87efbb9e62c9c58dfe8709dce42c8e011bf3338bd86b05d486befd4c9e554f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd50b568401204c1289c16767a7acc4d1073b759b096a454b243856d0c372e8`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 30.2 MB (30150787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653d3258e5cf9a2c21ab7508e95c806af126ebe35e115ff9cb054bdfc47dad1`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0fde7ef9d30daad0a1ebf2abdd94642a82f6cbc2352eac9aea823092a8a1bd`  
		Last Modified: Fri, 17 Jan 2025 19:01:00 GMT  
		Size: 726.0 KB (725970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b380156e47baddf486b12e44bc2186ae9e8805cd77ce915c9543262f8b7453fc`  
		Last Modified: Fri, 17 Jan 2025 19:01:00 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4df7a48018e36dde3d10f5f5d4961f84d2a063350abc23a0e3c1fe36e393ae`  
		Last Modified: Fri, 17 Jan 2025 19:01:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:7095211436838685445b19febee7863a872e77ac77333fcf0c9d89dad2890bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c2e8d5309e6ef34a1aa41831f1481a09ce1a8eadec6d2a942918c016835c43`

```dockerfile
```

-	Layers:
	-	`sha256:b40158dd770afa7b112486e8d5a30050cb36abe66727e2399a74e11b25262be7`  
		Last Modified: Fri, 17 Jan 2025 19:00:59 GMT  
		Size: 2.2 MB (2158069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3fc77de0b178aa79a8c9d98ebf50c0ce7065e6ac4dac8dfb3690e10ecbe3d1`  
		Last Modified: Fri, 17 Jan 2025 19:00:58 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:77812cb369d8a42db041efba9da530a542b3468a087e68919111612427ff67f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74113901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a124fca3ddc8f759c944c1685729a500ede9dfadde178742e010986b067492`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ded2f1970092c503a682b521201d635e8da0ad60d85a3975060091b0f092d`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 13.6 MB (13591559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12833fff26b4ea2cc381b02e1323f22bd1ac14a4e52a6c8417bbaa55152bd4e`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c693c7cf8097154c6af6b666782076f82f2824477b99c90ff0ca4adb3dbf3cb`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 20.4 MB (20438477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a526ad694be5912a4e8430a6cc668e490cde1f20e6e2b3b004536d3c0a679c`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092dc5a53c2e0204ffcfdfa51a695d5cd5bce5efd0d5d3a58243608a7c6b688`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb5a4ba752055d65a4614132f2cf5a9e53ce62b1e4d38c29a132319b331092`  
		Last Modified: Fri, 17 Jan 2025 18:51:48 GMT  
		Size: 32.0 MB (32004216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99ebc1999608761928e8f7869e0332f0652885f6d3ec81a815c3af8606c258f`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb6be86afb4f93600a29aff19b90dce61e601afb134a82bdff8673e51abeb2f`  
		Last Modified: Fri, 17 Jan 2025 18:52:23 GMT  
		Size: 734.9 KB (734915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45981721fe0761a0305dd59f9567caaeef46fd464382ae34114b490fc61ebda`  
		Last Modified: Fri, 17 Jan 2025 18:52:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0ba0a229a3e08dcbca879697901952658e1635ba1f5fe872a5d5923c75b758`  
		Last Modified: Fri, 17 Jan 2025 18:52:24 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:cb7b3fc12e8b6a5644d753ada86e70c00c3e366ad04086de20b2d0ce449f8113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672654cb1f7512b60382c69c99a8d3d9612d42e790446e3ccdff6d58ca99843`

```dockerfile
```

-	Layers:
	-	`sha256:010ac6c4a92f0a1b0210b7a80f91903d77525cece3840618252e3ed4c20e7985`  
		Last Modified: Fri, 17 Jan 2025 18:52:23 GMT  
		Size: 2.2 MB (2157893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a58bc5ee847bd99d01c14b8acd94d0b00780ecb7dced4bcab3c893f9a9e41c1`  
		Last Modified: Fri, 17 Jan 2025 18:52:22 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; 386

```console
$ docker pull composer@sha256:0376015388eb0c4e0e2a048353fb4a996d0e14a72b20a8a32b25abee8fa607fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54517309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ec4296bf1615a63f52a61f4cb8b8f8a34dbb9c8052dd9201393b6deecb7083`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfcabeec76e82e774d4a80656efdfc79ff8f40c450fbdd73dd3f9950ceb81d`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 3.4 MB (3373778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d250fddeb1debe229bb3f39f26177002aa97298c86687390ec93c5560a19f`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211adc87542ef1dd59501ad1b38031188049730b7b2712675469c23330a736`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87e5b0c31577e6cc14f074a34f293cf80c8700b2325895b1e60d511618578a6`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 13.6 MB (13591509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c7e04c7c5fc0f3187954b25a758a9d80b000947e870a1b160927dca9d40ea`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7c2a142bbfe468340f79a720467957f43a6f702651de57e539baba60bed9ab`  
		Last Modified: Fri, 17 Jan 2025 17:35:40 GMT  
		Size: 21.4 MB (21405219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6e9c16628bd2c485e0f707d1d17f8bd3395400810810ed37be2ba3c51eb6b1`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac723b08e7819bbfef249f592e8c7e989e37423caf36f3a55b17f82f9725fd7d`  
		Last Modified: Fri, 17 Jan 2025 17:35:37 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039f95d894bab1fa4ff121b492e15e7ee19f40e390b76e7839f85f6411bf38d8`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 11.4 MB (11422368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82585710f86585eabf5cb54a38c2dd44a7876261824901a409a9b0dc169798af`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4487baf956c2f025d48f2673806357c7fc1f5620a9265de115efffe49bc764e`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 1.2 MB (1236422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7bd854aabd0a2be0fff545908290c973dddcd4a4a064ab3ea153c014e30d7d`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223b48ae68b36774e967c010f79283db40f684a386ec7f5fb0e403aae38af24f`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:1a5276be0fc84fee553c0e65252ced541c4f810d88bc429436495a188554c567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.1 KB (458053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d7f97ebdb452a45afc57bfd5812adb0cf04f79c1ae7c2e03dd335e168587b2`

```dockerfile
```

-	Layers:
	-	`sha256:dbfaa1eb952ce4ad49fbacf43c8a18369822fb722b28f00b107f126878ec5a5e`  
		Last Modified: Fri, 17 Jan 2025 18:29:05 GMT  
		Size: 427.4 KB (427417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49fb341e1f0d26d169dc3c74c686ca6eb9c597b41661074bbe601e243dafd32b`  
		Last Modified: Fri, 17 Jan 2025 18:29:05 GMT  
		Size: 30.6 KB (30636 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; ppc64le

```console
$ docker pull composer@sha256:4b1513c51938e1e558a81d04eb6a26b69f7ee308ffedb7b97be2e53592a9aef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76713347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495bbf873098d8ac889d964bfa7662517a4975ad063d0b1914484b54b3d748ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b4383e34608c265e3fcbc92f32f5b8e945fc93e6ecdaee910fa87b61b91eb7`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 13.6 MB (13591557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e98b79c382ca554316b5d1b58a69661a67bd73dd451dd9abba75515417cbf`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127935b1403b47049e26eb8a451d0fe15bf3dad3927f479ecfaea54a6026fc5`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 21.8 MB (21795018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8ff0ba33694c0f44258826a3874aaba09beb6072bf0353bb8c47363c0352c`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a75fc421d956d999c53c8003d5e0e6d664732d35993de12ae6e2232c4b9f1da`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63365f65e1acf2e91a180d560297bef7c52ed1b068a3ac5e41cfcab736a1edad`  
		Last Modified: Fri, 17 Jan 2025 18:37:26 GMT  
		Size: 32.9 MB (32944628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7bf30775a0bd0ff25c3418afea9aaee7ede8783e218f3d3368cc426b619c01`  
		Last Modified: Fri, 17 Jan 2025 18:37:24 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c8e9b27017ce878482f1789c56f8497d435632e60a3bcb029134995e689eda`  
		Last Modified: Fri, 17 Jan 2025 18:38:21 GMT  
		Size: 1.3 MB (1307492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8bd6d927ede2ec84d0c0b3185d20fdc1526bf4c1957b5d69fdb45aa13281f2`  
		Last Modified: Fri, 17 Jan 2025 18:38:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6515f866130a388a57f354d33c5779cee51867f353aa30695d0a91d5cea029d`  
		Last Modified: Fri, 17 Jan 2025 18:38:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:0c67da5cacd80b8a253de1e63275c282be6c0221287f164cbb129dee534dea1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f6ccbf6b17ce696826a17ec2ab3f204754f0ba82d8343caba49f3a4dbf4075`

```dockerfile
```

-	Layers:
	-	`sha256:2f36f16717dbb53739dfe52c7ad1c0ad7cb4558cbfe12369170e7809d1280d1f`  
		Last Modified: Fri, 17 Jan 2025 18:38:20 GMT  
		Size: 2.2 MB (2156316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e492c096763a9fcc7e4791995cee96f7444d911462be7b6a96b4dd0cc39aa6ba`  
		Last Modified: Fri, 17 Jan 2025 18:38:20 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; riscv64

```console
$ docker pull composer@sha256:ee152e540432328e13108ec84afc015bf23dea64c7c04999d749e4d8c9b2b32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73035699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be6a8fb02be39fef30f354d98422c35bc79aa3b42ef9c794e876be6af62532c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 08 Jan 2025 23:26:57 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 19:26:15 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 19:26:16 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 19:26:14 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680962a19a25c3960d22cb3a10ea5a2197502ebe67fe87e93e01d571dc161d6`  
		Last Modified: Sat, 18 Jan 2025 02:16:46 GMT  
		Size: 31.0 MB (31000955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b510b40be7ea214b9ab25bd8ec441bf4b4f4d23b112019f368e2f69c97d3d`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ec0aab3bdf7a4e1fe4171af27392c3d118447e7070479ab154572734d9656b`  
		Last Modified: Sat, 18 Jan 2025 02:21:56 GMT  
		Size: 1.3 MB (1290080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b0f62f350e1e191b43d7e26196f7292ec4e3fd421fe6c59272281b34608c9b`  
		Last Modified: Sat, 18 Jan 2025 02:21:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4f3ee911bd3c8e3bda361ed3f502b76a9137e1309ecccce81a8336ea76e4a2`  
		Last Modified: Sat, 18 Jan 2025 02:21:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:f3303d58c9797d5f86efe787f3572a89512aa4848e0a9484dc2cd4e76f518270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41278b70823d827c32e4f578569af2aaede160d87a2c47cfef7b2bd2ad43b0e7`

```dockerfile
```

-	Layers:
	-	`sha256:58f466d74e8cb7002f72a2b9fd5af89bf2e6d04dd606e459cc2d41f6b8a712c0`  
		Last Modified: Sat, 18 Jan 2025 02:21:55 GMT  
		Size: 2.2 MB (2155258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:445e66973e632c38a4c006d379e93b9e1114018a8f1d9226188b471fd3fb87c0`  
		Last Modified: Sat, 18 Jan 2025 02:21:55 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1` - linux; s390x

```console
$ docker pull composer@sha256:7e20ac6fe79289732b6d393e54889ee4a0e251cd79f6d4367569469cc393694c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74994761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ef62539726071388045d696014e2e66c53f88c217ed47cb5349456040f84cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd3b180b852bfd68493c7e27214dde2fc3d4e836aabe9023ed45c8fb27e3e51`  
		Last Modified: Fri, 17 Jan 2025 19:06:19 GMT  
		Size: 31.7 MB (31677476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bc62e74286362c0d45e020cba1c516cb4c2cc297b67f803d103e9b29f070d`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd10dc6b34f98694f6877d29a7b58697c521ca6dc72ccba1904e9170fbe552`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 1.3 MB (1298930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a530e29e1832e69abdb289f76419ea77a583ded99364e9f2d0ab65f9e1a60bb1`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f65dc591f0b96d19aa98ad0c539cae4cdb1d37b80384762d209c867ee257ab`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1` - unknown; unknown

```console
$ docker pull composer@sha256:3b5664a2a00286d481e2893f726d1da9dbf225086d0eeb090b1cae448ff9d2a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c1398be2d4d8444f400d2f004eb60389bbd5f2971545adbfffb4c21bc9ffe3`

```dockerfile
```

-	Layers:
	-	`sha256:9a77f7d6776dedb5112d71772250eda1bfccf0fb2406a812267916ccb4ff48b6`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 2.2 MB (2155044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c9859306194382d74ac07a37236c26b27e93bebd140cdcb7032e817c5a1b3f`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 30.7 KB (30666 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10`

```console
$ docker pull composer@sha256:09bc7fee35a9138e8fd8c270a778dcee00a8593b4c59001ea54186ec153b3725
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
$ docker pull composer@sha256:768215cde03ed7f4d09c35404b056c78653cb3eb5993ffe627c960b82e840fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74635922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2877408cd5e3b4152f4f6d1a0611bc007583a47ba7e476a1b009d61576769601`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79c0dc8060e2f059662ca297aa3feae6b3652e5ce0ab171e72b087bec9eb496`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 3.3 MB (3333627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c72c57155ad8b911527445f9878aaf9a4be98da1365dc25227d456bbc357591`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235f6cd368cc120d2abc4c6cb424fde285daf59e2c3f78c72eaa5d14143b8ca`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abdd5367cc40b78b668ff086497ce457af0e483ed80d43df0d8939be0777869`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 13.6 MB (13591519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774922f802bd2f5aeddab05459b4faa03b0664c923d4d04e30d5a5d016662437`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245938a8f085f24c8cf3660fa4370cfad0223a42c79a99e915bbe89ff2910aeb`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.9 MB (20889503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893a8e1213f3e7623f34d6436a30f720ae4cb772c2bdb4e1308dd1333693fee2`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd82ceb5444495c6039a1591b24bb6cde1dd739805a599f07047bbac0e1e9ef`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4e043d9e29c69239ba1132e2798df426a1fdfd2810df74d28f1f634fc52781`  
		Last Modified: Fri, 17 Jan 2025 18:29:26 GMT  
		Size: 31.9 MB (31897535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3ac59736f5bfc588754b0cdb23c4908b225c6f7513e4b36f979806350dc13`  
		Last Modified: Fri, 17 Jan 2025 18:29:25 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91eef26589c2e0534fdaf247c9dedb7ccefe830751f9a9592ddf5f3b6a9b12e7`  
		Last Modified: Fri, 17 Jan 2025 18:29:25 GMT  
		Size: 1.3 MB (1257146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6798583195f68cec585365a4e55a39f4cc42c0d68844ce31f316ee6345adec`  
		Last Modified: Fri, 17 Jan 2025 18:29:25 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039d761834a9bc230994f8758a9ce0d6fce13e09040f053b05f1c6c0cbbb311b`  
		Last Modified: Fri, 17 Jan 2025 18:29:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:970c4faaee6feee3e5579e424615c069cd40c05afd7afc41423a33b6f34b58fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189b197a6c0e473d9324b110fbb641b4e9d6ac53df3337561c6ea9b1f3fc2906`

```dockerfile
```

-	Layers:
	-	`sha256:b0d4fe55feef5e24aabd607f549b5f70314ad8f83fae06efb004d3a44c8c5bba`  
		Last Modified: Fri, 17 Jan 2025 18:29:24 GMT  
		Size: 2.2 MB (2157759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee887a60bd6d5b4ade8cda77941cfd7777c0865a8335d4c00813f5dc793309e6`  
		Last Modified: Fri, 17 Jan 2025 18:29:24 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v6

```console
$ docker pull composer@sha256:e7d25df986db56a16c42bf9d1146d18cf46c0831ef1d7f1b4f0b90be0f3b3e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70684825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f083abe1f39fc1ed772ef6dd504c615898b51b4eb02dbf8dcccc1bb082e7e169`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 08 Jan 2025 18:49:59 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c35832122daf4e6cfd46f0be114a1c6d91b28caceb8f9b86ccb0253e0678632`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 13.6 MB (13591522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abac4d6df3f8471bdecc32831cfc97f2c065ebc58af29566d6e67161775d19e0`  
		Last Modified: Fri, 17 Jan 2025 17:36:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2e9c673c0e2f9934f576e177ae7ca6da19e281e8237523ec2deaddd3b94bb9`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.0 MB (19026889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fed1b7e2d514321545f15b0b6088794d7792c9f6d76c05ea93a61a505107b0`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f1b1f6a6b1a43d58472514b514bd3dc9e1bea6c950d8157396f5af086179d`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1602695904d94b7c906ed6ec74d99f418f62b6c4568fbbad2ab38440a9d1523f`  
		Last Modified: Fri, 17 Jan 2025 18:28:47 GMT  
		Size: 30.6 MB (30642262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e61ca26b0794a9473633a58d896e1b0db4d23c3019d4bf7c5501224de9ae50`  
		Last Modified: Fri, 17 Jan 2025 18:28:46 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5059976bdb25c5aaa39cfcac2c9eb8816257c984039a88f8d7cb1b415d2e5126`  
		Last Modified: Fri, 17 Jan 2025 18:29:22 GMT  
		Size: 735.1 KB (735085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceec54fcb2477b469f9dca645219b218dc16b9abef7401105c9053f18e97c13`  
		Last Modified: Thu, 12 Dec 2024 01:10:16 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250d615bccc5eb6d9bdac6d6c423eeeeb190758abb44c2f0824e8bdf282080e7`  
		Last Modified: Fri, 17 Jan 2025 18:29:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:dd71c89033641a4688e1e9decb2306a4345b7402cc85996dddbed7af6f4d085f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ed269b877f1428a0d110692457a0acca5a18c895d6c1fe8479f3f120f0fc35`

```dockerfile
```

-	Layers:
	-	`sha256:c7cc6ca60272946a2a64e5825627c05fad96a03fa341a71d2839f3f85ce42bf4`  
		Last Modified: Fri, 17 Jan 2025 18:29:21 GMT  
		Size: 30.5 KB (30543 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm variant v7

```console
$ docker pull composer@sha256:8b3b0f6f411a9e87e16f33e755595580999498ccf68531b8cfdaf0dfeb4ced77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68714221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e87efbb9e62c9c58dfe8709dce42c8e011bf3338bd86b05d486befd4c9e554f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd50b568401204c1289c16767a7acc4d1073b759b096a454b243856d0c372e8`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 30.2 MB (30150787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653d3258e5cf9a2c21ab7508e95c806af126ebe35e115ff9cb054bdfc47dad1`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0fde7ef9d30daad0a1ebf2abdd94642a82f6cbc2352eac9aea823092a8a1bd`  
		Last Modified: Fri, 17 Jan 2025 19:01:00 GMT  
		Size: 726.0 KB (725970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b380156e47baddf486b12e44bc2186ae9e8805cd77ce915c9543262f8b7453fc`  
		Last Modified: Fri, 17 Jan 2025 19:01:00 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4df7a48018e36dde3d10f5f5d4961f84d2a063350abc23a0e3c1fe36e393ae`  
		Last Modified: Fri, 17 Jan 2025 19:01:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:7095211436838685445b19febee7863a872e77ac77333fcf0c9d89dad2890bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c2e8d5309e6ef34a1aa41831f1481a09ce1a8eadec6d2a942918c016835c43`

```dockerfile
```

-	Layers:
	-	`sha256:b40158dd770afa7b112486e8d5a30050cb36abe66727e2399a74e11b25262be7`  
		Last Modified: Fri, 17 Jan 2025 19:00:59 GMT  
		Size: 2.2 MB (2158069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3fc77de0b178aa79a8c9d98ebf50c0ce7065e6ac4dac8dfb3690e10ecbe3d1`  
		Last Modified: Fri, 17 Jan 2025 19:00:58 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:77812cb369d8a42db041efba9da530a542b3468a087e68919111612427ff67f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74113901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a124fca3ddc8f759c944c1685729a500ede9dfadde178742e010986b067492`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ded2f1970092c503a682b521201d635e8da0ad60d85a3975060091b0f092d`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 13.6 MB (13591559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12833fff26b4ea2cc381b02e1323f22bd1ac14a4e52a6c8417bbaa55152bd4e`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c693c7cf8097154c6af6b666782076f82f2824477b99c90ff0ca4adb3dbf3cb`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 20.4 MB (20438477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a526ad694be5912a4e8430a6cc668e490cde1f20e6e2b3b004536d3c0a679c`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092dc5a53c2e0204ffcfdfa51a695d5cd5bce5efd0d5d3a58243608a7c6b688`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb5a4ba752055d65a4614132f2cf5a9e53ce62b1e4d38c29a132319b331092`  
		Last Modified: Fri, 17 Jan 2025 18:51:48 GMT  
		Size: 32.0 MB (32004216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99ebc1999608761928e8f7869e0332f0652885f6d3ec81a815c3af8606c258f`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb6be86afb4f93600a29aff19b90dce61e601afb134a82bdff8673e51abeb2f`  
		Last Modified: Fri, 17 Jan 2025 18:52:23 GMT  
		Size: 734.9 KB (734915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45981721fe0761a0305dd59f9567caaeef46fd464382ae34114b490fc61ebda`  
		Last Modified: Fri, 17 Jan 2025 18:52:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0ba0a229a3e08dcbca879697901952658e1635ba1f5fe872a5d5923c75b758`  
		Last Modified: Fri, 17 Jan 2025 18:52:24 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:cb7b3fc12e8b6a5644d753ada86e70c00c3e366ad04086de20b2d0ce449f8113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672654cb1f7512b60382c69c99a8d3d9612d42e790446e3ccdff6d58ca99843`

```dockerfile
```

-	Layers:
	-	`sha256:010ac6c4a92f0a1b0210b7a80f91903d77525cece3840618252e3ed4c20e7985`  
		Last Modified: Fri, 17 Jan 2025 18:52:23 GMT  
		Size: 2.2 MB (2157893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a58bc5ee847bd99d01c14b8acd94d0b00780ecb7dced4bcab3c893f9a9e41c1`  
		Last Modified: Fri, 17 Jan 2025 18:52:22 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; 386

```console
$ docker pull composer@sha256:0376015388eb0c4e0e2a048353fb4a996d0e14a72b20a8a32b25abee8fa607fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54517309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ec4296bf1615a63f52a61f4cb8b8f8a34dbb9c8052dd9201393b6deecb7083`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfcabeec76e82e774d4a80656efdfc79ff8f40c450fbdd73dd3f9950ceb81d`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 3.4 MB (3373778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d250fddeb1debe229bb3f39f26177002aa97298c86687390ec93c5560a19f`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211adc87542ef1dd59501ad1b38031188049730b7b2712675469c23330a736`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87e5b0c31577e6cc14f074a34f293cf80c8700b2325895b1e60d511618578a6`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 13.6 MB (13591509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c7e04c7c5fc0f3187954b25a758a9d80b000947e870a1b160927dca9d40ea`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7c2a142bbfe468340f79a720467957f43a6f702651de57e539baba60bed9ab`  
		Last Modified: Fri, 17 Jan 2025 17:35:40 GMT  
		Size: 21.4 MB (21405219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6e9c16628bd2c485e0f707d1d17f8bd3395400810810ed37be2ba3c51eb6b1`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac723b08e7819bbfef249f592e8c7e989e37423caf36f3a55b17f82f9725fd7d`  
		Last Modified: Fri, 17 Jan 2025 17:35:37 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039f95d894bab1fa4ff121b492e15e7ee19f40e390b76e7839f85f6411bf38d8`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 11.4 MB (11422368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82585710f86585eabf5cb54a38c2dd44a7876261824901a409a9b0dc169798af`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4487baf956c2f025d48f2673806357c7fc1f5620a9265de115efffe49bc764e`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 1.2 MB (1236422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7bd854aabd0a2be0fff545908290c973dddcd4a4a064ab3ea153c014e30d7d`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223b48ae68b36774e967c010f79283db40f684a386ec7f5fb0e403aae38af24f`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:1a5276be0fc84fee553c0e65252ced541c4f810d88bc429436495a188554c567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.1 KB (458053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d7f97ebdb452a45afc57bfd5812adb0cf04f79c1ae7c2e03dd335e168587b2`

```dockerfile
```

-	Layers:
	-	`sha256:dbfaa1eb952ce4ad49fbacf43c8a18369822fb722b28f00b107f126878ec5a5e`  
		Last Modified: Fri, 17 Jan 2025 18:29:05 GMT  
		Size: 427.4 KB (427417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49fb341e1f0d26d169dc3c74c686ca6eb9c597b41661074bbe601e243dafd32b`  
		Last Modified: Fri, 17 Jan 2025 18:29:05 GMT  
		Size: 30.6 KB (30636 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; ppc64le

```console
$ docker pull composer@sha256:4b1513c51938e1e558a81d04eb6a26b69f7ee308ffedb7b97be2e53592a9aef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76713347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495bbf873098d8ac889d964bfa7662517a4975ad063d0b1914484b54b3d748ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b4383e34608c265e3fcbc92f32f5b8e945fc93e6ecdaee910fa87b61b91eb7`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 13.6 MB (13591557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e98b79c382ca554316b5d1b58a69661a67bd73dd451dd9abba75515417cbf`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127935b1403b47049e26eb8a451d0fe15bf3dad3927f479ecfaea54a6026fc5`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 21.8 MB (21795018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8ff0ba33694c0f44258826a3874aaba09beb6072bf0353bb8c47363c0352c`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a75fc421d956d999c53c8003d5e0e6d664732d35993de12ae6e2232c4b9f1da`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63365f65e1acf2e91a180d560297bef7c52ed1b068a3ac5e41cfcab736a1edad`  
		Last Modified: Fri, 17 Jan 2025 18:37:26 GMT  
		Size: 32.9 MB (32944628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7bf30775a0bd0ff25c3418afea9aaee7ede8783e218f3d3368cc426b619c01`  
		Last Modified: Fri, 17 Jan 2025 18:37:24 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c8e9b27017ce878482f1789c56f8497d435632e60a3bcb029134995e689eda`  
		Last Modified: Fri, 17 Jan 2025 18:38:21 GMT  
		Size: 1.3 MB (1307492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8bd6d927ede2ec84d0c0b3185d20fdc1526bf4c1957b5d69fdb45aa13281f2`  
		Last Modified: Fri, 17 Jan 2025 18:38:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6515f866130a388a57f354d33c5779cee51867f353aa30695d0a91d5cea029d`  
		Last Modified: Fri, 17 Jan 2025 18:38:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:0c67da5cacd80b8a253de1e63275c282be6c0221287f164cbb129dee534dea1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f6ccbf6b17ce696826a17ec2ab3f204754f0ba82d8343caba49f3a4dbf4075`

```dockerfile
```

-	Layers:
	-	`sha256:2f36f16717dbb53739dfe52c7ad1c0ad7cb4558cbfe12369170e7809d1280d1f`  
		Last Modified: Fri, 17 Jan 2025 18:38:20 GMT  
		Size: 2.2 MB (2156316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e492c096763a9fcc7e4791995cee96f7444d911462be7b6a96b4dd0cc39aa6ba`  
		Last Modified: Fri, 17 Jan 2025 18:38:20 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; riscv64

```console
$ docker pull composer@sha256:ee152e540432328e13108ec84afc015bf23dea64c7c04999d749e4d8c9b2b32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73035699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be6a8fb02be39fef30f354d98422c35bc79aa3b42ef9c794e876be6af62532c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 08 Jan 2025 23:26:57 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 19:26:15 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 19:26:16 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 19:26:14 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680962a19a25c3960d22cb3a10ea5a2197502ebe67fe87e93e01d571dc161d6`  
		Last Modified: Sat, 18 Jan 2025 02:16:46 GMT  
		Size: 31.0 MB (31000955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b510b40be7ea214b9ab25bd8ec441bf4b4f4d23b112019f368e2f69c97d3d`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ec0aab3bdf7a4e1fe4171af27392c3d118447e7070479ab154572734d9656b`  
		Last Modified: Sat, 18 Jan 2025 02:21:56 GMT  
		Size: 1.3 MB (1290080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b0f62f350e1e191b43d7e26196f7292ec4e3fd421fe6c59272281b34608c9b`  
		Last Modified: Sat, 18 Jan 2025 02:21:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4f3ee911bd3c8e3bda361ed3f502b76a9137e1309ecccce81a8336ea76e4a2`  
		Last Modified: Sat, 18 Jan 2025 02:21:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:f3303d58c9797d5f86efe787f3572a89512aa4848e0a9484dc2cd4e76f518270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41278b70823d827c32e4f578569af2aaede160d87a2c47cfef7b2bd2ad43b0e7`

```dockerfile
```

-	Layers:
	-	`sha256:58f466d74e8cb7002f72a2b9fd5af89bf2e6d04dd606e459cc2d41f6b8a712c0`  
		Last Modified: Sat, 18 Jan 2025 02:21:55 GMT  
		Size: 2.2 MB (2155258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:445e66973e632c38a4c006d379e93b9e1114018a8f1d9226188b471fd3fb87c0`  
		Last Modified: Sat, 18 Jan 2025 02:21:55 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10` - linux; s390x

```console
$ docker pull composer@sha256:7e20ac6fe79289732b6d393e54889ee4a0e251cd79f6d4367569469cc393694c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74994761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ef62539726071388045d696014e2e66c53f88c217ed47cb5349456040f84cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd3b180b852bfd68493c7e27214dde2fc3d4e836aabe9023ed45c8fb27e3e51`  
		Last Modified: Fri, 17 Jan 2025 19:06:19 GMT  
		Size: 31.7 MB (31677476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bc62e74286362c0d45e020cba1c516cb4c2cc297b67f803d103e9b29f070d`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd10dc6b34f98694f6877d29a7b58697c521ca6dc72ccba1904e9170fbe552`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 1.3 MB (1298930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a530e29e1832e69abdb289f76419ea77a583ded99364e9f2d0ab65f9e1a60bb1`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f65dc591f0b96d19aa98ad0c539cae4cdb1d37b80384762d209c867ee257ab`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10` - unknown; unknown

```console
$ docker pull composer@sha256:3b5664a2a00286d481e2893f726d1da9dbf225086d0eeb090b1cae448ff9d2a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c1398be2d4d8444f400d2f004eb60389bbd5f2971545adbfffb4c21bc9ffe3`

```dockerfile
```

-	Layers:
	-	`sha256:9a77f7d6776dedb5112d71772250eda1bfccf0fb2406a812267916ccb4ff48b6`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 2.2 MB (2155044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c9859306194382d74ac07a37236c26b27e93bebd140cdcb7032e817c5a1b3f`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 30.7 KB (30666 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:1.10.27`

```console
$ docker pull composer@sha256:09bc7fee35a9138e8fd8c270a778dcee00a8593b4c59001ea54186ec153b3725
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
$ docker pull composer@sha256:768215cde03ed7f4d09c35404b056c78653cb3eb5993ffe627c960b82e840fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74635922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2877408cd5e3b4152f4f6d1a0611bc007583a47ba7e476a1b009d61576769601`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79c0dc8060e2f059662ca297aa3feae6b3652e5ce0ab171e72b087bec9eb496`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 3.3 MB (3333627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c72c57155ad8b911527445f9878aaf9a4be98da1365dc25227d456bbc357591`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235f6cd368cc120d2abc4c6cb424fde285daf59e2c3f78c72eaa5d14143b8ca`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abdd5367cc40b78b668ff086497ce457af0e483ed80d43df0d8939be0777869`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 13.6 MB (13591519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774922f802bd2f5aeddab05459b4faa03b0664c923d4d04e30d5a5d016662437`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245938a8f085f24c8cf3660fa4370cfad0223a42c79a99e915bbe89ff2910aeb`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.9 MB (20889503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893a8e1213f3e7623f34d6436a30f720ae4cb772c2bdb4e1308dd1333693fee2`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd82ceb5444495c6039a1591b24bb6cde1dd739805a599f07047bbac0e1e9ef`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4e043d9e29c69239ba1132e2798df426a1fdfd2810df74d28f1f634fc52781`  
		Last Modified: Fri, 17 Jan 2025 18:29:26 GMT  
		Size: 31.9 MB (31897535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e3ac59736f5bfc588754b0cdb23c4908b225c6f7513e4b36f979806350dc13`  
		Last Modified: Fri, 17 Jan 2025 18:29:25 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91eef26589c2e0534fdaf247c9dedb7ccefe830751f9a9592ddf5f3b6a9b12e7`  
		Last Modified: Fri, 17 Jan 2025 18:29:25 GMT  
		Size: 1.3 MB (1257146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6798583195f68cec585365a4e55a39f4cc42c0d68844ce31f316ee6345adec`  
		Last Modified: Fri, 17 Jan 2025 18:29:25 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039d761834a9bc230994f8758a9ce0d6fce13e09040f053b05f1c6c0cbbb311b`  
		Last Modified: Fri, 17 Jan 2025 18:29:26 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:970c4faaee6feee3e5579e424615c069cd40c05afd7afc41423a33b6f34b58fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189b197a6c0e473d9324b110fbb641b4e9d6ac53df3337561c6ea9b1f3fc2906`

```dockerfile
```

-	Layers:
	-	`sha256:b0d4fe55feef5e24aabd607f549b5f70314ad8f83fae06efb004d3a44c8c5bba`  
		Last Modified: Fri, 17 Jan 2025 18:29:24 GMT  
		Size: 2.2 MB (2157759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee887a60bd6d5b4ade8cda77941cfd7777c0865a8335d4c00813f5dc793309e6`  
		Last Modified: Fri, 17 Jan 2025 18:29:24 GMT  
		Size: 30.7 KB (30667 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v6

```console
$ docker pull composer@sha256:e7d25df986db56a16c42bf9d1146d18cf46c0831ef1d7f1b4f0b90be0f3b3e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70684825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f083abe1f39fc1ed772ef6dd504c615898b51b4eb02dbf8dcccc1bb082e7e169`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 08 Jan 2025 18:49:59 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c35832122daf4e6cfd46f0be114a1c6d91b28caceb8f9b86ccb0253e0678632`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 13.6 MB (13591522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abac4d6df3f8471bdecc32831cfc97f2c065ebc58af29566d6e67161775d19e0`  
		Last Modified: Fri, 17 Jan 2025 17:36:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2e9c673c0e2f9934f576e177ae7ca6da19e281e8237523ec2deaddd3b94bb9`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.0 MB (19026889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fed1b7e2d514321545f15b0b6088794d7792c9f6d76c05ea93a61a505107b0`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f1b1f6a6b1a43d58472514b514bd3dc9e1bea6c950d8157396f5af086179d`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1602695904d94b7c906ed6ec74d99f418f62b6c4568fbbad2ab38440a9d1523f`  
		Last Modified: Fri, 17 Jan 2025 18:28:47 GMT  
		Size: 30.6 MB (30642262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e61ca26b0794a9473633a58d896e1b0db4d23c3019d4bf7c5501224de9ae50`  
		Last Modified: Fri, 17 Jan 2025 18:28:46 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5059976bdb25c5aaa39cfcac2c9eb8816257c984039a88f8d7cb1b415d2e5126`  
		Last Modified: Fri, 17 Jan 2025 18:29:22 GMT  
		Size: 735.1 KB (735085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ceec54fcb2477b469f9dca645219b218dc16b9abef7401105c9053f18e97c13`  
		Last Modified: Thu, 12 Dec 2024 01:10:16 GMT  
		Size: 411.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250d615bccc5eb6d9bdac6d6c423eeeeb190758abb44c2f0824e8bdf282080e7`  
		Last Modified: Fri, 17 Jan 2025 18:29:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:dd71c89033641a4688e1e9decb2306a4345b7402cc85996dddbed7af6f4d085f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ed269b877f1428a0d110692457a0acca5a18c895d6c1fe8479f3f120f0fc35`

```dockerfile
```

-	Layers:
	-	`sha256:c7cc6ca60272946a2a64e5825627c05fad96a03fa341a71d2839f3f85ce42bf4`  
		Last Modified: Fri, 17 Jan 2025 18:29:21 GMT  
		Size: 30.5 KB (30543 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm variant v7

```console
$ docker pull composer@sha256:8b3b0f6f411a9e87e16f33e755595580999498ccf68531b8cfdaf0dfeb4ced77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68714221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e87efbb9e62c9c58dfe8709dce42c8e011bf3338bd86b05d486befd4c9e554f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd50b568401204c1289c16767a7acc4d1073b759b096a454b243856d0c372e8`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 30.2 MB (30150787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653d3258e5cf9a2c21ab7508e95c806af126ebe35e115ff9cb054bdfc47dad1`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0fde7ef9d30daad0a1ebf2abdd94642a82f6cbc2352eac9aea823092a8a1bd`  
		Last Modified: Fri, 17 Jan 2025 19:01:00 GMT  
		Size: 726.0 KB (725970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b380156e47baddf486b12e44bc2186ae9e8805cd77ce915c9543262f8b7453fc`  
		Last Modified: Fri, 17 Jan 2025 19:01:00 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4df7a48018e36dde3d10f5f5d4961f84d2a063350abc23a0e3c1fe36e393ae`  
		Last Modified: Fri, 17 Jan 2025 19:01:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:7095211436838685445b19febee7863a872e77ac77333fcf0c9d89dad2890bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00c2e8d5309e6ef34a1aa41831f1481a09ce1a8eadec6d2a942918c016835c43`

```dockerfile
```

-	Layers:
	-	`sha256:b40158dd770afa7b112486e8d5a30050cb36abe66727e2399a74e11b25262be7`  
		Last Modified: Fri, 17 Jan 2025 19:00:59 GMT  
		Size: 2.2 MB (2158069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da3fc77de0b178aa79a8c9d98ebf50c0ce7065e6ac4dac8dfb3690e10ecbe3d1`  
		Last Modified: Fri, 17 Jan 2025 19:00:58 GMT  
		Size: 30.8 KB (30757 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:77812cb369d8a42db041efba9da530a542b3468a087e68919111612427ff67f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74113901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a124fca3ddc8f759c944c1685729a500ede9dfadde178742e010986b067492`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ded2f1970092c503a682b521201d635e8da0ad60d85a3975060091b0f092d`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 13.6 MB (13591559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12833fff26b4ea2cc381b02e1323f22bd1ac14a4e52a6c8417bbaa55152bd4e`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c693c7cf8097154c6af6b666782076f82f2824477b99c90ff0ca4adb3dbf3cb`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 20.4 MB (20438477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a526ad694be5912a4e8430a6cc668e490cde1f20e6e2b3b004536d3c0a679c`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092dc5a53c2e0204ffcfdfa51a695d5cd5bce5efd0d5d3a58243608a7c6b688`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb5a4ba752055d65a4614132f2cf5a9e53ce62b1e4d38c29a132319b331092`  
		Last Modified: Fri, 17 Jan 2025 18:51:48 GMT  
		Size: 32.0 MB (32004216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99ebc1999608761928e8f7869e0332f0652885f6d3ec81a815c3af8606c258f`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb6be86afb4f93600a29aff19b90dce61e601afb134a82bdff8673e51abeb2f`  
		Last Modified: Fri, 17 Jan 2025 18:52:23 GMT  
		Size: 734.9 KB (734915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45981721fe0761a0305dd59f9567caaeef46fd464382ae34114b490fc61ebda`  
		Last Modified: Fri, 17 Jan 2025 18:52:24 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0ba0a229a3e08dcbca879697901952658e1635ba1f5fe872a5d5923c75b758`  
		Last Modified: Fri, 17 Jan 2025 18:52:24 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:cb7b3fc12e8b6a5644d753ada86e70c00c3e366ad04086de20b2d0ce449f8113
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6672654cb1f7512b60382c69c99a8d3d9612d42e790446e3ccdff6d58ca99843`

```dockerfile
```

-	Layers:
	-	`sha256:010ac6c4a92f0a1b0210b7a80f91903d77525cece3840618252e3ed4c20e7985`  
		Last Modified: Fri, 17 Jan 2025 18:52:23 GMT  
		Size: 2.2 MB (2157893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a58bc5ee847bd99d01c14b8acd94d0b00780ecb7dced4bcab3c893f9a9e41c1`  
		Last Modified: Fri, 17 Jan 2025 18:52:22 GMT  
		Size: 30.8 KB (30786 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; 386

```console
$ docker pull composer@sha256:0376015388eb0c4e0e2a048353fb4a996d0e14a72b20a8a32b25abee8fa607fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54517309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ec4296bf1615a63f52a61f4cb8b8f8a34dbb9c8052dd9201393b6deecb7083`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfcabeec76e82e774d4a80656efdfc79ff8f40c450fbdd73dd3f9950ceb81d`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 3.4 MB (3373778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d250fddeb1debe229bb3f39f26177002aa97298c86687390ec93c5560a19f`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211adc87542ef1dd59501ad1b38031188049730b7b2712675469c23330a736`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87e5b0c31577e6cc14f074a34f293cf80c8700b2325895b1e60d511618578a6`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 13.6 MB (13591509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c7e04c7c5fc0f3187954b25a758a9d80b000947e870a1b160927dca9d40ea`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7c2a142bbfe468340f79a720467957f43a6f702651de57e539baba60bed9ab`  
		Last Modified: Fri, 17 Jan 2025 17:35:40 GMT  
		Size: 21.4 MB (21405219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6e9c16628bd2c485e0f707d1d17f8bd3395400810810ed37be2ba3c51eb6b1`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac723b08e7819bbfef249f592e8c7e989e37423caf36f3a55b17f82f9725fd7d`  
		Last Modified: Fri, 17 Jan 2025 17:35:37 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039f95d894bab1fa4ff121b492e15e7ee19f40e390b76e7839f85f6411bf38d8`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 11.4 MB (11422368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82585710f86585eabf5cb54a38c2dd44a7876261824901a409a9b0dc169798af`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4487baf956c2f025d48f2673806357c7fc1f5620a9265de115efffe49bc764e`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 1.2 MB (1236422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7bd854aabd0a2be0fff545908290c973dddcd4a4a064ab3ea153c014e30d7d`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223b48ae68b36774e967c010f79283db40f684a386ec7f5fb0e403aae38af24f`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:1a5276be0fc84fee553c0e65252ced541c4f810d88bc429436495a188554c567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **458.1 KB (458053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d7f97ebdb452a45afc57bfd5812adb0cf04f79c1ae7c2e03dd335e168587b2`

```dockerfile
```

-	Layers:
	-	`sha256:dbfaa1eb952ce4ad49fbacf43c8a18369822fb722b28f00b107f126878ec5a5e`  
		Last Modified: Fri, 17 Jan 2025 18:29:05 GMT  
		Size: 427.4 KB (427417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49fb341e1f0d26d169dc3c74c686ca6eb9c597b41661074bbe601e243dafd32b`  
		Last Modified: Fri, 17 Jan 2025 18:29:05 GMT  
		Size: 30.6 KB (30636 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; ppc64le

```console
$ docker pull composer@sha256:4b1513c51938e1e558a81d04eb6a26b69f7ee308ffedb7b97be2e53592a9aef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.7 MB (76713347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495bbf873098d8ac889d964bfa7662517a4975ad063d0b1914484b54b3d748ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b4383e34608c265e3fcbc92f32f5b8e945fc93e6ecdaee910fa87b61b91eb7`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 13.6 MB (13591557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e98b79c382ca554316b5d1b58a69661a67bd73dd451dd9abba75515417cbf`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127935b1403b47049e26eb8a451d0fe15bf3dad3927f479ecfaea54a6026fc5`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 21.8 MB (21795018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8ff0ba33694c0f44258826a3874aaba09beb6072bf0353bb8c47363c0352c`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a75fc421d956d999c53c8003d5e0e6d664732d35993de12ae6e2232c4b9f1da`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63365f65e1acf2e91a180d560297bef7c52ed1b068a3ac5e41cfcab736a1edad`  
		Last Modified: Fri, 17 Jan 2025 18:37:26 GMT  
		Size: 32.9 MB (32944628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7bf30775a0bd0ff25c3418afea9aaee7ede8783e218f3d3368cc426b619c01`  
		Last Modified: Fri, 17 Jan 2025 18:37:24 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c8e9b27017ce878482f1789c56f8497d435632e60a3bcb029134995e689eda`  
		Last Modified: Fri, 17 Jan 2025 18:38:21 GMT  
		Size: 1.3 MB (1307492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8bd6d927ede2ec84d0c0b3185d20fdc1526bf4c1957b5d69fdb45aa13281f2`  
		Last Modified: Fri, 17 Jan 2025 18:38:21 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6515f866130a388a57f354d33c5779cee51867f353aa30695d0a91d5cea029d`  
		Last Modified: Fri, 17 Jan 2025 18:38:21 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:0c67da5cacd80b8a253de1e63275c282be6c0221287f164cbb129dee534dea1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30f6ccbf6b17ce696826a17ec2ab3f204754f0ba82d8343caba49f3a4dbf4075`

```dockerfile
```

-	Layers:
	-	`sha256:2f36f16717dbb53739dfe52c7ad1c0ad7cb4558cbfe12369170e7809d1280d1f`  
		Last Modified: Fri, 17 Jan 2025 18:38:20 GMT  
		Size: 2.2 MB (2156316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e492c096763a9fcc7e4791995cee96f7444d911462be7b6a96b4dd0cc39aa6ba`  
		Last Modified: Fri, 17 Jan 2025 18:38:20 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; riscv64

```console
$ docker pull composer@sha256:ee152e540432328e13108ec84afc015bf23dea64c7c04999d749e4d8c9b2b32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73035699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be6a8fb02be39fef30f354d98422c35bc79aa3b42ef9c794e876be6af62532c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 08 Jan 2025 23:26:57 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 19:26:15 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 19:26:16 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 19:26:14 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680962a19a25c3960d22cb3a10ea5a2197502ebe67fe87e93e01d571dc161d6`  
		Last Modified: Sat, 18 Jan 2025 02:16:46 GMT  
		Size: 31.0 MB (31000955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b510b40be7ea214b9ab25bd8ec441bf4b4f4d23b112019f368e2f69c97d3d`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ec0aab3bdf7a4e1fe4171af27392c3d118447e7070479ab154572734d9656b`  
		Last Modified: Sat, 18 Jan 2025 02:21:56 GMT  
		Size: 1.3 MB (1290080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b0f62f350e1e191b43d7e26196f7292ec4e3fd421fe6c59272281b34608c9b`  
		Last Modified: Sat, 18 Jan 2025 02:21:56 GMT  
		Size: 410.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb4f3ee911bd3c8e3bda361ed3f502b76a9137e1309ecccce81a8336ea76e4a2`  
		Last Modified: Sat, 18 Jan 2025 02:21:56 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:f3303d58c9797d5f86efe787f3572a89512aa4848e0a9484dc2cd4e76f518270
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41278b70823d827c32e4f578569af2aaede160d87a2c47cfef7b2bd2ad43b0e7`

```dockerfile
```

-	Layers:
	-	`sha256:58f466d74e8cb7002f72a2b9fd5af89bf2e6d04dd606e459cc2d41f6b8a712c0`  
		Last Modified: Sat, 18 Jan 2025 02:21:55 GMT  
		Size: 2.2 MB (2155258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:445e66973e632c38a4c006d379e93b9e1114018a8f1d9226188b471fd3fb87c0`  
		Last Modified: Sat, 18 Jan 2025 02:21:55 GMT  
		Size: 30.7 KB (30707 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:1.10.27` - linux; s390x

```console
$ docker pull composer@sha256:7e20ac6fe79289732b6d393e54889ee4a0e251cd79f6d4367569469cc393694c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.0 MB (74994761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ef62539726071388045d696014e2e66c53f88c217ed47cb5349456040f84cf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 14 Nov 2024 10:47:28 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["/bin/sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 14 Nov 2024 10:47:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 14 Nov 2024 10:47:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_VERSION=8.4.3
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 14 Nov 2024 10:47:28 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["php" "-a"]
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 14 Nov 2024 10:47:28 GMT
ENV COMPOSER_VERSION=1.10.27
# Thu, 14 Nov 2024 10:47:28 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 14 Nov 2024 10:47:28 GMT
WORKDIR /app
# Thu, 14 Nov 2024 10:47:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 Nov 2024 10:47:28 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd3b180b852bfd68493c7e27214dde2fc3d4e836aabe9023ed45c8fb27e3e51`  
		Last Modified: Fri, 17 Jan 2025 19:06:19 GMT  
		Size: 31.7 MB (31677476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bc62e74286362c0d45e020cba1c516cb4c2cc297b67f803d103e9b29f070d`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83bd10dc6b34f98694f6877d29a7b58697c521ca6dc72ccba1904e9170fbe552`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 1.3 MB (1298930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a530e29e1832e69abdb289f76419ea77a583ded99364e9f2d0ab65f9e1a60bb1`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 409.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f65dc591f0b96d19aa98ad0c539cae4cdb1d37b80384762d209c867ee257ab`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:1.10.27` - unknown; unknown

```console
$ docker pull composer@sha256:3b5664a2a00286d481e2893f726d1da9dbf225086d0eeb090b1cae448ff9d2a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2185710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c1398be2d4d8444f400d2f004eb60389bbd5f2971545adbfffb4c21bc9ffe3`

```dockerfile
```

-	Layers:
	-	`sha256:9a77f7d6776dedb5112d71772250eda1bfccf0fb2406a812267916ccb4ff48b6`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 2.2 MB (2155044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7c9859306194382d74ac07a37236c26b27e93bebd140cdcb7032e817c5a1b3f`  
		Last Modified: Fri, 17 Jan 2025 19:07:22 GMT  
		Size: 30.7 KB (30666 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2`

```console
$ docker pull composer@sha256:72b9e4b2038558f7256e7f925495aa791c0ee764e1d351f3963b379b18b4c2f5
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
$ docker pull composer@sha256:b0d1f86b249e8ad13385460acf91fe8981025254b1c99182c77ec2d5a2acb3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74867031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3068ed6d9d3483b75a985d9810de4e9f01aa7e5b0ed9d6a07d961341ff3b9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79c0dc8060e2f059662ca297aa3feae6b3652e5ce0ab171e72b087bec9eb496`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 3.3 MB (3333627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c72c57155ad8b911527445f9878aaf9a4be98da1365dc25227d456bbc357591`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235f6cd368cc120d2abc4c6cb424fde285daf59e2c3f78c72eaa5d14143b8ca`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abdd5367cc40b78b668ff086497ce457af0e483ed80d43df0d8939be0777869`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 13.6 MB (13591519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774922f802bd2f5aeddab05459b4faa03b0664c923d4d04e30d5a5d016662437`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245938a8f085f24c8cf3660fa4370cfad0223a42c79a99e915bbe89ff2910aeb`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.9 MB (20889503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893a8e1213f3e7623f34d6436a30f720ae4cb772c2bdb4e1308dd1333693fee2`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd82ceb5444495c6039a1591b24bb6cde1dd739805a599f07047bbac0e1e9ef`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92275c43a85b8aa4d5d29a473e99b45a0a58bd6fc3d19747ded8ae5bd5b09bfd`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 31.9 MB (31897758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b171394f04ec4be3ca122091116ef51e5b93e03f1441874fc269f3ea2cfbd90f`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b5efc53199ab0f27d01547156e5f9fc738c814b925906eee944a7e938e0ae2`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 1.5 MB (1488021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a2d00126212ed657639a3471bad1fe81be0e0e4d3f1c091efb1817bc80f3a0`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4f79a1f4e2be242c1bcf4ca94b21dbc50987dc8cfdce0671e018164c46e28`  
		Last Modified: Fri, 17 Jan 2025 18:29:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:e8c19a35ef2d84ce075be7d29ea8db42e0e32a403760c5c12a362691883578d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0f45264204260dad5a9d5efa4e9f92f8ad9d2a8978278eca6f925b1a99d205`

```dockerfile
```

-	Layers:
	-	`sha256:c3172cea930f51e6b3274339e20d769dd681448257536f8a40d8a170416908c4`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 2.2 MB (2159253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332c80b37d35b3ebe67ff7661823d9be1a091023a2057bba2db5985b99b3414e`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v6

```console
$ docker pull composer@sha256:7f141df4c345189f1873674d2f2b661b4dfc4f04e9581d152e671bbecdb2546a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70915330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b4d9b874548bc37e8d5b38772691b758116321780c007f1afe8769c416816f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 08 Jan 2025 18:49:59 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c35832122daf4e6cfd46f0be114a1c6d91b28caceb8f9b86ccb0253e0678632`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 13.6 MB (13591522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abac4d6df3f8471bdecc32831cfc97f2c065ebc58af29566d6e67161775d19e0`  
		Last Modified: Fri, 17 Jan 2025 17:36:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2e9c673c0e2f9934f576e177ae7ca6da19e281e8237523ec2deaddd3b94bb9`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.0 MB (19026889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fed1b7e2d514321545f15b0b6088794d7792c9f6d76c05ea93a61a505107b0`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f1b1f6a6b1a43d58472514b514bd3dc9e1bea6c950d8157396f5af086179d`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1602695904d94b7c906ed6ec74d99f418f62b6c4568fbbad2ab38440a9d1523f`  
		Last Modified: Fri, 17 Jan 2025 18:28:47 GMT  
		Size: 30.6 MB (30642262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e61ca26b0794a9473633a58d896e1b0db4d23c3019d4bf7c5501224de9ae50`  
		Last Modified: Fri, 17 Jan 2025 18:28:46 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4610cac406d8d57d794ab5c079a884d4b91acce4d551e6587b6eb74c784dde6c`  
		Last Modified: Fri, 17 Jan 2025 18:29:57 GMT  
		Size: 965.6 KB (965582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3826a6b574a6d595615f31b1ef9fae34a30dd1e418f79cee3bc7ab6a295e46ee`  
		Last Modified: Thu, 12 Dec 2024 19:28:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3c203e31a9b3ce363affb2b7bdad1da625d875ecac95065bedd70818887640`  
		Last Modified: Fri, 17 Jan 2025 18:29:57 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:e8c1b89db9235c3f2b590483301d18f71261a7ad139f41c2efd67067c0583605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cab451954bba3cfcefac968eb15ec096230128589be0c692014679eb36f0208`

```dockerfile
```

-	Layers:
	-	`sha256:a028c4ddb16f18673428b8b3b1051a9c5371bec27500fddcf29bc791172e21dc`  
		Last Modified: Fri, 17 Jan 2025 18:29:56 GMT  
		Size: 30.8 KB (30845 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm variant v7

```console
$ docker pull composer@sha256:f2775b2881f79afa2f5eae48c1e42efe9dd7a770edb4f9c50bd481f62eea5f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68945004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fb0a57178754951e43d36e9b3339fae42640a49ec81ebff948bd3dfdd194f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd50b568401204c1289c16767a7acc4d1073b759b096a454b243856d0c372e8`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 30.2 MB (30150787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653d3258e5cf9a2c21ab7508e95c806af126ebe35e115ff9cb054bdfc47dad1`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bb1d25f3841491b6bac119ae64d1347bc0a1b1254eb7b6124b2ff37bf7718b`  
		Last Modified: Fri, 17 Jan 2025 19:01:41 GMT  
		Size: 956.7 KB (956741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7daae6fd21bb945c0c6cda66b271b53494a15746ad03187c8f4c3091d9b4a7`  
		Last Modified: Fri, 17 Jan 2025 19:01:41 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4859256f8687c04b3166ccedb99b87aad36db1681edf9201e8955068d1a585`  
		Last Modified: Fri, 17 Jan 2025 19:01:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:85a9914de79bea623f353a8d8751970238dbbd1fe77a116d027e383c1911c258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d5389def231fdbc98394e6e3b762ff68cd55e7c474d8c444bb9c8a89c1e70f`

```dockerfile
```

-	Layers:
	-	`sha256:8f9b5db3de8336316eec834c847d89ff5f37ddc768dba303187202b6563384d0`  
		Last Modified: Fri, 17 Jan 2025 19:01:40 GMT  
		Size: 2.2 MB (2159571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a154e02ab0e548ed6a1684113b9857cf0776d1fef5dba6d6a8c6879333876dd9`  
		Last Modified: Fri, 17 Jan 2025 19:01:40 GMT  
		Size: 31.1 KB (31059 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:7c063c2c8a4d2322841db1784b242972de6103929049df728f2a06e1c24b11cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74344757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb86978297a92933cbbb7709acbd5835ea6273bf5366ecd5785ba2f390b2fe5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ded2f1970092c503a682b521201d635e8da0ad60d85a3975060091b0f092d`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 13.6 MB (13591559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12833fff26b4ea2cc381b02e1323f22bd1ac14a4e52a6c8417bbaa55152bd4e`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c693c7cf8097154c6af6b666782076f82f2824477b99c90ff0ca4adb3dbf3cb`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 20.4 MB (20438477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a526ad694be5912a4e8430a6cc668e490cde1f20e6e2b3b004536d3c0a679c`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092dc5a53c2e0204ffcfdfa51a695d5cd5bce5efd0d5d3a58243608a7c6b688`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb5a4ba752055d65a4614132f2cf5a9e53ce62b1e4d38c29a132319b331092`  
		Last Modified: Fri, 17 Jan 2025 18:51:48 GMT  
		Size: 32.0 MB (32004216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99ebc1999608761928e8f7869e0332f0652885f6d3ec81a815c3af8606c258f`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c9376466fb2ff8bc5528153d7f861f04995f0daa87b044e5525d9d8a40909f`  
		Last Modified: Fri, 17 Jan 2025 18:52:59 GMT  
		Size: 965.8 KB (965760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfa5bd629098bac4f5b8754994d5ae0b9470c39f074ad4d2b2472e0d4b48cd`  
		Last Modified: Fri, 17 Jan 2025 18:52:59 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4f60a0974f888f32ced79e6c2a4f32178d62863c80020590947e63fe98f206`  
		Last Modified: Fri, 17 Jan 2025 18:53:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:6f70519f4cd62d4aab830560dc8ae18c6848a2cd35e9d8ce385de0ad011a448d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256d25ea4546755db3302dff210d29cd5d78c4c16b49a3276b3fab0760e535f6`

```dockerfile
```

-	Layers:
	-	`sha256:cba006b914cec0703d0a33e228ae94a218f3a7ba8ef00a0ab6ef45d144207778`  
		Last Modified: Fri, 17 Jan 2025 18:52:58 GMT  
		Size: 2.2 MB (2159399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:985a870bb36e77fa6e85295356876be6db751e4a1375de124648887b21f26e1e`  
		Last Modified: Fri, 17 Jan 2025 18:52:58 GMT  
		Size: 31.1 KB (31091 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; 386

```console
$ docker pull composer@sha256:2850528275031a129a34ade0fa178e786068ef95773938bf2f22d3c893f91025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54747999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91daf8ffcc4aa2f14ee2a088fc525bd9a0f86849cbc0952c0f7b755ff91d99bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfcabeec76e82e774d4a80656efdfc79ff8f40c450fbdd73dd3f9950ceb81d`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 3.4 MB (3373778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d250fddeb1debe229bb3f39f26177002aa97298c86687390ec93c5560a19f`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211adc87542ef1dd59501ad1b38031188049730b7b2712675469c23330a736`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87e5b0c31577e6cc14f074a34f293cf80c8700b2325895b1e60d511618578a6`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 13.6 MB (13591509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c7e04c7c5fc0f3187954b25a758a9d80b000947e870a1b160927dca9d40ea`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7c2a142bbfe468340f79a720467957f43a6f702651de57e539baba60bed9ab`  
		Last Modified: Fri, 17 Jan 2025 17:35:40 GMT  
		Size: 21.4 MB (21405219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6e9c16628bd2c485e0f707d1d17f8bd3395400810810ed37be2ba3c51eb6b1`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac723b08e7819bbfef249f592e8c7e989e37423caf36f3a55b17f82f9725fd7d`  
		Last Modified: Fri, 17 Jan 2025 17:35:37 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0cb52933b74a8bd009eefe51cc608d16321e03af899e8cfdeb15ac3dcec360`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 11.4 MB (11422348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f69b64652dc4f61503554fe51944b51aa2b1a0de45969c509cebb5e2aee178`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b3f5bbe8654ef041dd9c306653961e4447c7ab54ac0c3086149958a1c9f3c4`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 1.5 MB (1467121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0b30d38f38f43d13e3639dd4817c354e8c4dac615f32c2088a167cdae8a557`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ddf37642fd1586646c6a31e21ba13ebe32541843f684a1aa9fae408b4059`  
		Last Modified: Fri, 17 Jan 2025 18:29:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:4a40599e138b4481df374b85d4d1858fd3902b9377986b77ff742e1e5bf108f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.8 KB (459831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93828c340e549a91e0b9a91b9a548ef84019770f9e6ee56b8a2a02709049b7bf`

```dockerfile
```

-	Layers:
	-	`sha256:2fd802b66bb8f9df09c89907a2ad1e36004e951a9e5991d7d569c61fd8e659df`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 428.9 KB (428906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fd2d904e4e5db8739d8fbda2129f1682bfa98eb21e864b62ce212939287c29`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; ppc64le

```console
$ docker pull composer@sha256:9da1507a1d17a5217c557bc8ef4727149d8c02f04b6a250ddcac2bc3f706bd37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76945265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1061d6a2c341df8b2294de4d117d80090b29b0c8a428bcf80d6e28f5836b96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b4383e34608c265e3fcbc92f32f5b8e945fc93e6ecdaee910fa87b61b91eb7`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 13.6 MB (13591557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e98b79c382ca554316b5d1b58a69661a67bd73dd451dd9abba75515417cbf`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127935b1403b47049e26eb8a451d0fe15bf3dad3927f479ecfaea54a6026fc5`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 21.8 MB (21795018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8ff0ba33694c0f44258826a3874aaba09beb6072bf0353bb8c47363c0352c`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a75fc421d956d999c53c8003d5e0e6d664732d35993de12ae6e2232c4b9f1da`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63365f65e1acf2e91a180d560297bef7c52ed1b068a3ac5e41cfcab736a1edad`  
		Last Modified: Fri, 17 Jan 2025 18:37:26 GMT  
		Size: 32.9 MB (32944628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7bf30775a0bd0ff25c3418afea9aaee7ede8783e218f3d3368cc426b619c01`  
		Last Modified: Fri, 17 Jan 2025 18:37:24 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd5e1913b7f8e9b6704b2e47884ccdd3b5d1e6424a19f53e91e02decc49ae4`  
		Last Modified: Fri, 17 Jan 2025 18:39:15 GMT  
		Size: 1.5 MB (1539398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5970900b0927fa0a730bdab2c0340e276db67dabf5f9cb0d023cbdebdfe3e51c`  
		Last Modified: Fri, 17 Jan 2025 18:39:15 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea8d3ad4cc5b3e229330f3b7ed1e831cada7cc8473ce4dcc54189ad951bf302`  
		Last Modified: Fri, 17 Jan 2025 18:39:15 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:a00c2a6b1b6e99304383ccacc1ac3c1e9a0f8be382e0a4b5dc1dff2d9c800710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f816122a748a29919a5bb7f8c0d167dd2373fea7b547daa11407fe753be12724`

```dockerfile
```

-	Layers:
	-	`sha256:da69f05cfb45c7c9c58c6aa383a17010c5777a996668a7cbb51d1623d85ddf36`  
		Last Modified: Fri, 17 Jan 2025 18:39:14 GMT  
		Size: 2.2 MB (2157816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c44cffb580860307d110d05c1f8e8fbc544878f905d9629695afdb0ca9eae8c`  
		Last Modified: Fri, 17 Jan 2025 18:39:14 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; riscv64

```console
$ docker pull composer@sha256:c50999d5b3bed5a8afc9d0ef596045b7f464fcdf7ed18339f4d856553b037c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73266527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae7a90617237ce4ca8ec221d9053df1dcb9d11ac3e2c6a1111e83843e3b948c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 08 Jan 2025 23:26:57 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 19:26:15 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 19:26:16 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 19:26:14 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680962a19a25c3960d22cb3a10ea5a2197502ebe67fe87e93e01d571dc161d6`  
		Last Modified: Sat, 18 Jan 2025 02:16:46 GMT  
		Size: 31.0 MB (31000955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b510b40be7ea214b9ab25bd8ec441bf4b4f4d23b112019f368e2f69c97d3d`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498d72bce4c2de0ffa86f86c00dd3bd54d3fbed403fee4717c9850665d0c8a9c`  
		Last Modified: Sat, 18 Jan 2025 02:27:09 GMT  
		Size: 1.5 MB (1520900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef3b442868969fb3a61dc6cd53d62dcc30465a773f95c5e798d6cabbfd2aa24`  
		Last Modified: Sat, 18 Jan 2025 02:27:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b6973f8270719e37a3cf40182c78acc208cd93c751c47493416ebd52763bd`  
		Last Modified: Sat, 18 Jan 2025 02:27:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:a18f431993c86eb84a67e0abfc762946793a5bfaf22a707b51e2c450f8275aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b22c3aee387fe25a95fe0325794c77927376f3f78daee3e4f7cb60fc694cb3`

```dockerfile
```

-	Layers:
	-	`sha256:d5a27470811617dd898ecffead1b6cc149e207bb50d23b53c447238db468a57f`  
		Last Modified: Sat, 18 Jan 2025 02:27:09 GMT  
		Size: 2.2 MB (2156758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db04b25fb3fc56c5f133c7a3d67bd3464eeb5933b7bfc5636da607b4aa61d3e`  
		Last Modified: Sat, 18 Jan 2025 02:27:08 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2` - linux; s390x

```console
$ docker pull composer@sha256:77238e3ac94e54493c9cbdd764e469d8b564f61817c114b6c06146b3f9b9d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75224497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b952a8b1ed6779ed4535d0380817a48673eafd2a5ff17a50efb536f6b3d6ed6a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd3b180b852bfd68493c7e27214dde2fc3d4e836aabe9023ed45c8fb27e3e51`  
		Last Modified: Fri, 17 Jan 2025 19:06:19 GMT  
		Size: 31.7 MB (31677476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bc62e74286362c0d45e020cba1c516cb4c2cc297b67f803d103e9b29f070d`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511d99151c23495e84a0a38c4a514fd5f223b9e6bce6c20fed79eb4728f9fc96`  
		Last Modified: Fri, 17 Jan 2025 19:08:50 GMT  
		Size: 1.5 MB (1528656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb6ae28e53beaac1131bed1e3a97281cad10e9d502e8e224ff7310e2cd49b66`  
		Last Modified: Fri, 17 Jan 2025 19:08:50 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a8f78785fe3ee01237beb3477833584285e858035dd690fe36147bf54b5e4`  
		Last Modified: Fri, 17 Jan 2025 19:08:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2` - unknown; unknown

```console
$ docker pull composer@sha256:fe9fdae7536dd6a4da813df4818cf011312a8b9ed71e87c4473f093a5baffe68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbdcaf3013a5f9bb5078db2ed4b28ae50979b7586e1656243de036ea41468917`

```dockerfile
```

-	Layers:
	-	`sha256:8f3d1dce1d93bcd3141cfd5e981736383ac6350319e70eb2f8e69fa8aa492701`  
		Last Modified: Fri, 17 Jan 2025 19:08:49 GMT  
		Size: 2.2 MB (2156538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cf3f89998fc38d0a6a7f7b535745dd2a8be6729f4440068f1631641e4c07093`  
		Last Modified: Fri, 17 Jan 2025 19:08:49 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2`

```console
$ docker pull composer@sha256:f469b147bba65b0d595814f937130129fa125c9e0995039250222ccf71294c2f
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
$ docker pull composer@sha256:96793fabaa05186f59cd35f4197e63d18941383d12f778b1c02da27c9aff8ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74724790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4671a196c45a1995453d2c44f767096f05aa909dde13792a7c3db45540cc8427`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79c0dc8060e2f059662ca297aa3feae6b3652e5ce0ab171e72b087bec9eb496`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 3.3 MB (3333627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c72c57155ad8b911527445f9878aaf9a4be98da1365dc25227d456bbc357591`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235f6cd368cc120d2abc4c6cb424fde285daf59e2c3f78c72eaa5d14143b8ca`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abdd5367cc40b78b668ff086497ce457af0e483ed80d43df0d8939be0777869`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 13.6 MB (13591519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774922f802bd2f5aeddab05459b4faa03b0664c923d4d04e30d5a5d016662437`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245938a8f085f24c8cf3660fa4370cfad0223a42c79a99e915bbe89ff2910aeb`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.9 MB (20889503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893a8e1213f3e7623f34d6436a30f720ae4cb772c2bdb4e1308dd1333693fee2`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd82ceb5444495c6039a1591b24bb6cde1dd739805a599f07047bbac0e1e9ef`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1527141d4faeff5d269c76cd42a974a71e5c577bed2749951e40a2f5a4fd661e`  
		Last Modified: Fri, 17 Jan 2025 18:29:07 GMT  
		Size: 31.9 MB (31897780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c74ec0b371988df37d4c96b4165909c0d8d10f4ab0d0946ac19de4345f9445`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52fc5b87f24441faf972e9f07ae3b0904dc07ccfc7f816bdd08c82fdfd5cbec`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 1.3 MB (1345758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0b30d38f38f43d13e3639dd4817c354e8c4dac615f32c2088a167cdae8a557`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ddf37642fd1586646c6a31e21ba13ebe32541843f684a1aa9fae408b4059`  
		Last Modified: Fri, 17 Jan 2025 18:29:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:84e647b71bb52730bb9145e160956119e14a59d0f53dd557acbb8cfe05729b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af44d3c75c67fe75b574db0cc821d502082a45afddd97af6380ab523e2db9cd3`

```dockerfile
```

-	Layers:
	-	`sha256:ba1ed2d0559851dffc219873b41fc31fb5aee90b4757e2822328fd531f7fb1fb`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 2.2 MB (2158959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ffb6749672e92edf8f877fb3a289201371dfb52a31730f20574c58884a59ea6`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v6

```console
$ docker pull composer@sha256:b02c096257035cdc0a088905c39f1f55b2a80103184db02167244c1c3b7cf120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70768994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5935203ab018cd2ea7be4bea0ea407b982419a15fc0775ac8c15808c80ec2a60`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 08 Jan 2025 18:49:59 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c35832122daf4e6cfd46f0be114a1c6d91b28caceb8f9b86ccb0253e0678632`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 13.6 MB (13591522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abac4d6df3f8471bdecc32831cfc97f2c065ebc58af29566d6e67161775d19e0`  
		Last Modified: Fri, 17 Jan 2025 17:36:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2e9c673c0e2f9934f576e177ae7ca6da19e281e8237523ec2deaddd3b94bb9`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.0 MB (19026889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fed1b7e2d514321545f15b0b6088794d7792c9f6d76c05ea93a61a505107b0`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f1b1f6a6b1a43d58472514b514bd3dc9e1bea6c950d8157396f5af086179d`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1602695904d94b7c906ed6ec74d99f418f62b6c4568fbbad2ab38440a9d1523f`  
		Last Modified: Fri, 17 Jan 2025 18:28:47 GMT  
		Size: 30.6 MB (30642262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e61ca26b0794a9473633a58d896e1b0db4d23c3019d4bf7c5501224de9ae50`  
		Last Modified: Fri, 17 Jan 2025 18:28:46 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e175182fb0ff2c8693a41655bae2f111d3c95f1119b4d88fb43ca01932e3ee`  
		Last Modified: Fri, 17 Jan 2025 18:28:46 GMT  
		Size: 819.2 KB (819246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d76b9a3e1f7c21e5a182c9d58502bc43af53578e67a16921add85659a9209`  
		Last Modified: Thu, 12 Dec 2024 19:27:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2291e98374dab3cb8c942015f1f0ae8a8cfca7ed175f86c6e22983f7c64e38b4`  
		Last Modified: Fri, 17 Jan 2025 18:28:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:50e375a6f18042b23239c31345d0ac95931346f9d22672dfed2f940e0af8609e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe86566fb4099218ed93e4cc6d0d0d475cb6500cbc711f5acaf09e797645795`

```dockerfile
```

-	Layers:
	-	`sha256:123363b4dbc03d974bb8bcb10b11551fac061e94bc30ec22bd87af8303c4e8aa`  
		Last Modified: Fri, 17 Jan 2025 18:28:45 GMT  
		Size: 30.5 KB (30533 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm variant v7

```console
$ docker pull composer@sha256:d7245dcd145941c1c589cf04a2503c543de6eb75935a40f4b7758467ef62a312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68798531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dbfa3cf9fff0fc1761f56b386c9968073c08b90b2248ec39a2c685472c2bd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd50b568401204c1289c16767a7acc4d1073b759b096a454b243856d0c372e8`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 30.2 MB (30150787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653d3258e5cf9a2c21ab7508e95c806af126ebe35e115ff9cb054bdfc47dad1`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148d1e0b6399d41ad9bcd5213f31abd8773104383468ae5ce0efa9971456107f`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 810.3 KB (810270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ca19478abff7d0316cc8e35fb574bf6edfb3f50b0587a844fa77c82bfe56e`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bd72ec9791ff16d7b7c0f71f6c563016f5f5830afda6d83fb8cc1acbb0dde4`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:ad393f676ed5b81bd99a1705834fd0773c3a2c7c6caa5fbacb11141c6fa8b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fe1f14d3a8b572eb0102b67b7356390f4245063887de435928e3e942312d51`

```dockerfile
```

-	Layers:
	-	`sha256:5204a11d18ca79d192f7c167e64f96108193f5047a9d40e4ae431d8a8bda821c`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 2.2 MB (2159269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfe27a53b3160c4fd5a866347b86aaf4dca9d59a251de44e671e2767011d5e45`  
		Last Modified: Fri, 17 Jan 2025 19:00:16 GMT  
		Size: 30.7 KB (30748 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:c5ad6462bb1be9db72d1250864b15d5ec5708a874b235c30ba9c5cf8170134a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74198443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b659cf3a6e8d96a46803562e955322c833e5092ca2e2ba00c77c26e7622d9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ded2f1970092c503a682b521201d635e8da0ad60d85a3975060091b0f092d`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 13.6 MB (13591559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12833fff26b4ea2cc381b02e1323f22bd1ac14a4e52a6c8417bbaa55152bd4e`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c693c7cf8097154c6af6b666782076f82f2824477b99c90ff0ca4adb3dbf3cb`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 20.4 MB (20438477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a526ad694be5912a4e8430a6cc668e490cde1f20e6e2b3b004536d3c0a679c`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092dc5a53c2e0204ffcfdfa51a695d5cd5bce5efd0d5d3a58243608a7c6b688`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb5a4ba752055d65a4614132f2cf5a9e53ce62b1e4d38c29a132319b331092`  
		Last Modified: Fri, 17 Jan 2025 18:51:48 GMT  
		Size: 32.0 MB (32004216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99ebc1999608761928e8f7869e0332f0652885f6d3ec81a815c3af8606c258f`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f847085a1f57bb8121064d6658a7ee1eb3baed5cbf92678e08ecef7a994585`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 819.4 KB (819445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539026a99069ae2a8e895d884c899a0bdac4ff1a55bc1547f1af1db796e31bea`  
		Last Modified: Fri, 17 Jan 2025 18:51:47 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4cee27a10cd3a35e9482974a0b6f534b40ef20991e0a155083d9a9bb22688`  
		Last Modified: Fri, 17 Jan 2025 18:51:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:f87c7aae94bcba085e2d140981d6d3e0f7f25f3a6688a832191ff95797ff9cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e9ea99d292753f2fdabe9c27e5d1f65396054ff1adf5d1cc4104d53634bcef`

```dockerfile
```

-	Layers:
	-	`sha256:0d96f99686b59c25264f7002f82ece06bfd3d84e29737590cce75363ef72ef24`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 2.2 MB (2159093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8bdbac2ac63261c84692f7cec8668c9009a6ba646e548687005ca827f59e1e`  
		Last Modified: Fri, 17 Jan 2025 18:51:45 GMT  
		Size: 30.8 KB (30776 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; 386

```console
$ docker pull composer@sha256:eaecfa515406eb3d07b523a52feed3df0ffaca67ceb7b6efbcf32bbcb38419d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54605180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009f5668f5ce10d1ff9b81902c637d29269c45fb56eac820e0bfe466c4a000df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfcabeec76e82e774d4a80656efdfc79ff8f40c450fbdd73dd3f9950ceb81d`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 3.4 MB (3373778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d250fddeb1debe229bb3f39f26177002aa97298c86687390ec93c5560a19f`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211adc87542ef1dd59501ad1b38031188049730b7b2712675469c23330a736`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87e5b0c31577e6cc14f074a34f293cf80c8700b2325895b1e60d511618578a6`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 13.6 MB (13591509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c7e04c7c5fc0f3187954b25a758a9d80b000947e870a1b160927dca9d40ea`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7c2a142bbfe468340f79a720467957f43a6f702651de57e539baba60bed9ab`  
		Last Modified: Fri, 17 Jan 2025 17:35:40 GMT  
		Size: 21.4 MB (21405219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6e9c16628bd2c485e0f707d1d17f8bd3395400810810ed37be2ba3c51eb6b1`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac723b08e7819bbfef249f592e8c7e989e37423caf36f3a55b17f82f9725fd7d`  
		Last Modified: Fri, 17 Jan 2025 17:35:37 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12859eab84c5ae8830d9986463e7bf1df9a5a10b3f15ba1f87cee54b47b7d4`  
		Last Modified: Fri, 17 Jan 2025 18:29:16 GMT  
		Size: 11.4 MB (11422353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf60544407c44864858c12ddcc662afef315e00c32edf36e4bbc8a3a18f00962`  
		Last Modified: Fri, 17 Jan 2025 18:29:15 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8268087019df663ad3491825e5db6723d464ce8ca0a69425ba76d7f1bab262c5`  
		Last Modified: Fri, 17 Jan 2025 18:29:15 GMT  
		Size: 1.3 MB (1324297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76168d61806aebd72cbaa43e8e7070a3d7df56399dae47acc3ba794eb04def51`  
		Last Modified: Fri, 17 Jan 2025 18:29:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbcf3e062f41eab3a36cbc6bb70c357ccc2e87a41d7e17d33fd506e73302b44`  
		Last Modified: Fri, 17 Jan 2025 18:29:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:5a2af2645fae2aaf994b4ecffceb64c10370836dfdbe7aa33e9c71ec9be3329f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.2 KB (459243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5303fdb59a1c424d3b76813924136892b71761dca7a3b2d1f76f2e02957b287`

```dockerfile
```

-	Layers:
	-	`sha256:96d59d5bf45350f771ad1be8fc9d312ddd073d84a102c8fcafb731485c44d174`  
		Last Modified: Fri, 17 Jan 2025 18:29:14 GMT  
		Size: 428.6 KB (428617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3447110edac1628279af0ef635ed494e6fa9655445e7c10d5bd5e53dd59d9726`  
		Last Modified: Fri, 17 Jan 2025 18:29:14 GMT  
		Size: 30.6 KB (30626 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; ppc64le

```console
$ docker pull composer@sha256:7e19bfa629a6ca9702b685a24fbbb4c96062e44051dbcc4fb71520a76daaeac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76803537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3941a72e4749fbe47a57d951edf43c7a32e8f5dfac53c03e294368567a61b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b4383e34608c265e3fcbc92f32f5b8e945fc93e6ecdaee910fa87b61b91eb7`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 13.6 MB (13591557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e98b79c382ca554316b5d1b58a69661a67bd73dd451dd9abba75515417cbf`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127935b1403b47049e26eb8a451d0fe15bf3dad3927f479ecfaea54a6026fc5`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 21.8 MB (21795018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8ff0ba33694c0f44258826a3874aaba09beb6072bf0353bb8c47363c0352c`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a75fc421d956d999c53c8003d5e0e6d664732d35993de12ae6e2232c4b9f1da`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63365f65e1acf2e91a180d560297bef7c52ed1b068a3ac5e41cfcab736a1edad`  
		Last Modified: Fri, 17 Jan 2025 18:37:26 GMT  
		Size: 32.9 MB (32944628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7bf30775a0bd0ff25c3418afea9aaee7ede8783e218f3d3368cc426b619c01`  
		Last Modified: Fri, 17 Jan 2025 18:37:24 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6025f0e71117c7ecd74ec14ce9ba1d6103b63be4ddc3d84cac666297aefc13`  
		Last Modified: Fri, 17 Jan 2025 18:37:25 GMT  
		Size: 1.4 MB (1397672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c44e2c86f322d086f61bf528446b604c305a46faf3471a04fe644b3eddf19`  
		Last Modified: Fri, 17 Jan 2025 18:37:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8704a333d78fed49ffef9b72e2ef8f8391284ceaf7778ff2da5945b116d24334`  
		Last Modified: Fri, 17 Jan 2025 18:37:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:f1cbffdfb6478c2b7e756e0217e00c344029f3e2bf2ed0c36e10075cc58bee71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4cd54f9c1addf822120a6569948a43470ab69ea7039a7df644adabcda488b8`

```dockerfile
```

-	Layers:
	-	`sha256:5bb68d6df03abb8c8ff17f1fa35995b4214d8ff0ed457f89663dc6e4f06dcb46`  
		Last Modified: Fri, 17 Jan 2025 18:37:24 GMT  
		Size: 2.2 MB (2157516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9b47c98f10583927e0f2a65f971230eb17748b98446837fc61467e40e49c461`  
		Last Modified: Fri, 17 Jan 2025 18:37:23 GMT  
		Size: 30.7 KB (30698 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; riscv64

```console
$ docker pull composer@sha256:d6142384a723e761d160e5c298ec87f0a1e2b2000e303a26f0a50c75cee30eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73124156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e3774521d5a8b409c6320fbd1ae3a0efa06605d66c8005875cc06400a5fc45`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 08 Jan 2025 23:26:57 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 19:26:15 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 19:26:16 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 19:26:14 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680962a19a25c3960d22cb3a10ea5a2197502ebe67fe87e93e01d571dc161d6`  
		Last Modified: Sat, 18 Jan 2025 02:16:46 GMT  
		Size: 31.0 MB (31000955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b510b40be7ea214b9ab25bd8ec441bf4b4f4d23b112019f368e2f69c97d3d`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca3f716c7d6c07b7864ca90178cabd40ce3f35b799025dd92e78f2e27dfe257`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 1.4 MB (1378528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c980a2bb344d5beb98db8c599534ebaae15a96f41a2db56dd5e804ac618aca`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a09a2153130b477bc812dca95e9139ab9a573c13d965538024653ad1e726cba`  
		Last Modified: Sat, 18 Jan 2025 02:16:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:bf74a594aa130c5a8d0befc048d0d62b46acf5e1c9573858f09f5cd6d415b1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf3b4406ba22db0200b57763d9898909c2c0898d90154adf05be9044fb52e9f`

```dockerfile
```

-	Layers:
	-	`sha256:f07cfc696af4a1a70f60720a0bb1c52203011ddcdffbe286c7929dd9e956d83d`  
		Last Modified: Sat, 18 Jan 2025 02:16:41 GMT  
		Size: 2.2 MB (2156458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29537fa8b3bd01e77a70cbcd0660589967c286ab8fe9fae10d07afc93903c86d`  
		Last Modified: Sat, 18 Jan 2025 02:16:41 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2` - linux; s390x

```console
$ docker pull composer@sha256:ec748362bd43e5427c13ef6c988bfea050fd41ece701d8c431d7abac7752dbae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7005cb5e70f3ba1ecb117e125c4132fff05470bfcd5ad50a9d16460cb24d6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd3b180b852bfd68493c7e27214dde2fc3d4e836aabe9023ed45c8fb27e3e51`  
		Last Modified: Fri, 17 Jan 2025 19:06:19 GMT  
		Size: 31.7 MB (31677476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bc62e74286362c0d45e020cba1c516cb4c2cc297b67f803d103e9b29f070d`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f223a40dae18b4df58004cb809d24133b12b86d2f6ae4708d6916744fd7e2d03`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 1.4 MB (1383339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92b28f407c6bc36539330b131e61ffc84ffbbec00cd585d3ecdf5b2dc967cd9`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f421cc305f6e0885cda5e2955a8644b6f0594d5c9fa63e616ecbf61ef0941cd2`  
		Last Modified: Fri, 17 Jan 2025 19:06:19 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2` - unknown; unknown

```console
$ docker pull composer@sha256:72f286c27e585f98c52fbfb2fc5b5630cbb9f1bd4cc62e987ef389f819ca7b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f8316da92cb2ccf3d30559a7f004a6f9d44f67deccc5e03db5cc59a5fef3a0`

```dockerfile
```

-	Layers:
	-	`sha256:f660794c0517579b350fd0e018e612236719eb63a333a4d5bde12225b261bc1d`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 2.2 MB (2156244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90717b0136b64c73cc5df9de88d8f6bf319dc3ca502dbb96534538f4af82100b`  
		Last Modified: Fri, 17 Jan 2025 19:06:17 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.2.25`

```console
$ docker pull composer@sha256:f469b147bba65b0d595814f937130129fa125c9e0995039250222ccf71294c2f
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
$ docker pull composer@sha256:96793fabaa05186f59cd35f4197e63d18941383d12f778b1c02da27c9aff8ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74724790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4671a196c45a1995453d2c44f767096f05aa909dde13792a7c3db45540cc8427`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79c0dc8060e2f059662ca297aa3feae6b3652e5ce0ab171e72b087bec9eb496`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 3.3 MB (3333627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c72c57155ad8b911527445f9878aaf9a4be98da1365dc25227d456bbc357591`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235f6cd368cc120d2abc4c6cb424fde285daf59e2c3f78c72eaa5d14143b8ca`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abdd5367cc40b78b668ff086497ce457af0e483ed80d43df0d8939be0777869`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 13.6 MB (13591519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774922f802bd2f5aeddab05459b4faa03b0664c923d4d04e30d5a5d016662437`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245938a8f085f24c8cf3660fa4370cfad0223a42c79a99e915bbe89ff2910aeb`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.9 MB (20889503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893a8e1213f3e7623f34d6436a30f720ae4cb772c2bdb4e1308dd1333693fee2`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd82ceb5444495c6039a1591b24bb6cde1dd739805a599f07047bbac0e1e9ef`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1527141d4faeff5d269c76cd42a974a71e5c577bed2749951e40a2f5a4fd661e`  
		Last Modified: Fri, 17 Jan 2025 18:29:07 GMT  
		Size: 31.9 MB (31897780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c74ec0b371988df37d4c96b4165909c0d8d10f4ab0d0946ac19de4345f9445`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52fc5b87f24441faf972e9f07ae3b0904dc07ccfc7f816bdd08c82fdfd5cbec`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 1.3 MB (1345758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0b30d38f38f43d13e3639dd4817c354e8c4dac615f32c2088a167cdae8a557`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ddf37642fd1586646c6a31e21ba13ebe32541843f684a1aa9fae408b4059`  
		Last Modified: Fri, 17 Jan 2025 18:29:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:84e647b71bb52730bb9145e160956119e14a59d0f53dd557acbb8cfe05729b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af44d3c75c67fe75b574db0cc821d502082a45afddd97af6380ab523e2db9cd3`

```dockerfile
```

-	Layers:
	-	`sha256:ba1ed2d0559851dffc219873b41fc31fb5aee90b4757e2822328fd531f7fb1fb`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 2.2 MB (2158959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ffb6749672e92edf8f877fb3a289201371dfb52a31730f20574c58884a59ea6`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v6

```console
$ docker pull composer@sha256:b02c096257035cdc0a088905c39f1f55b2a80103184db02167244c1c3b7cf120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70768994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5935203ab018cd2ea7be4bea0ea407b982419a15fc0775ac8c15808c80ec2a60`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 08 Jan 2025 18:49:59 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c35832122daf4e6cfd46f0be114a1c6d91b28caceb8f9b86ccb0253e0678632`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 13.6 MB (13591522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abac4d6df3f8471bdecc32831cfc97f2c065ebc58af29566d6e67161775d19e0`  
		Last Modified: Fri, 17 Jan 2025 17:36:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2e9c673c0e2f9934f576e177ae7ca6da19e281e8237523ec2deaddd3b94bb9`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.0 MB (19026889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fed1b7e2d514321545f15b0b6088794d7792c9f6d76c05ea93a61a505107b0`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f1b1f6a6b1a43d58472514b514bd3dc9e1bea6c950d8157396f5af086179d`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1602695904d94b7c906ed6ec74d99f418f62b6c4568fbbad2ab38440a9d1523f`  
		Last Modified: Fri, 17 Jan 2025 18:28:47 GMT  
		Size: 30.6 MB (30642262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e61ca26b0794a9473633a58d896e1b0db4d23c3019d4bf7c5501224de9ae50`  
		Last Modified: Fri, 17 Jan 2025 18:28:46 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e175182fb0ff2c8693a41655bae2f111d3c95f1119b4d88fb43ca01932e3ee`  
		Last Modified: Fri, 17 Jan 2025 18:28:46 GMT  
		Size: 819.2 KB (819246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d76b9a3e1f7c21e5a182c9d58502bc43af53578e67a16921add85659a9209`  
		Last Modified: Thu, 12 Dec 2024 19:27:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2291e98374dab3cb8c942015f1f0ae8a8cfca7ed175f86c6e22983f7c64e38b4`  
		Last Modified: Fri, 17 Jan 2025 18:28:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:50e375a6f18042b23239c31345d0ac95931346f9d22672dfed2f940e0af8609e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe86566fb4099218ed93e4cc6d0d0d475cb6500cbc711f5acaf09e797645795`

```dockerfile
```

-	Layers:
	-	`sha256:123363b4dbc03d974bb8bcb10b11551fac061e94bc30ec22bd87af8303c4e8aa`  
		Last Modified: Fri, 17 Jan 2025 18:28:45 GMT  
		Size: 30.5 KB (30533 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm variant v7

```console
$ docker pull composer@sha256:d7245dcd145941c1c589cf04a2503c543de6eb75935a40f4b7758467ef62a312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68798531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dbfa3cf9fff0fc1761f56b386c9968073c08b90b2248ec39a2c685472c2bd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd50b568401204c1289c16767a7acc4d1073b759b096a454b243856d0c372e8`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 30.2 MB (30150787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653d3258e5cf9a2c21ab7508e95c806af126ebe35e115ff9cb054bdfc47dad1`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148d1e0b6399d41ad9bcd5213f31abd8773104383468ae5ce0efa9971456107f`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 810.3 KB (810270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ca19478abff7d0316cc8e35fb574bf6edfb3f50b0587a844fa77c82bfe56e`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bd72ec9791ff16d7b7c0f71f6c563016f5f5830afda6d83fb8cc1acbb0dde4`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:ad393f676ed5b81bd99a1705834fd0773c3a2c7c6caa5fbacb11141c6fa8b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fe1f14d3a8b572eb0102b67b7356390f4245063887de435928e3e942312d51`

```dockerfile
```

-	Layers:
	-	`sha256:5204a11d18ca79d192f7c167e64f96108193f5047a9d40e4ae431d8a8bda821c`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 2.2 MB (2159269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfe27a53b3160c4fd5a866347b86aaf4dca9d59a251de44e671e2767011d5e45`  
		Last Modified: Fri, 17 Jan 2025 19:00:16 GMT  
		Size: 30.7 KB (30748 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:c5ad6462bb1be9db72d1250864b15d5ec5708a874b235c30ba9c5cf8170134a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74198443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b659cf3a6e8d96a46803562e955322c833e5092ca2e2ba00c77c26e7622d9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ded2f1970092c503a682b521201d635e8da0ad60d85a3975060091b0f092d`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 13.6 MB (13591559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12833fff26b4ea2cc381b02e1323f22bd1ac14a4e52a6c8417bbaa55152bd4e`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c693c7cf8097154c6af6b666782076f82f2824477b99c90ff0ca4adb3dbf3cb`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 20.4 MB (20438477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a526ad694be5912a4e8430a6cc668e490cde1f20e6e2b3b004536d3c0a679c`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092dc5a53c2e0204ffcfdfa51a695d5cd5bce5efd0d5d3a58243608a7c6b688`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb5a4ba752055d65a4614132f2cf5a9e53ce62b1e4d38c29a132319b331092`  
		Last Modified: Fri, 17 Jan 2025 18:51:48 GMT  
		Size: 32.0 MB (32004216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99ebc1999608761928e8f7869e0332f0652885f6d3ec81a815c3af8606c258f`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f847085a1f57bb8121064d6658a7ee1eb3baed5cbf92678e08ecef7a994585`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 819.4 KB (819445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539026a99069ae2a8e895d884c899a0bdac4ff1a55bc1547f1af1db796e31bea`  
		Last Modified: Fri, 17 Jan 2025 18:51:47 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4cee27a10cd3a35e9482974a0b6f534b40ef20991e0a155083d9a9bb22688`  
		Last Modified: Fri, 17 Jan 2025 18:51:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:f87c7aae94bcba085e2d140981d6d3e0f7f25f3a6688a832191ff95797ff9cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e9ea99d292753f2fdabe9c27e5d1f65396054ff1adf5d1cc4104d53634bcef`

```dockerfile
```

-	Layers:
	-	`sha256:0d96f99686b59c25264f7002f82ece06bfd3d84e29737590cce75363ef72ef24`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 2.2 MB (2159093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8bdbac2ac63261c84692f7cec8668c9009a6ba646e548687005ca827f59e1e`  
		Last Modified: Fri, 17 Jan 2025 18:51:45 GMT  
		Size: 30.8 KB (30776 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; 386

```console
$ docker pull composer@sha256:eaecfa515406eb3d07b523a52feed3df0ffaca67ceb7b6efbcf32bbcb38419d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54605180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009f5668f5ce10d1ff9b81902c637d29269c45fb56eac820e0bfe466c4a000df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfcabeec76e82e774d4a80656efdfc79ff8f40c450fbdd73dd3f9950ceb81d`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 3.4 MB (3373778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d250fddeb1debe229bb3f39f26177002aa97298c86687390ec93c5560a19f`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211adc87542ef1dd59501ad1b38031188049730b7b2712675469c23330a736`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87e5b0c31577e6cc14f074a34f293cf80c8700b2325895b1e60d511618578a6`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 13.6 MB (13591509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c7e04c7c5fc0f3187954b25a758a9d80b000947e870a1b160927dca9d40ea`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7c2a142bbfe468340f79a720467957f43a6f702651de57e539baba60bed9ab`  
		Last Modified: Fri, 17 Jan 2025 17:35:40 GMT  
		Size: 21.4 MB (21405219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6e9c16628bd2c485e0f707d1d17f8bd3395400810810ed37be2ba3c51eb6b1`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac723b08e7819bbfef249f592e8c7e989e37423caf36f3a55b17f82f9725fd7d`  
		Last Modified: Fri, 17 Jan 2025 17:35:37 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12859eab84c5ae8830d9986463e7bf1df9a5a10b3f15ba1f87cee54b47b7d4`  
		Last Modified: Fri, 17 Jan 2025 18:29:16 GMT  
		Size: 11.4 MB (11422353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf60544407c44864858c12ddcc662afef315e00c32edf36e4bbc8a3a18f00962`  
		Last Modified: Fri, 17 Jan 2025 18:29:15 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8268087019df663ad3491825e5db6723d464ce8ca0a69425ba76d7f1bab262c5`  
		Last Modified: Fri, 17 Jan 2025 18:29:15 GMT  
		Size: 1.3 MB (1324297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76168d61806aebd72cbaa43e8e7070a3d7df56399dae47acc3ba794eb04def51`  
		Last Modified: Fri, 17 Jan 2025 18:29:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbcf3e062f41eab3a36cbc6bb70c357ccc2e87a41d7e17d33fd506e73302b44`  
		Last Modified: Fri, 17 Jan 2025 18:29:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:5a2af2645fae2aaf994b4ecffceb64c10370836dfdbe7aa33e9c71ec9be3329f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.2 KB (459243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5303fdb59a1c424d3b76813924136892b71761dca7a3b2d1f76f2e02957b287`

```dockerfile
```

-	Layers:
	-	`sha256:96d59d5bf45350f771ad1be8fc9d312ddd073d84a102c8fcafb731485c44d174`  
		Last Modified: Fri, 17 Jan 2025 18:29:14 GMT  
		Size: 428.6 KB (428617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3447110edac1628279af0ef635ed494e6fa9655445e7c10d5bd5e53dd59d9726`  
		Last Modified: Fri, 17 Jan 2025 18:29:14 GMT  
		Size: 30.6 KB (30626 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; ppc64le

```console
$ docker pull composer@sha256:7e19bfa629a6ca9702b685a24fbbb4c96062e44051dbcc4fb71520a76daaeac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76803537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3941a72e4749fbe47a57d951edf43c7a32e8f5dfac53c03e294368567a61b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b4383e34608c265e3fcbc92f32f5b8e945fc93e6ecdaee910fa87b61b91eb7`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 13.6 MB (13591557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e98b79c382ca554316b5d1b58a69661a67bd73dd451dd9abba75515417cbf`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127935b1403b47049e26eb8a451d0fe15bf3dad3927f479ecfaea54a6026fc5`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 21.8 MB (21795018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8ff0ba33694c0f44258826a3874aaba09beb6072bf0353bb8c47363c0352c`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a75fc421d956d999c53c8003d5e0e6d664732d35993de12ae6e2232c4b9f1da`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63365f65e1acf2e91a180d560297bef7c52ed1b068a3ac5e41cfcab736a1edad`  
		Last Modified: Fri, 17 Jan 2025 18:37:26 GMT  
		Size: 32.9 MB (32944628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7bf30775a0bd0ff25c3418afea9aaee7ede8783e218f3d3368cc426b619c01`  
		Last Modified: Fri, 17 Jan 2025 18:37:24 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6025f0e71117c7ecd74ec14ce9ba1d6103b63be4ddc3d84cac666297aefc13`  
		Last Modified: Fri, 17 Jan 2025 18:37:25 GMT  
		Size: 1.4 MB (1397672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c44e2c86f322d086f61bf528446b604c305a46faf3471a04fe644b3eddf19`  
		Last Modified: Fri, 17 Jan 2025 18:37:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8704a333d78fed49ffef9b72e2ef8f8391284ceaf7778ff2da5945b116d24334`  
		Last Modified: Fri, 17 Jan 2025 18:37:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:f1cbffdfb6478c2b7e756e0217e00c344029f3e2bf2ed0c36e10075cc58bee71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4cd54f9c1addf822120a6569948a43470ab69ea7039a7df644adabcda488b8`

```dockerfile
```

-	Layers:
	-	`sha256:5bb68d6df03abb8c8ff17f1fa35995b4214d8ff0ed457f89663dc6e4f06dcb46`  
		Last Modified: Fri, 17 Jan 2025 18:37:24 GMT  
		Size: 2.2 MB (2157516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9b47c98f10583927e0f2a65f971230eb17748b98446837fc61467e40e49c461`  
		Last Modified: Fri, 17 Jan 2025 18:37:23 GMT  
		Size: 30.7 KB (30698 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; riscv64

```console
$ docker pull composer@sha256:d6142384a723e761d160e5c298ec87f0a1e2b2000e303a26f0a50c75cee30eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73124156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e3774521d5a8b409c6320fbd1ae3a0efa06605d66c8005875cc06400a5fc45`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 08 Jan 2025 23:26:57 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 19:26:15 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 19:26:16 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 19:26:14 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680962a19a25c3960d22cb3a10ea5a2197502ebe67fe87e93e01d571dc161d6`  
		Last Modified: Sat, 18 Jan 2025 02:16:46 GMT  
		Size: 31.0 MB (31000955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b510b40be7ea214b9ab25bd8ec441bf4b4f4d23b112019f368e2f69c97d3d`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca3f716c7d6c07b7864ca90178cabd40ce3f35b799025dd92e78f2e27dfe257`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 1.4 MB (1378528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c980a2bb344d5beb98db8c599534ebaae15a96f41a2db56dd5e804ac618aca`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a09a2153130b477bc812dca95e9139ab9a573c13d965538024653ad1e726cba`  
		Last Modified: Sat, 18 Jan 2025 02:16:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:bf74a594aa130c5a8d0befc048d0d62b46acf5e1c9573858f09f5cd6d415b1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf3b4406ba22db0200b57763d9898909c2c0898d90154adf05be9044fb52e9f`

```dockerfile
```

-	Layers:
	-	`sha256:f07cfc696af4a1a70f60720a0bb1c52203011ddcdffbe286c7929dd9e956d83d`  
		Last Modified: Sat, 18 Jan 2025 02:16:41 GMT  
		Size: 2.2 MB (2156458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29537fa8b3bd01e77a70cbcd0660589967c286ab8fe9fae10d07afc93903c86d`  
		Last Modified: Sat, 18 Jan 2025 02:16:41 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.2.25` - linux; s390x

```console
$ docker pull composer@sha256:ec748362bd43e5427c13ef6c988bfea050fd41ece701d8c431d7abac7752dbae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7005cb5e70f3ba1ecb117e125c4132fff05470bfcd5ad50a9d16460cb24d6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd3b180b852bfd68493c7e27214dde2fc3d4e836aabe9023ed45c8fb27e3e51`  
		Last Modified: Fri, 17 Jan 2025 19:06:19 GMT  
		Size: 31.7 MB (31677476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bc62e74286362c0d45e020cba1c516cb4c2cc297b67f803d103e9b29f070d`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f223a40dae18b4df58004cb809d24133b12b86d2f6ae4708d6916744fd7e2d03`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 1.4 MB (1383339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92b28f407c6bc36539330b131e61ffc84ffbbec00cd585d3ecdf5b2dc967cd9`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f421cc305f6e0885cda5e2955a8644b6f0594d5c9fa63e616ecbf61ef0941cd2`  
		Last Modified: Fri, 17 Jan 2025 19:06:19 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.2.25` - unknown; unknown

```console
$ docker pull composer@sha256:72f286c27e585f98c52fbfb2fc5b5630cbb9f1bd4cc62e987ef389f819ca7b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f8316da92cb2ccf3d30559a7f004a6f9d44f67deccc5e03db5cc59a5fef3a0`

```dockerfile
```

-	Layers:
	-	`sha256:f660794c0517579b350fd0e018e612236719eb63a333a4d5bde12225b261bc1d`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 2.2 MB (2156244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90717b0136b64c73cc5df9de88d8f6bf319dc3ca502dbb96534538f4af82100b`  
		Last Modified: Fri, 17 Jan 2025 19:06:17 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8`

```console
$ docker pull composer@sha256:72b9e4b2038558f7256e7f925495aa791c0ee764e1d351f3963b379b18b4c2f5
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
$ docker pull composer@sha256:b0d1f86b249e8ad13385460acf91fe8981025254b1c99182c77ec2d5a2acb3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74867031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3068ed6d9d3483b75a985d9810de4e9f01aa7e5b0ed9d6a07d961341ff3b9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79c0dc8060e2f059662ca297aa3feae6b3652e5ce0ab171e72b087bec9eb496`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 3.3 MB (3333627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c72c57155ad8b911527445f9878aaf9a4be98da1365dc25227d456bbc357591`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235f6cd368cc120d2abc4c6cb424fde285daf59e2c3f78c72eaa5d14143b8ca`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abdd5367cc40b78b668ff086497ce457af0e483ed80d43df0d8939be0777869`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 13.6 MB (13591519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774922f802bd2f5aeddab05459b4faa03b0664c923d4d04e30d5a5d016662437`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245938a8f085f24c8cf3660fa4370cfad0223a42c79a99e915bbe89ff2910aeb`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.9 MB (20889503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893a8e1213f3e7623f34d6436a30f720ae4cb772c2bdb4e1308dd1333693fee2`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd82ceb5444495c6039a1591b24bb6cde1dd739805a599f07047bbac0e1e9ef`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92275c43a85b8aa4d5d29a473e99b45a0a58bd6fc3d19747ded8ae5bd5b09bfd`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 31.9 MB (31897758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b171394f04ec4be3ca122091116ef51e5b93e03f1441874fc269f3ea2cfbd90f`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b5efc53199ab0f27d01547156e5f9fc738c814b925906eee944a7e938e0ae2`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 1.5 MB (1488021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a2d00126212ed657639a3471bad1fe81be0e0e4d3f1c091efb1817bc80f3a0`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4f79a1f4e2be242c1bcf4ca94b21dbc50987dc8cfdce0671e018164c46e28`  
		Last Modified: Fri, 17 Jan 2025 18:29:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:e8c19a35ef2d84ce075be7d29ea8db42e0e32a403760c5c12a362691883578d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0f45264204260dad5a9d5efa4e9f92f8ad9d2a8978278eca6f925b1a99d205`

```dockerfile
```

-	Layers:
	-	`sha256:c3172cea930f51e6b3274339e20d769dd681448257536f8a40d8a170416908c4`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 2.2 MB (2159253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332c80b37d35b3ebe67ff7661823d9be1a091023a2057bba2db5985b99b3414e`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v6

```console
$ docker pull composer@sha256:7f141df4c345189f1873674d2f2b661b4dfc4f04e9581d152e671bbecdb2546a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70915330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b4d9b874548bc37e8d5b38772691b758116321780c007f1afe8769c416816f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 08 Jan 2025 18:49:59 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c35832122daf4e6cfd46f0be114a1c6d91b28caceb8f9b86ccb0253e0678632`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 13.6 MB (13591522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abac4d6df3f8471bdecc32831cfc97f2c065ebc58af29566d6e67161775d19e0`  
		Last Modified: Fri, 17 Jan 2025 17:36:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2e9c673c0e2f9934f576e177ae7ca6da19e281e8237523ec2deaddd3b94bb9`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.0 MB (19026889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fed1b7e2d514321545f15b0b6088794d7792c9f6d76c05ea93a61a505107b0`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f1b1f6a6b1a43d58472514b514bd3dc9e1bea6c950d8157396f5af086179d`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1602695904d94b7c906ed6ec74d99f418f62b6c4568fbbad2ab38440a9d1523f`  
		Last Modified: Fri, 17 Jan 2025 18:28:47 GMT  
		Size: 30.6 MB (30642262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e61ca26b0794a9473633a58d896e1b0db4d23c3019d4bf7c5501224de9ae50`  
		Last Modified: Fri, 17 Jan 2025 18:28:46 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4610cac406d8d57d794ab5c079a884d4b91acce4d551e6587b6eb74c784dde6c`  
		Last Modified: Fri, 17 Jan 2025 18:29:57 GMT  
		Size: 965.6 KB (965582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3826a6b574a6d595615f31b1ef9fae34a30dd1e418f79cee3bc7ab6a295e46ee`  
		Last Modified: Thu, 12 Dec 2024 19:28:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3c203e31a9b3ce363affb2b7bdad1da625d875ecac95065bedd70818887640`  
		Last Modified: Fri, 17 Jan 2025 18:29:57 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:e8c1b89db9235c3f2b590483301d18f71261a7ad139f41c2efd67067c0583605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cab451954bba3cfcefac968eb15ec096230128589be0c692014679eb36f0208`

```dockerfile
```

-	Layers:
	-	`sha256:a028c4ddb16f18673428b8b3b1051a9c5371bec27500fddcf29bc791172e21dc`  
		Last Modified: Fri, 17 Jan 2025 18:29:56 GMT  
		Size: 30.8 KB (30845 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm variant v7

```console
$ docker pull composer@sha256:f2775b2881f79afa2f5eae48c1e42efe9dd7a770edb4f9c50bd481f62eea5f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68945004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fb0a57178754951e43d36e9b3339fae42640a49ec81ebff948bd3dfdd194f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd50b568401204c1289c16767a7acc4d1073b759b096a454b243856d0c372e8`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 30.2 MB (30150787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653d3258e5cf9a2c21ab7508e95c806af126ebe35e115ff9cb054bdfc47dad1`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bb1d25f3841491b6bac119ae64d1347bc0a1b1254eb7b6124b2ff37bf7718b`  
		Last Modified: Fri, 17 Jan 2025 19:01:41 GMT  
		Size: 956.7 KB (956741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7daae6fd21bb945c0c6cda66b271b53494a15746ad03187c8f4c3091d9b4a7`  
		Last Modified: Fri, 17 Jan 2025 19:01:41 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4859256f8687c04b3166ccedb99b87aad36db1681edf9201e8955068d1a585`  
		Last Modified: Fri, 17 Jan 2025 19:01:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:85a9914de79bea623f353a8d8751970238dbbd1fe77a116d027e383c1911c258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d5389def231fdbc98394e6e3b762ff68cd55e7c474d8c444bb9c8a89c1e70f`

```dockerfile
```

-	Layers:
	-	`sha256:8f9b5db3de8336316eec834c847d89ff5f37ddc768dba303187202b6563384d0`  
		Last Modified: Fri, 17 Jan 2025 19:01:40 GMT  
		Size: 2.2 MB (2159571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a154e02ab0e548ed6a1684113b9857cf0776d1fef5dba6d6a8c6879333876dd9`  
		Last Modified: Fri, 17 Jan 2025 19:01:40 GMT  
		Size: 31.1 KB (31059 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:7c063c2c8a4d2322841db1784b242972de6103929049df728f2a06e1c24b11cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74344757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb86978297a92933cbbb7709acbd5835ea6273bf5366ecd5785ba2f390b2fe5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ded2f1970092c503a682b521201d635e8da0ad60d85a3975060091b0f092d`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 13.6 MB (13591559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12833fff26b4ea2cc381b02e1323f22bd1ac14a4e52a6c8417bbaa55152bd4e`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c693c7cf8097154c6af6b666782076f82f2824477b99c90ff0ca4adb3dbf3cb`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 20.4 MB (20438477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a526ad694be5912a4e8430a6cc668e490cde1f20e6e2b3b004536d3c0a679c`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092dc5a53c2e0204ffcfdfa51a695d5cd5bce5efd0d5d3a58243608a7c6b688`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb5a4ba752055d65a4614132f2cf5a9e53ce62b1e4d38c29a132319b331092`  
		Last Modified: Fri, 17 Jan 2025 18:51:48 GMT  
		Size: 32.0 MB (32004216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99ebc1999608761928e8f7869e0332f0652885f6d3ec81a815c3af8606c258f`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c9376466fb2ff8bc5528153d7f861f04995f0daa87b044e5525d9d8a40909f`  
		Last Modified: Fri, 17 Jan 2025 18:52:59 GMT  
		Size: 965.8 KB (965760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfa5bd629098bac4f5b8754994d5ae0b9470c39f074ad4d2b2472e0d4b48cd`  
		Last Modified: Fri, 17 Jan 2025 18:52:59 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4f60a0974f888f32ced79e6c2a4f32178d62863c80020590947e63fe98f206`  
		Last Modified: Fri, 17 Jan 2025 18:53:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:6f70519f4cd62d4aab830560dc8ae18c6848a2cd35e9d8ce385de0ad011a448d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256d25ea4546755db3302dff210d29cd5d78c4c16b49a3276b3fab0760e535f6`

```dockerfile
```

-	Layers:
	-	`sha256:cba006b914cec0703d0a33e228ae94a218f3a7ba8ef00a0ab6ef45d144207778`  
		Last Modified: Fri, 17 Jan 2025 18:52:58 GMT  
		Size: 2.2 MB (2159399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:985a870bb36e77fa6e85295356876be6db751e4a1375de124648887b21f26e1e`  
		Last Modified: Fri, 17 Jan 2025 18:52:58 GMT  
		Size: 31.1 KB (31091 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; 386

```console
$ docker pull composer@sha256:2850528275031a129a34ade0fa178e786068ef95773938bf2f22d3c893f91025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54747999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91daf8ffcc4aa2f14ee2a088fc525bd9a0f86849cbc0952c0f7b755ff91d99bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfcabeec76e82e774d4a80656efdfc79ff8f40c450fbdd73dd3f9950ceb81d`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 3.4 MB (3373778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d250fddeb1debe229bb3f39f26177002aa97298c86687390ec93c5560a19f`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211adc87542ef1dd59501ad1b38031188049730b7b2712675469c23330a736`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87e5b0c31577e6cc14f074a34f293cf80c8700b2325895b1e60d511618578a6`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 13.6 MB (13591509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c7e04c7c5fc0f3187954b25a758a9d80b000947e870a1b160927dca9d40ea`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7c2a142bbfe468340f79a720467957f43a6f702651de57e539baba60bed9ab`  
		Last Modified: Fri, 17 Jan 2025 17:35:40 GMT  
		Size: 21.4 MB (21405219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6e9c16628bd2c485e0f707d1d17f8bd3395400810810ed37be2ba3c51eb6b1`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac723b08e7819bbfef249f592e8c7e989e37423caf36f3a55b17f82f9725fd7d`  
		Last Modified: Fri, 17 Jan 2025 17:35:37 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0cb52933b74a8bd009eefe51cc608d16321e03af899e8cfdeb15ac3dcec360`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 11.4 MB (11422348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f69b64652dc4f61503554fe51944b51aa2b1a0de45969c509cebb5e2aee178`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b3f5bbe8654ef041dd9c306653961e4447c7ab54ac0c3086149958a1c9f3c4`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 1.5 MB (1467121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0b30d38f38f43d13e3639dd4817c354e8c4dac615f32c2088a167cdae8a557`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ddf37642fd1586646c6a31e21ba13ebe32541843f684a1aa9fae408b4059`  
		Last Modified: Fri, 17 Jan 2025 18:29:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:4a40599e138b4481df374b85d4d1858fd3902b9377986b77ff742e1e5bf108f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.8 KB (459831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93828c340e549a91e0b9a91b9a548ef84019770f9e6ee56b8a2a02709049b7bf`

```dockerfile
```

-	Layers:
	-	`sha256:2fd802b66bb8f9df09c89907a2ad1e36004e951a9e5991d7d569c61fd8e659df`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 428.9 KB (428906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fd2d904e4e5db8739d8fbda2129f1682bfa98eb21e864b62ce212939287c29`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; ppc64le

```console
$ docker pull composer@sha256:9da1507a1d17a5217c557bc8ef4727149d8c02f04b6a250ddcac2bc3f706bd37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76945265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1061d6a2c341df8b2294de4d117d80090b29b0c8a428bcf80d6e28f5836b96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b4383e34608c265e3fcbc92f32f5b8e945fc93e6ecdaee910fa87b61b91eb7`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 13.6 MB (13591557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e98b79c382ca554316b5d1b58a69661a67bd73dd451dd9abba75515417cbf`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127935b1403b47049e26eb8a451d0fe15bf3dad3927f479ecfaea54a6026fc5`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 21.8 MB (21795018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8ff0ba33694c0f44258826a3874aaba09beb6072bf0353bb8c47363c0352c`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a75fc421d956d999c53c8003d5e0e6d664732d35993de12ae6e2232c4b9f1da`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63365f65e1acf2e91a180d560297bef7c52ed1b068a3ac5e41cfcab736a1edad`  
		Last Modified: Fri, 17 Jan 2025 18:37:26 GMT  
		Size: 32.9 MB (32944628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7bf30775a0bd0ff25c3418afea9aaee7ede8783e218f3d3368cc426b619c01`  
		Last Modified: Fri, 17 Jan 2025 18:37:24 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd5e1913b7f8e9b6704b2e47884ccdd3b5d1e6424a19f53e91e02decc49ae4`  
		Last Modified: Fri, 17 Jan 2025 18:39:15 GMT  
		Size: 1.5 MB (1539398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5970900b0927fa0a730bdab2c0340e276db67dabf5f9cb0d023cbdebdfe3e51c`  
		Last Modified: Fri, 17 Jan 2025 18:39:15 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea8d3ad4cc5b3e229330f3b7ed1e831cada7cc8473ce4dcc54189ad951bf302`  
		Last Modified: Fri, 17 Jan 2025 18:39:15 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:a00c2a6b1b6e99304383ccacc1ac3c1e9a0f8be382e0a4b5dc1dff2d9c800710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f816122a748a29919a5bb7f8c0d167dd2373fea7b547daa11407fe753be12724`

```dockerfile
```

-	Layers:
	-	`sha256:da69f05cfb45c7c9c58c6aa383a17010c5777a996668a7cbb51d1623d85ddf36`  
		Last Modified: Fri, 17 Jan 2025 18:39:14 GMT  
		Size: 2.2 MB (2157816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c44cffb580860307d110d05c1f8e8fbc544878f905d9629695afdb0ca9eae8c`  
		Last Modified: Fri, 17 Jan 2025 18:39:14 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; riscv64

```console
$ docker pull composer@sha256:c50999d5b3bed5a8afc9d0ef596045b7f464fcdf7ed18339f4d856553b037c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73266527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae7a90617237ce4ca8ec221d9053df1dcb9d11ac3e2c6a1111e83843e3b948c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 08 Jan 2025 23:26:57 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 19:26:15 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 19:26:16 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 19:26:14 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680962a19a25c3960d22cb3a10ea5a2197502ebe67fe87e93e01d571dc161d6`  
		Last Modified: Sat, 18 Jan 2025 02:16:46 GMT  
		Size: 31.0 MB (31000955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b510b40be7ea214b9ab25bd8ec441bf4b4f4d23b112019f368e2f69c97d3d`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498d72bce4c2de0ffa86f86c00dd3bd54d3fbed403fee4717c9850665d0c8a9c`  
		Last Modified: Sat, 18 Jan 2025 02:27:09 GMT  
		Size: 1.5 MB (1520900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef3b442868969fb3a61dc6cd53d62dcc30465a773f95c5e798d6cabbfd2aa24`  
		Last Modified: Sat, 18 Jan 2025 02:27:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b6973f8270719e37a3cf40182c78acc208cd93c751c47493416ebd52763bd`  
		Last Modified: Sat, 18 Jan 2025 02:27:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:a18f431993c86eb84a67e0abfc762946793a5bfaf22a707b51e2c450f8275aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b22c3aee387fe25a95fe0325794c77927376f3f78daee3e4f7cb60fc694cb3`

```dockerfile
```

-	Layers:
	-	`sha256:d5a27470811617dd898ecffead1b6cc149e207bb50d23b53c447238db468a57f`  
		Last Modified: Sat, 18 Jan 2025 02:27:09 GMT  
		Size: 2.2 MB (2156758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db04b25fb3fc56c5f133c7a3d67bd3464eeb5933b7bfc5636da607b4aa61d3e`  
		Last Modified: Sat, 18 Jan 2025 02:27:08 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:2.8` - linux; s390x

```console
$ docker pull composer@sha256:77238e3ac94e54493c9cbdd764e469d8b564f61817c114b6c06146b3f9b9d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75224497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b952a8b1ed6779ed4535d0380817a48673eafd2a5ff17a50efb536f6b3d6ed6a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd3b180b852bfd68493c7e27214dde2fc3d4e836aabe9023ed45c8fb27e3e51`  
		Last Modified: Fri, 17 Jan 2025 19:06:19 GMT  
		Size: 31.7 MB (31677476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bc62e74286362c0d45e020cba1c516cb4c2cc297b67f803d103e9b29f070d`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511d99151c23495e84a0a38c4a514fd5f223b9e6bce6c20fed79eb4728f9fc96`  
		Last Modified: Fri, 17 Jan 2025 19:08:50 GMT  
		Size: 1.5 MB (1528656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb6ae28e53beaac1131bed1e3a97281cad10e9d502e8e224ff7310e2cd49b66`  
		Last Modified: Fri, 17 Jan 2025 19:08:50 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a8f78785fe3ee01237beb3477833584285e858035dd690fe36147bf54b5e4`  
		Last Modified: Fri, 17 Jan 2025 19:08:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:2.8` - unknown; unknown

```console
$ docker pull composer@sha256:fe9fdae7536dd6a4da813df4818cf011312a8b9ed71e87c4473f093a5baffe68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbdcaf3013a5f9bb5078db2ed4b28ae50979b7586e1656243de036ea41468917`

```dockerfile
```

-	Layers:
	-	`sha256:8f3d1dce1d93bcd3141cfd5e981736383ac6350319e70eb2f8e69fa8aa492701`  
		Last Modified: Fri, 17 Jan 2025 19:08:49 GMT  
		Size: 2.2 MB (2156538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cf3f89998fc38d0a6a7f7b535745dd2a8be6729f4440068f1631641e4c07093`  
		Last Modified: Fri, 17 Jan 2025 19:08:49 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:2.8.5`

```console
$ docker pull composer@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `composer:latest`

```console
$ docker pull composer@sha256:72b9e4b2038558f7256e7f925495aa791c0ee764e1d351f3963b379b18b4c2f5
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
$ docker pull composer@sha256:b0d1f86b249e8ad13385460acf91fe8981025254b1c99182c77ec2d5a2acb3bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74867031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b3068ed6d9d3483b75a985d9810de4e9f01aa7e5b0ed9d6a07d961341ff3b9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79c0dc8060e2f059662ca297aa3feae6b3652e5ce0ab171e72b087bec9eb496`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 3.3 MB (3333627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c72c57155ad8b911527445f9878aaf9a4be98da1365dc25227d456bbc357591`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235f6cd368cc120d2abc4c6cb424fde285daf59e2c3f78c72eaa5d14143b8ca`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abdd5367cc40b78b668ff086497ce457af0e483ed80d43df0d8939be0777869`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 13.6 MB (13591519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774922f802bd2f5aeddab05459b4faa03b0664c923d4d04e30d5a5d016662437`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245938a8f085f24c8cf3660fa4370cfad0223a42c79a99e915bbe89ff2910aeb`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.9 MB (20889503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893a8e1213f3e7623f34d6436a30f720ae4cb772c2bdb4e1308dd1333693fee2`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd82ceb5444495c6039a1591b24bb6cde1dd739805a599f07047bbac0e1e9ef`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92275c43a85b8aa4d5d29a473e99b45a0a58bd6fc3d19747ded8ae5bd5b09bfd`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 31.9 MB (31897758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b171394f04ec4be3ca122091116ef51e5b93e03f1441874fc269f3ea2cfbd90f`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19b5efc53199ab0f27d01547156e5f9fc738c814b925906eee944a7e938e0ae2`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 1.5 MB (1488021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a2d00126212ed657639a3471bad1fe81be0e0e4d3f1c091efb1817bc80f3a0`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b4f79a1f4e2be242c1bcf4ca94b21dbc50987dc8cfdce0671e018164c46e28`  
		Last Modified: Fri, 17 Jan 2025 18:29:13 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:e8c19a35ef2d84ce075be7d29ea8db42e0e32a403760c5c12a362691883578d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0f45264204260dad5a9d5efa4e9f92f8ad9d2a8978278eca6f925b1a99d205`

```dockerfile
```

-	Layers:
	-	`sha256:c3172cea930f51e6b3274339e20d769dd681448257536f8a40d8a170416908c4`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 2.2 MB (2159253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332c80b37d35b3ebe67ff7661823d9be1a091023a2057bba2db5985b99b3414e`  
		Last Modified: Fri, 17 Jan 2025 18:29:12 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v6

```console
$ docker pull composer@sha256:7f141df4c345189f1873674d2f2b661b4dfc4f04e9581d152e671bbecdb2546a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70915330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b4d9b874548bc37e8d5b38772691b758116321780c007f1afe8769c416816f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 08 Jan 2025 18:49:59 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c35832122daf4e6cfd46f0be114a1c6d91b28caceb8f9b86ccb0253e0678632`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 13.6 MB (13591522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abac4d6df3f8471bdecc32831cfc97f2c065ebc58af29566d6e67161775d19e0`  
		Last Modified: Fri, 17 Jan 2025 17:36:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2e9c673c0e2f9934f576e177ae7ca6da19e281e8237523ec2deaddd3b94bb9`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.0 MB (19026889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fed1b7e2d514321545f15b0b6088794d7792c9f6d76c05ea93a61a505107b0`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f1b1f6a6b1a43d58472514b514bd3dc9e1bea6c950d8157396f5af086179d`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1602695904d94b7c906ed6ec74d99f418f62b6c4568fbbad2ab38440a9d1523f`  
		Last Modified: Fri, 17 Jan 2025 18:28:47 GMT  
		Size: 30.6 MB (30642262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e61ca26b0794a9473633a58d896e1b0db4d23c3019d4bf7c5501224de9ae50`  
		Last Modified: Fri, 17 Jan 2025 18:28:46 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4610cac406d8d57d794ab5c079a884d4b91acce4d551e6587b6eb74c784dde6c`  
		Last Modified: Fri, 17 Jan 2025 18:29:57 GMT  
		Size: 965.6 KB (965582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3826a6b574a6d595615f31b1ef9fae34a30dd1e418f79cee3bc7ab6a295e46ee`  
		Last Modified: Thu, 12 Dec 2024 19:28:04 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3c203e31a9b3ce363affb2b7bdad1da625d875ecac95065bedd70818887640`  
		Last Modified: Fri, 17 Jan 2025 18:29:57 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:e8c1b89db9235c3f2b590483301d18f71261a7ad139f41c2efd67067c0583605
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cab451954bba3cfcefac968eb15ec096230128589be0c692014679eb36f0208`

```dockerfile
```

-	Layers:
	-	`sha256:a028c4ddb16f18673428b8b3b1051a9c5371bec27500fddcf29bc791172e21dc`  
		Last Modified: Fri, 17 Jan 2025 18:29:56 GMT  
		Size: 30.8 KB (30845 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm variant v7

```console
$ docker pull composer@sha256:f2775b2881f79afa2f5eae48c1e42efe9dd7a770edb4f9c50bd481f62eea5f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68945004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fb0a57178754951e43d36e9b3339fae42640a49ec81ebff948bd3dfdd194f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd50b568401204c1289c16767a7acc4d1073b759b096a454b243856d0c372e8`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 30.2 MB (30150787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653d3258e5cf9a2c21ab7508e95c806af126ebe35e115ff9cb054bdfc47dad1`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2bb1d25f3841491b6bac119ae64d1347bc0a1b1254eb7b6124b2ff37bf7718b`  
		Last Modified: Fri, 17 Jan 2025 19:01:41 GMT  
		Size: 956.7 KB (956741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7daae6fd21bb945c0c6cda66b271b53494a15746ad03187c8f4c3091d9b4a7`  
		Last Modified: Fri, 17 Jan 2025 19:01:41 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4859256f8687c04b3166ccedb99b87aad36db1681edf9201e8955068d1a585`  
		Last Modified: Fri, 17 Jan 2025 19:01:41 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:85a9914de79bea623f353a8d8751970238dbbd1fe77a116d027e383c1911c258
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58d5389def231fdbc98394e6e3b762ff68cd55e7c474d8c444bb9c8a89c1e70f`

```dockerfile
```

-	Layers:
	-	`sha256:8f9b5db3de8336316eec834c847d89ff5f37ddc768dba303187202b6563384d0`  
		Last Modified: Fri, 17 Jan 2025 19:01:40 GMT  
		Size: 2.2 MB (2159571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a154e02ab0e548ed6a1684113b9857cf0776d1fef5dba6d6a8c6879333876dd9`  
		Last Modified: Fri, 17 Jan 2025 19:01:40 GMT  
		Size: 31.1 KB (31059 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:7c063c2c8a4d2322841db1784b242972de6103929049df728f2a06e1c24b11cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74344757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb86978297a92933cbbb7709acbd5835ea6273bf5366ecd5785ba2f390b2fe5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ded2f1970092c503a682b521201d635e8da0ad60d85a3975060091b0f092d`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 13.6 MB (13591559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12833fff26b4ea2cc381b02e1323f22bd1ac14a4e52a6c8417bbaa55152bd4e`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c693c7cf8097154c6af6b666782076f82f2824477b99c90ff0ca4adb3dbf3cb`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 20.4 MB (20438477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a526ad694be5912a4e8430a6cc668e490cde1f20e6e2b3b004536d3c0a679c`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092dc5a53c2e0204ffcfdfa51a695d5cd5bce5efd0d5d3a58243608a7c6b688`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb5a4ba752055d65a4614132f2cf5a9e53ce62b1e4d38c29a132319b331092`  
		Last Modified: Fri, 17 Jan 2025 18:51:48 GMT  
		Size: 32.0 MB (32004216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99ebc1999608761928e8f7869e0332f0652885f6d3ec81a815c3af8606c258f`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c9376466fb2ff8bc5528153d7f861f04995f0daa87b044e5525d9d8a40909f`  
		Last Modified: Fri, 17 Jan 2025 18:52:59 GMT  
		Size: 965.8 KB (965760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfa5bd629098bac4f5b8754994d5ae0b9470c39f074ad4d2b2472e0d4b48cd`  
		Last Modified: Fri, 17 Jan 2025 18:52:59 GMT  
		Size: 420.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4f60a0974f888f32ced79e6c2a4f32178d62863c80020590947e63fe98f206`  
		Last Modified: Fri, 17 Jan 2025 18:53:00 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:6f70519f4cd62d4aab830560dc8ae18c6848a2cd35e9d8ce385de0ad011a448d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256d25ea4546755db3302dff210d29cd5d78c4c16b49a3276b3fab0760e535f6`

```dockerfile
```

-	Layers:
	-	`sha256:cba006b914cec0703d0a33e228ae94a218f3a7ba8ef00a0ab6ef45d144207778`  
		Last Modified: Fri, 17 Jan 2025 18:52:58 GMT  
		Size: 2.2 MB (2159399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:985a870bb36e77fa6e85295356876be6db751e4a1375de124648887b21f26e1e`  
		Last Modified: Fri, 17 Jan 2025 18:52:58 GMT  
		Size: 31.1 KB (31091 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; 386

```console
$ docker pull composer@sha256:2850528275031a129a34ade0fa178e786068ef95773938bf2f22d3c893f91025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54747999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91daf8ffcc4aa2f14ee2a088fc525bd9a0f86849cbc0952c0f7b755ff91d99bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfcabeec76e82e774d4a80656efdfc79ff8f40c450fbdd73dd3f9950ceb81d`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 3.4 MB (3373778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d250fddeb1debe229bb3f39f26177002aa97298c86687390ec93c5560a19f`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211adc87542ef1dd59501ad1b38031188049730b7b2712675469c23330a736`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87e5b0c31577e6cc14f074a34f293cf80c8700b2325895b1e60d511618578a6`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 13.6 MB (13591509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c7e04c7c5fc0f3187954b25a758a9d80b000947e870a1b160927dca9d40ea`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7c2a142bbfe468340f79a720467957f43a6f702651de57e539baba60bed9ab`  
		Last Modified: Fri, 17 Jan 2025 17:35:40 GMT  
		Size: 21.4 MB (21405219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6e9c16628bd2c485e0f707d1d17f8bd3395400810810ed37be2ba3c51eb6b1`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac723b08e7819bbfef249f592e8c7e989e37423caf36f3a55b17f82f9725fd7d`  
		Last Modified: Fri, 17 Jan 2025 17:35:37 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0cb52933b74a8bd009eefe51cc608d16321e03af899e8cfdeb15ac3dcec360`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 11.4 MB (11422348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f69b64652dc4f61503554fe51944b51aa2b1a0de45969c509cebb5e2aee178`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b3f5bbe8654ef041dd9c306653961e4447c7ab54ac0c3086149958a1c9f3c4`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 1.5 MB (1467121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0b30d38f38f43d13e3639dd4817c354e8c4dac615f32c2088a167cdae8a557`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ddf37642fd1586646c6a31e21ba13ebe32541843f684a1aa9fae408b4059`  
		Last Modified: Fri, 17 Jan 2025 18:29:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:4a40599e138b4481df374b85d4d1858fd3902b9377986b77ff742e1e5bf108f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.8 KB (459831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93828c340e549a91e0b9a91b9a548ef84019770f9e6ee56b8a2a02709049b7bf`

```dockerfile
```

-	Layers:
	-	`sha256:2fd802b66bb8f9df09c89907a2ad1e36004e951a9e5991d7d569c61fd8e659df`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 428.9 KB (428906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46fd2d904e4e5db8739d8fbda2129f1682bfa98eb21e864b62ce212939287c29`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 30.9 KB (30925 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; ppc64le

```console
$ docker pull composer@sha256:9da1507a1d17a5217c557bc8ef4727149d8c02f04b6a250ddcac2bc3f706bd37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76945265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1061d6a2c341df8b2294de4d117d80090b29b0c8a428bcf80d6e28f5836b96`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b4383e34608c265e3fcbc92f32f5b8e945fc93e6ecdaee910fa87b61b91eb7`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 13.6 MB (13591557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e98b79c382ca554316b5d1b58a69661a67bd73dd451dd9abba75515417cbf`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127935b1403b47049e26eb8a451d0fe15bf3dad3927f479ecfaea54a6026fc5`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 21.8 MB (21795018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8ff0ba33694c0f44258826a3874aaba09beb6072bf0353bb8c47363c0352c`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a75fc421d956d999c53c8003d5e0e6d664732d35993de12ae6e2232c4b9f1da`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63365f65e1acf2e91a180d560297bef7c52ed1b068a3ac5e41cfcab736a1edad`  
		Last Modified: Fri, 17 Jan 2025 18:37:26 GMT  
		Size: 32.9 MB (32944628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7bf30775a0bd0ff25c3418afea9aaee7ede8783e218f3d3368cc426b619c01`  
		Last Modified: Fri, 17 Jan 2025 18:37:24 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1fd5e1913b7f8e9b6704b2e47884ccdd3b5d1e6424a19f53e91e02decc49ae4`  
		Last Modified: Fri, 17 Jan 2025 18:39:15 GMT  
		Size: 1.5 MB (1539398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5970900b0927fa0a730bdab2c0340e276db67dabf5f9cb0d023cbdebdfe3e51c`  
		Last Modified: Fri, 17 Jan 2025 18:39:15 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea8d3ad4cc5b3e229330f3b7ed1e831cada7cc8473ce4dcc54189ad951bf302`  
		Last Modified: Fri, 17 Jan 2025 18:39:15 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:a00c2a6b1b6e99304383ccacc1ac3c1e9a0f8be382e0a4b5dc1dff2d9c800710
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f816122a748a29919a5bb7f8c0d167dd2373fea7b547daa11407fe753be12724`

```dockerfile
```

-	Layers:
	-	`sha256:da69f05cfb45c7c9c58c6aa383a17010c5777a996668a7cbb51d1623d85ddf36`  
		Last Modified: Fri, 17 Jan 2025 18:39:14 GMT  
		Size: 2.2 MB (2157816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c44cffb580860307d110d05c1f8e8fbc544878f905d9629695afdb0ca9eae8c`  
		Last Modified: Fri, 17 Jan 2025 18:39:14 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; riscv64

```console
$ docker pull composer@sha256:c50999d5b3bed5a8afc9d0ef596045b7f464fcdf7ed18339f4d856553b037c5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.3 MB (73266527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ae7a90617237ce4ca8ec221d9053df1dcb9d11ac3e2c6a1111e83843e3b948c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 08 Jan 2025 23:26:57 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 19:26:15 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 19:26:16 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 19:26:14 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680962a19a25c3960d22cb3a10ea5a2197502ebe67fe87e93e01d571dc161d6`  
		Last Modified: Sat, 18 Jan 2025 02:16:46 GMT  
		Size: 31.0 MB (31000955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b510b40be7ea214b9ab25bd8ec441bf4b4f4d23b112019f368e2f69c97d3d`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498d72bce4c2de0ffa86f86c00dd3bd54d3fbed403fee4717c9850665d0c8a9c`  
		Last Modified: Sat, 18 Jan 2025 02:27:09 GMT  
		Size: 1.5 MB (1520900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aef3b442868969fb3a61dc6cd53d62dcc30465a773f95c5e798d6cabbfd2aa24`  
		Last Modified: Sat, 18 Jan 2025 02:27:09 GMT  
		Size: 418.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b6973f8270719e37a3cf40182c78acc208cd93c751c47493416ebd52763bd`  
		Last Modified: Sat, 18 Jan 2025 02:27:09 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:a18f431993c86eb84a67e0abfc762946793a5bfaf22a707b51e2c450f8275aee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b22c3aee387fe25a95fe0325794c77927376f3f78daee3e4f7cb60fc694cb3`

```dockerfile
```

-	Layers:
	-	`sha256:d5a27470811617dd898ecffead1b6cc149e207bb50d23b53c447238db468a57f`  
		Last Modified: Sat, 18 Jan 2025 02:27:09 GMT  
		Size: 2.2 MB (2156758 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db04b25fb3fc56c5f133c7a3d67bd3464eeb5933b7bfc5636da607b4aa61d3e`  
		Last Modified: Sat, 18 Jan 2025 02:27:08 GMT  
		Size: 31.0 KB (31009 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:latest` - linux; s390x

```console
$ docker pull composer@sha256:77238e3ac94e54493c9cbdd764e469d8b564f61817c114b6c06146b3f9b9d443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75224497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b952a8b1ed6779ed4535d0380817a48673eafd2a5ff17a50efb536f6b3d6ed6a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:30:55 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:30:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:30:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:30:55 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:30:55 GMT
ENV COMPOSER_VERSION=2.8.4
# Thu, 12 Dec 2024 08:30:55 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:30:55 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:30:55 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:30:55 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd3b180b852bfd68493c7e27214dde2fc3d4e836aabe9023ed45c8fb27e3e51`  
		Last Modified: Fri, 17 Jan 2025 19:06:19 GMT  
		Size: 31.7 MB (31677476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bc62e74286362c0d45e020cba1c516cb4c2cc297b67f803d103e9b29f070d`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511d99151c23495e84a0a38c4a514fd5f223b9e6bce6c20fed79eb4728f9fc96`  
		Last Modified: Fri, 17 Jan 2025 19:08:50 GMT  
		Size: 1.5 MB (1528656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fb6ae28e53beaac1131bed1e3a97281cad10e9d502e8e224ff7310e2cd49b66`  
		Last Modified: Fri, 17 Jan 2025 19:08:50 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a8f78785fe3ee01237beb3477833584285e858035dd690fe36147bf54b5e4`  
		Last Modified: Fri, 17 Jan 2025 19:08:50 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:latest` - unknown; unknown

```console
$ docker pull composer@sha256:fe9fdae7536dd6a4da813df4818cf011312a8b9ed71e87c4473f093a5baffe68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbdcaf3013a5f9bb5078db2ed4b28ae50979b7586e1656243de036ea41468917`

```dockerfile
```

-	Layers:
	-	`sha256:8f3d1dce1d93bcd3141cfd5e981736383ac6350319e70eb2f8e69fa8aa492701`  
		Last Modified: Fri, 17 Jan 2025 19:08:49 GMT  
		Size: 2.2 MB (2156538 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cf3f89998fc38d0a6a7f7b535745dd2a8be6729f4440068f1631641e4c07093`  
		Last Modified: Fri, 17 Jan 2025 19:08:49 GMT  
		Size: 31.0 KB (30961 bytes)  
		MIME: application/vnd.in-toto+json

## `composer:lts`

```console
$ docker pull composer@sha256:f469b147bba65b0d595814f937130129fa125c9e0995039250222ccf71294c2f
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
$ docker pull composer@sha256:96793fabaa05186f59cd35f4197e63d18941383d12f778b1c02da27c9aff8ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74724790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4671a196c45a1995453d2c44f767096f05aa909dde13792a7c3db45540cc8427`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79c0dc8060e2f059662ca297aa3feae6b3652e5ce0ab171e72b087bec9eb496`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 3.3 MB (3333627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c72c57155ad8b911527445f9878aaf9a4be98da1365dc25227d456bbc357591`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f235f6cd368cc120d2abc4c6cb424fde285daf59e2c3f78c72eaa5d14143b8ca`  
		Last Modified: Fri, 17 Jan 2025 17:35:32 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2abdd5367cc40b78b668ff086497ce457af0e483ed80d43df0d8939be0777869`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 13.6 MB (13591519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:774922f802bd2f5aeddab05459b4faa03b0664c923d4d04e30d5a5d016662437`  
		Last Modified: Fri, 17 Jan 2025 17:35:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245938a8f085f24c8cf3660fa4370cfad0223a42c79a99e915bbe89ff2910aeb`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.9 MB (20889503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893a8e1213f3e7623f34d6436a30f720ae4cb772c2bdb4e1308dd1333693fee2`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd82ceb5444495c6039a1591b24bb6cde1dd739805a599f07047bbac0e1e9ef`  
		Last Modified: Fri, 17 Jan 2025 17:35:34 GMT  
		Size: 20.0 KB (20029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1527141d4faeff5d269c76cd42a974a71e5c577bed2749951e40a2f5a4fd661e`  
		Last Modified: Fri, 17 Jan 2025 18:29:07 GMT  
		Size: 31.9 MB (31897780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c74ec0b371988df37d4c96b4165909c0d8d10f4ab0d0946ac19de4345f9445`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52fc5b87f24441faf972e9f07ae3b0904dc07ccfc7f816bdd08c82fdfd5cbec`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 1.3 MB (1345758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0b30d38f38f43d13e3639dd4817c354e8c4dac615f32c2088a167cdae8a557`  
		Last Modified: Fri, 17 Jan 2025 18:29:03 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e714ddf37642fd1586646c6a31e21ba13ebe32541843f684a1aa9fae408b4059`  
		Last Modified: Fri, 17 Jan 2025 18:29:04 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:84e647b71bb52730bb9145e160956119e14a59d0f53dd557acbb8cfe05729b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af44d3c75c67fe75b574db0cc821d502082a45afddd97af6380ab523e2db9cd3`

```dockerfile
```

-	Layers:
	-	`sha256:ba1ed2d0559851dffc219873b41fc31fb5aee90b4757e2822328fd531f7fb1fb`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 2.2 MB (2158959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ffb6749672e92edf8f877fb3a289201371dfb52a31730f20574c58884a59ea6`  
		Last Modified: Fri, 17 Jan 2025 18:29:06 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v6

```console
$ docker pull composer@sha256:b02c096257035cdc0a088905c39f1f55b2a80103184db02167244c1c3b7cf120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70768994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5935203ab018cd2ea7be4bea0ea407b982419a15fc0775ac8c15808c80ec2a60`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 08 Jan 2025 18:49:59 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c35832122daf4e6cfd46f0be114a1c6d91b28caceb8f9b86ccb0253e0678632`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 13.6 MB (13591522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abac4d6df3f8471bdecc32831cfc97f2c065ebc58af29566d6e67161775d19e0`  
		Last Modified: Fri, 17 Jan 2025 17:36:05 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed2e9c673c0e2f9934f576e177ae7ca6da19e281e8237523ec2deaddd3b94bb9`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.0 MB (19026889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66fed1b7e2d514321545f15b0b6088794d7792c9f6d76c05ea93a61a505107b0`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632f1b1f6a6b1a43d58472514b514bd3dc9e1bea6c950d8157396f5af086179d`  
		Last Modified: Fri, 17 Jan 2025 17:36:06 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1602695904d94b7c906ed6ec74d99f418f62b6c4568fbbad2ab38440a9d1523f`  
		Last Modified: Fri, 17 Jan 2025 18:28:47 GMT  
		Size: 30.6 MB (30642262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e61ca26b0794a9473633a58d896e1b0db4d23c3019d4bf7c5501224de9ae50`  
		Last Modified: Fri, 17 Jan 2025 18:28:46 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e175182fb0ff2c8693a41655bae2f111d3c95f1119b4d88fb43ca01932e3ee`  
		Last Modified: Fri, 17 Jan 2025 18:28:46 GMT  
		Size: 819.2 KB (819246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386d76b9a3e1f7c21e5a182c9d58502bc43af53578e67a16921add85659a9209`  
		Last Modified: Thu, 12 Dec 2024 19:27:26 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2291e98374dab3cb8c942015f1f0ae8a8cfca7ed175f86c6e22983f7c64e38b4`  
		Last Modified: Fri, 17 Jan 2025 18:28:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:50e375a6f18042b23239c31345d0ac95931346f9d22672dfed2f940e0af8609e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fe86566fb4099218ed93e4cc6d0d0d475cb6500cbc711f5acaf09e797645795`

```dockerfile
```

-	Layers:
	-	`sha256:123363b4dbc03d974bb8bcb10b11551fac061e94bc30ec22bd87af8303c4e8aa`  
		Last Modified: Fri, 17 Jan 2025 18:28:45 GMT  
		Size: 30.5 KB (30533 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm variant v7

```console
$ docker pull composer@sha256:d7245dcd145941c1c589cf04a2503c543de6eb75935a40f4b7758467ef62a312
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68798531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99dbfa3cf9fff0fc1761f56b386c9968073c08b90b2248ec39a2c685472c2bd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af380792c6ed7330e643768bea28add4b6263c5a5c63fc16dc22a9b5eb71c54b`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 18.0 MB (18008759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecaa7045b5f7bb834783ff6d6a3a054c5fda6892335b75187aecd35a80995dc`  
		Last Modified: Fri, 17 Jan 2025 18:14:09 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a1694a29e45fa45acabb57b83407382b46f2539ac52e6a29667eaeeec7f470`  
		Last Modified: Fri, 17 Jan 2025 18:14:10 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd50b568401204c1289c16767a7acc4d1073b759b096a454b243856d0c372e8`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 30.2 MB (30150787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8653d3258e5cf9a2c21ab7508e95c806af126ebe35e115ff9cb054bdfc47dad1`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148d1e0b6399d41ad9bcd5213f31abd8773104383468ae5ce0efa9971456107f`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 810.3 KB (810270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:604ca19478abff7d0316cc8e35fb574bf6edfb3f50b0587a844fa77c82bfe56e`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bd72ec9791ff16d7b7c0f71f6c563016f5f5830afda6d83fb8cc1acbb0dde4`  
		Last Modified: Fri, 17 Jan 2025 19:00:18 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:ad393f676ed5b81bd99a1705834fd0773c3a2c7c6caa5fbacb11141c6fa8b7fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2190017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40fe1f14d3a8b572eb0102b67b7356390f4245063887de435928e3e942312d51`

```dockerfile
```

-	Layers:
	-	`sha256:5204a11d18ca79d192f7c167e64f96108193f5047a9d40e4ae431d8a8bda821c`  
		Last Modified: Fri, 17 Jan 2025 19:00:17 GMT  
		Size: 2.2 MB (2159269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cfe27a53b3160c4fd5a866347b86aaf4dca9d59a251de44e671e2767011d5e45`  
		Last Modified: Fri, 17 Jan 2025 19:00:16 GMT  
		Size: 30.7 KB (30748 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; arm64 variant v8

```console
$ docker pull composer@sha256:c5ad6462bb1be9db72d1250864b15d5ec5708a874b235c30ba9c5cf8170134a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.2 MB (74198443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b659cf3a6e8d96a46803562e955322c833e5092ca2e2ba00c77c26e7622d9a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ded2f1970092c503a682b521201d635e8da0ad60d85a3975060091b0f092d`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 13.6 MB (13591559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12833fff26b4ea2cc381b02e1323f22bd1ac14a4e52a6c8417bbaa55152bd4e`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c693c7cf8097154c6af6b666782076f82f2824477b99c90ff0ca4adb3dbf3cb`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 20.4 MB (20438477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a526ad694be5912a4e8430a6cc668e490cde1f20e6e2b3b004536d3c0a679c`  
		Last Modified: Fri, 17 Jan 2025 17:57:46 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f092dc5a53c2e0204ffcfdfa51a695d5cd5bce5efd0d5d3a58243608a7c6b688`  
		Last Modified: Fri, 17 Jan 2025 17:57:47 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb5a4ba752055d65a4614132f2cf5a9e53ce62b1e4d38c29a132319b331092`  
		Last Modified: Fri, 17 Jan 2025 18:51:48 GMT  
		Size: 32.0 MB (32004216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e99ebc1999608761928e8f7869e0332f0652885f6d3ec81a815c3af8606c258f`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f847085a1f57bb8121064d6658a7ee1eb3baed5cbf92678e08ecef7a994585`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 819.4 KB (819445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539026a99069ae2a8e895d884c899a0bdac4ff1a55bc1547f1af1db796e31bea`  
		Last Modified: Fri, 17 Jan 2025 18:51:47 GMT  
		Size: 421.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb4cee27a10cd3a35e9482974a0b6f534b40ef20991e0a155083d9a9bb22688`  
		Last Modified: Fri, 17 Jan 2025 18:51:47 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:f87c7aae94bcba085e2d140981d6d3e0f7f25f3a6688a832191ff95797ff9cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2189869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e9ea99d292753f2fdabe9c27e5d1f65396054ff1adf5d1cc4104d53634bcef`

```dockerfile
```

-	Layers:
	-	`sha256:0d96f99686b59c25264f7002f82ece06bfd3d84e29737590cce75363ef72ef24`  
		Last Modified: Fri, 17 Jan 2025 18:51:46 GMT  
		Size: 2.2 MB (2159093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e8bdbac2ac63261c84692f7cec8668c9009a6ba646e548687005ca827f59e1e`  
		Last Modified: Fri, 17 Jan 2025 18:51:45 GMT  
		Size: 30.8 KB (30776 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; 386

```console
$ docker pull composer@sha256:eaecfa515406eb3d07b523a52feed3df0ffaca67ceb7b6efbcf32bbcb38419d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54605180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:009f5668f5ce10d1ff9b81902c637d29269c45fb56eac820e0bfe466c4a000df`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfcabeec76e82e774d4a80656efdfc79ff8f40c450fbdd73dd3f9950ceb81d`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 3.4 MB (3373778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908d250fddeb1debe229bb3f39f26177002aa97298c86687390ec93c5560a19f`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9211adc87542ef1dd59501ad1b38031188049730b7b2712675469c23330a736`  
		Last Modified: Fri, 17 Jan 2025 17:35:35 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87e5b0c31577e6cc14f074a34f293cf80c8700b2325895b1e60d511618578a6`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 13.6 MB (13591509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152c7e04c7c5fc0f3187954b25a758a9d80b000947e870a1b160927dca9d40ea`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7c2a142bbfe468340f79a720467957f43a6f702651de57e539baba60bed9ab`  
		Last Modified: Fri, 17 Jan 2025 17:35:40 GMT  
		Size: 21.4 MB (21405219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6e9c16628bd2c485e0f707d1d17f8bd3395400810810ed37be2ba3c51eb6b1`  
		Last Modified: Fri, 17 Jan 2025 17:35:36 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac723b08e7819bbfef249f592e8c7e989e37423caf36f3a55b17f82f9725fd7d`  
		Last Modified: Fri, 17 Jan 2025 17:35:37 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e12859eab84c5ae8830d9986463e7bf1df9a5a10b3f15ba1f87cee54b47b7d4`  
		Last Modified: Fri, 17 Jan 2025 18:29:16 GMT  
		Size: 11.4 MB (11422353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf60544407c44864858c12ddcc662afef315e00c32edf36e4bbc8a3a18f00962`  
		Last Modified: Fri, 17 Jan 2025 18:29:15 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8268087019df663ad3491825e5db6723d464ce8ca0a69425ba76d7f1bab262c5`  
		Last Modified: Fri, 17 Jan 2025 18:29:15 GMT  
		Size: 1.3 MB (1324297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76168d61806aebd72cbaa43e8e7070a3d7df56399dae47acc3ba794eb04def51`  
		Last Modified: Fri, 17 Jan 2025 18:29:15 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fbcf3e062f41eab3a36cbc6bb70c357ccc2e87a41d7e17d33fd506e73302b44`  
		Last Modified: Fri, 17 Jan 2025 18:29:16 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:5a2af2645fae2aaf994b4ecffceb64c10370836dfdbe7aa33e9c71ec9be3329f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **459.2 KB (459243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5303fdb59a1c424d3b76813924136892b71761dca7a3b2d1f76f2e02957b287`

```dockerfile
```

-	Layers:
	-	`sha256:96d59d5bf45350f771ad1be8fc9d312ddd073d84a102c8fcafb731485c44d174`  
		Last Modified: Fri, 17 Jan 2025 18:29:14 GMT  
		Size: 428.6 KB (428617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3447110edac1628279af0ef635ed494e6fa9655445e7c10d5bd5e53dd59d9726`  
		Last Modified: Fri, 17 Jan 2025 18:29:14 GMT  
		Size: 30.6 KB (30626 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; ppc64le

```console
$ docker pull composer@sha256:7e19bfa629a6ca9702b685a24fbbb4c96062e44051dbcc4fb71520a76daaeac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76803537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db3941a72e4749fbe47a57d951edf43c7a32e8f5dfac53c03e294368567a61b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b4383e34608c265e3fcbc92f32f5b8e945fc93e6ecdaee910fa87b61b91eb7`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 13.6 MB (13591557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e98b79c382ca554316b5d1b58a69661a67bd73dd451dd9abba75515417cbf`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a127935b1403b47049e26eb8a451d0fe15bf3dad3927f479ecfaea54a6026fc5`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 21.8 MB (21795018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e8ff0ba33694c0f44258826a3874aaba09beb6072bf0353bb8c47363c0352c`  
		Last Modified: Fri, 17 Jan 2025 17:42:26 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a75fc421d956d999c53c8003d5e0e6d664732d35993de12ae6e2232c4b9f1da`  
		Last Modified: Fri, 17 Jan 2025 17:42:27 GMT  
		Size: 19.9 KB (19851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63365f65e1acf2e91a180d560297bef7c52ed1b068a3ac5e41cfcab736a1edad`  
		Last Modified: Fri, 17 Jan 2025 18:37:26 GMT  
		Size: 32.9 MB (32944628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7bf30775a0bd0ff25c3418afea9aaee7ede8783e218f3d3368cc426b619c01`  
		Last Modified: Fri, 17 Jan 2025 18:37:24 GMT  
		Size: 257.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6025f0e71117c7ecd74ec14ce9ba1d6103b63be4ddc3d84cac666297aefc13`  
		Last Modified: Fri, 17 Jan 2025 18:37:25 GMT  
		Size: 1.4 MB (1397672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090c44e2c86f322d086f61bf528446b604c305a46faf3471a04fe644b3eddf19`  
		Last Modified: Fri, 17 Jan 2025 18:37:25 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8704a333d78fed49ffef9b72e2ef8f8391284ceaf7778ff2da5945b116d24334`  
		Last Modified: Fri, 17 Jan 2025 18:37:08 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:f1cbffdfb6478c2b7e756e0217e00c344029f3e2bf2ed0c36e10075cc58bee71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2188214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4cd54f9c1addf822120a6569948a43470ab69ea7039a7df644adabcda488b8`

```dockerfile
```

-	Layers:
	-	`sha256:5bb68d6df03abb8c8ff17f1fa35995b4214d8ff0ed457f89663dc6e4f06dcb46`  
		Last Modified: Fri, 17 Jan 2025 18:37:24 GMT  
		Size: 2.2 MB (2157516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9b47c98f10583927e0f2a65f971230eb17748b98446837fc61467e40e49c461`  
		Last Modified: Fri, 17 Jan 2025 18:37:23 GMT  
		Size: 30.7 KB (30698 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; riscv64

```console
$ docker pull composer@sha256:d6142384a723e761d160e5c298ec87f0a1e2b2000e303a26f0a50c75cee30eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73124156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80e3774521d5a8b409c6320fbd1ae3a0efa06605d66c8005875cc06400a5fc45`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 08 Jan 2025 23:26:57 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 19:26:15 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b2e0734a505636d9a6882408cb59abcf1d4e724f5d8159c2b20c598356b52fd`  
		Last Modified: Fri, 17 Jan 2025 19:26:16 GMT  
		Size: 20.3 MB (20320244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74306690af56ad962cd04caf8cf5e2c63469c4a25d26fc20789e5bf2defdea29`  
		Last Modified: Fri, 17 Jan 2025 19:26:13 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d09a1e17cc19ca0bf76d8b675582f21ac7887cff99baf0591656050c3511b54`  
		Last Modified: Fri, 17 Jan 2025 19:26:14 GMT  
		Size: 19.8 KB (19838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0680962a19a25c3960d22cb3a10ea5a2197502ebe67fe87e93e01d571dc161d6`  
		Last Modified: Sat, 18 Jan 2025 02:16:46 GMT  
		Size: 31.0 MB (31000955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:264b510b40be7ea214b9ab25bd8ec441bf4b4f4d23b112019f368e2f69c97d3d`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca3f716c7d6c07b7864ca90178cabd40ce3f35b799025dd92e78f2e27dfe257`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 1.4 MB (1378528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c980a2bb344d5beb98db8c599534ebaae15a96f41a2db56dd5e804ac618aca`  
		Last Modified: Sat, 18 Jan 2025 02:16:42 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a09a2153130b477bc812dca95e9139ab9a573c13d965538024653ad1e726cba`  
		Last Modified: Sat, 18 Jan 2025 02:16:43 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:bf74a594aa130c5a8d0befc048d0d62b46acf5e1c9573858f09f5cd6d415b1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2187157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edf3b4406ba22db0200b57763d9898909c2c0898d90154adf05be9044fb52e9f`

```dockerfile
```

-	Layers:
	-	`sha256:f07cfc696af4a1a70f60720a0bb1c52203011ddcdffbe286c7929dd9e956d83d`  
		Last Modified: Sat, 18 Jan 2025 02:16:41 GMT  
		Size: 2.2 MB (2156458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29537fa8b3bd01e77a70cbcd0660589967c286ab8fe9fae10d07afc93903c86d`  
		Last Modified: Sat, 18 Jan 2025 02:16:41 GMT  
		Size: 30.7 KB (30699 bytes)  
		MIME: application/vnd.in-toto+json

### `composer:lts` - linux; s390x

```console
$ docker pull composer@sha256:ec748362bd43e5427c13ef6c988bfea050fd41ece701d8c431d7abac7752dbae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75079180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7005cb5e70f3ba1ecb117e125c4132fff05470bfcd5ad50a9d16460cb24d6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["composer"]`

```dockerfile
# Thu, 12 Dec 2024 08:31:09 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Dec 2024 08:31:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Dec 2024 08:31:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_VERSION=8.4.3
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Thu, 12 Dec 2024 08:31:09 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--enable-phpdbg 		--enable-phpdbg-readline 				--with-pear 			; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["php" "-a"]
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   apk add --no-cache --virtual .composer-rundeps     bash     coreutils     git     make     openssh-client     patch     subversion     tini     unzip     zip     $([ "$(apk --print-arch)" != "x86" ] && echo mercurial)     $([ "$(apk --print-arch)" != "armhf" ] && echo p7zip) # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
RUN printf "# composer php cli ini settings\ndate.timezone=UTC\nmemory_limit=-1\n" > $PHP_INI_DIR/php-cli.ini # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_HOME=/tmp
# Thu, 12 Dec 2024 08:31:09 GMT
ENV COMPOSER_VERSION=2.2.25
# Thu, 12 Dec 2024 08:31:09 GMT
RUN set -eux ;   curl     --silent     --fail     --location     --retry 3     --output /usr/local/bin/install-php-extensions     --url https://github.com/mlocati/docker-php-extension-installer/releases/download/1.2.58/install-php-extensions   ;   echo 182011b3dca5544a70fdeb587af44ed1760aa9a2ed37d787d0f280a99f92b008e638c37762360cd85583830a097665547849cb2293c4a0ee32c2a36ef7a349e2 /usr/local/bin/install-php-extensions | sha512sum --strict --check ;   chmod +x /usr/local/bin/install-php-extensions ;   install-php-extensions     bz2     zip   ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.dev.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/snapshots.pub   ;   echo 572b963c4b7512a7de3c71a788772440b1996d918b1d2b5354bf8ba2bb057fadec6f7ac4852f2f8a8c01ab94c18141ce0422aec3619354b057216e0597db5ac2 /tmp/keys.dev.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/keys.tags.pub     --url https://raw.githubusercontent.com/composer/composer.github.io/e7f28b7200249f8e5bc912b42837d4598c74153a/releases.pub   ;   echo 47f374b8840dcb0aa7b2327f13d24ab5f6ae9e58aa630af0d62b3d0ea114f4a315c5d97b21dcad3c7ffe2f0a95db2edec267adaba3f4f5a262abebe39aed3a28 /tmp/keys.tags.pub | sha512sum --strict --check ;   curl     --silent     --fail     --location     --retry 3     --output /tmp/installer.php     --url https://raw.githubusercontent.com/composer/getcomposer.org/f24b8f860b95b52167f91bbd3e3a7bcafe043038/web/installer   ;   echo 3137ad86bd990524ba1dedc2038309dfa6b63790d3ca52c28afea65dcc2eaead16fb33e9a72fd2a7a8240afaf26e065939a2d472f3b0eeaa575d1e8648f9bf19 /tmp/installer.php | sha512sum --strict --check ;   php /tmp/installer.php     --no-ansi     --install-dir=/usr/bin     --filename=composer     --version=${COMPOSER_VERSION}   ;   composer --ansi --version --no-interaction ;   rm -f /tmp/installer.php ;   find /tmp -type d -exec chmod -v 1777 {} + # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
COPY docker-entrypoint.sh /docker-entrypoint.sh # buildkit
# Thu, 12 Dec 2024 08:31:09 GMT
WORKDIR /app
# Thu, 12 Dec 2024 08:31:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 12 Dec 2024 08:31:09 GMT
CMD ["composer"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:042ce034e4627773d6ea167b16e0352b23628338f6241e9990bd8ed897ba572a`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 21.4 MB (21373958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3429aa8c1368d442190df362357ac521b89948235c9aac53b8e6930e06d14d5`  
		Last Modified: Fri, 17 Jan 2025 17:44:35 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fad2874686ae0adbe6c4585b617986f4411686fe64441db22ae97e5374978b10`  
		Last Modified: Fri, 17 Jan 2025 17:44:36 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd3b180b852bfd68493c7e27214dde2fc3d4e836aabe9023ed45c8fb27e3e51`  
		Last Modified: Fri, 17 Jan 2025 19:06:19 GMT  
		Size: 31.7 MB (31677476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10bc62e74286362c0d45e020cba1c516cb4c2cc297b67f803d103e9b29f070d`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f223a40dae18b4df58004cb809d24133b12b86d2f6ae4708d6916744fd7e2d03`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 1.4 MB (1383339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92b28f407c6bc36539330b131e61ffc84ffbbec00cd585d3ecdf5b2dc967cd9`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 419.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f421cc305f6e0885cda5e2955a8644b6f0594d5c9fa63e616ecbf61ef0941cd2`  
		Last Modified: Fri, 17 Jan 2025 19:06:19 GMT  
		Size: 93.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `composer:lts` - unknown; unknown

```console
$ docker pull composer@sha256:72f286c27e585f98c52fbfb2fc5b5630cbb9f1bd4cc62e987ef389f819ca7b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2186901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06f8316da92cb2ccf3d30559a7f004a6f9d44f67deccc5e03db5cc59a5fef3a0`

```dockerfile
```

-	Layers:
	-	`sha256:f660794c0517579b350fd0e018e612236719eb63a333a4d5bde12225b261bc1d`  
		Last Modified: Fri, 17 Jan 2025 19:06:18 GMT  
		Size: 2.2 MB (2156244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90717b0136b64c73cc5df9de88d8f6bf319dc3ca502dbb96534538f4af82100b`  
		Last Modified: Fri, 17 Jan 2025 19:06:17 GMT  
		Size: 30.7 KB (30657 bytes)  
		MIME: application/vnd.in-toto+json
